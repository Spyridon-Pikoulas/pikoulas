---
layout: page
title: "Convert addresses to latitude and longitude in Google Sheets™"
permalink: /geofill/address-to-lat-long-google-sheets/
---

# Convert addresses to latitude and longitude in Google Sheets™

Google Sheets™ has no built-in function that turns an address into coordinates. Its Apps Script,
though, includes Google's geocoder, the service Google Maps™ uses to find an address. You can call
it for free, without an API key, within a daily allowance: 1,000 addresses a day on a personal
Google account, 10,000 on Google Workspace™. Below are three ways to use it, plus an add-on and two
options without Sheets™.

## 1. A formula: =LATLNG(A2)

Go to Extensions > Apps Script, replace everything in `Code.gs` with the code below, and save:

```js
/** =LATLNG(A2): latitude and longitude of an address, in two cells. */
function LATLNG(address) {
  if (!address) return [['', '']];
  var cache = CacheService.getScriptCache();
  var key = Utilities.base64Encode(
      Utilities.computeDigest(Utilities.DigestAlgorithm.MD5, String(address)));
  var hit = cache.get(key);
  if (hit) return JSON.parse(hit);
  var r = Maps.newGeocoder().geocode(address).results[0];
  var out = r ? [[r.geometry.location.lat, r.geometry.location.lng]] : [['not found', '']];
  cache.put(key, JSON.stringify(out), 21600);
  return out;
}
```

Type `=LATLNG(A2)` next to your first address and fill it down. The latitude lands in that cell
and the longitude in the one to its right, so keep the column to its right empty. It needs no
authorization. An address the geocoder can't place shows "not found".

Sheets™ recalculates custom functions now and then, for example when the file is opened, and every
recalculation would geocode again and spend the allowance. The cache stops that for six hours at
a time. For a long list, or coordinates you want to keep, the next way is better.

## 2. Fill the columns once, as plain values

This version adds a menu that fills columns B and C with plain numbers, so the list is geocoded
once and never again. Put the addresses in column A under a header row, then use this as
`Code.gs` (it can sit next to LATLNG):

```js
function onOpen() {
  SpreadsheetApp.getUi().createMenu('Geocode')
    .addItem('Fill latitude and longitude', 'fillLatLng')
    .addToUi();
}

/** Addresses in column A from row 2: fills B (latitude) and C (longitude) where B is empty. */
function fillLatLng() {
  var sheet = SpreadsheetApp.getActiveSheet();
  if (sheet.getLastRow() < 2) return;
  var range = sheet.getRange(2, 1, sheet.getLastRow() - 1, 3);
  var rows = range.getValues();
  var geocoder = Maps.newGeocoder(), started = Date.now();
  try {
    rows.forEach(function (row) {
      if (!row[0] || row[1] !== '' || Date.now() - started > 5 * 60 * 1000) return;
      var r = geocoder.geocode(row[0]).results[0];
      row[1] = r ? r.geometry.location.lat : 'not found';
      row[2] = r ? r.geometry.location.lng : '';
    });
  } finally {
    range.setValues(rows);  // what was done is kept, even if the daily quota runs out midway
  }
}
```

Reload the spreadsheet, then choose Geocode > Fill latitude and longitude, and authorize the script
the first time. Rows that already have a latitude are skipped, so the script carries on where the
last run stopped. A run stops after five minutes, because Apps Script ends any run at six, so run
it again if some rows are left. If the daily allowance runs out partway, the finished rows are
kept, and the next day's run does the rest.

## 3. Coordinates back to an address

Reverse geocoding works the same way. Add this to the script and use `=ADDRESSOF(B2, C2)`:

```js
/** =ADDRESSOF(B2, C2): the address at a latitude and longitude. */
function ADDRESSOF(lat, lng) {
  if (lat === '' || lng === '') return '';
  var r = Maps.newGeocoder().reverseGeocode(lat, lng).results[0];
  return r ? r.formatted_address : 'not found';
}
```

## Getting good results

- Give the geocoder full addresses with the city and country. "12 Main Street" alone matches
  whichever Main Street it finds first.
- The scripts take the geocoder's first answer. That answer can be a street or a whole town
  rather than the exact building, so check any point that looks wrong on a map.
- If an address is split over several columns, join them first, e.g.
  `=TEXTJOIN(", ", TRUE, A2:C2)`, and geocode that column.

## 4. GeoFill (free for 100 addresses a day)

[GeoFill](/geofill/) is the add-on I make for this, if you'd rather not keep a script. Go to
Extensions > GeoFill > Geocode addresses, pick the address column, tick what you want, and click
Geocode. It adds these columns:

- latitude and longitude, the full formatted address, postcode or zip code, city, region, country
  and country code
- a Match column (Exact, Street, Area, Approximate or Not found), so you know which rows to check

It joins an address split over two columns, and a long list carries on where it stopped. It also
does coordinates to addresses. GeoFill Pro ($4.99 a month) adds `=GEOCODE()` and
`=REVERSE_GEOCODE()` formulas and the option to use your own Google Maps™ Platform key past the
daily allowance. It has access only to the spreadsheet you open it in.

## Without Sheets™

- **A few places**: in Google Maps™, right-click the spot. The coordinates are the first line of
  the menu, and clicking them copies them.
- **Many US addresses**: the US Census Bureau's free
  [Census Geocoder](https://geocoding.geo.census.gov/geocoder/) takes a file of up to 10,000
  addresses at a time and returns the coordinates.
