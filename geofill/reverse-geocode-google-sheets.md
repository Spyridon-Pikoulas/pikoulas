---
layout: page
title: "Reverse geocoding in Google Sheets™: latitude and longitude to address"
permalink: /geofill/reverse-geocode-google-sheets/
description: "Turn latitude and longitude into a street address, postcode, city, region and country in Google Sheets™, free with Google's geocoder, as a formula or as plain values."
---

# Reverse geocoding in Google Sheets™: latitude and longitude to address

Coordinates from a GPS log, a form or a phone are no use to someone reading a sheet. Google
Sheets™ has no function that turns them into an address. Its Apps Script, though, includes
Google's geocoder, the service Google Maps™ uses. You can call it for free, without an API key,
within a daily allowance: 1,000 lookups a day on a personal Google account, 10,000 on Google
Workspace™. Below are two ways to use it, and an add-on.

## 1. A formula: =ADDRESSPARTS(A2, B2)

Go to Extensions > Apps Script, replace everything in `Code.gs` with the code below, and save:

```js
/** =ADDRESSPARTS(A2, B2): the address, postcode, city, region and country at a latitude and longitude. */
function ADDRESSPARTS(lat, lng) {
  if (lat === '' || lng === '') return [['', '', '', '', '']];
  var cache = CacheService.getScriptCache(), key = lat + ',' + lng;
  var hit = cache.get(key);
  if (hit) return JSON.parse(hit);
  var r = Maps.newGeocoder().reverseGeocode(lat, lng).results[0];
  var out = [r ? parts(r) : ['not found', '', '', '', '']];
  cache.put(key, JSON.stringify(out), 21600);
  return out;
}

/** A geocoder result as [address, postcode, city, region, country]. */
function parts(r) {
  function find(type) {
    var c = r.address_components.filter(function (c) { return c.types.indexOf(type) >= 0; })[0];
    return c ? c.long_name : '';
  }
  return [r.formatted_address, find('postal_code'), find('locality') || find('postal_town'),
    find('administrative_area_level_1'), find('country')];
}
```

With the latitude in A and the longitude in B, type `=ADDRESSPARTS(A2, B2)` in C2 and fill it
down. It fills five cells to the right, so keep columns C to G empty. For example:

| Latitude | Longitude | Address | Postcode | City | Region | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 42.3601 | -71.0942 | 77 Massachusetts Ave, Cambridge, MA 02139, USA | 02139 | Cambridge | Massachusetts | United States |
| 48.8584 | 2.2945 | Tour Eiffel, 5 Av. Anatole France, 75007 Paris, France | 75007 | Paris | Île-de-France | France |
| 0 | 0 | not found | | | | |

It needs no authorization. The cache keeps each answer for six hours, so the recalculations
Sheets™ does now and then, for example when the file is opened, don't spend the allowance
again. For only the address, `=INDEX(ADDRESSPARTS(A2, B2), 1, 1)` gives one cell.

## 2. Fill the columns once, as plain values

For a long list, or addresses you want to keep, fill them once from a menu. Put the latitudes in
column A and the longitudes in B under a header row, add this to the script (next to the code
above, which it uses), and save:

```js
function onOpen() {
  SpreadsheetApp.getUi().createMenu('Geocode')
    .addItem('Fill addresses', 'fillAddresses')
    .addToUi();
}

/** Latitude in A, longitude in B from row 2: fills C to G where C is empty. */
function fillAddresses() {
  var sheet = SpreadsheetApp.getActiveSheet();
  if (sheet.getLastRow() < 2) return;
  sheet.getRange('D:D').setNumberFormat('@');  // postcodes stay text, leading zeros and all
  var range = sheet.getRange(2, 1, sheet.getLastRow() - 1, 7);
  var rows = range.getValues();
  var geocoder = Maps.newGeocoder(), started = Date.now();
  try {
    rows.forEach(function (row) {
      if (row[0] === '' || row[1] === '' || row[2] !== '' || Date.now() - started > 5 * 60 * 1000) return;
      var r = geocoder.reverseGeocode(row[0], row[1]).results[0];
      var p = r ? parts(r) : ['not found', '', '', '', ''];
      for (var i = 0; i < 5; i++) row[2 + i] = p[i];
    });
  } finally {
    range.setValues(rows);  // what was done is kept, even if the daily quota runs out midway
  }
}
```

Reload the spreadsheet, choose Geocode > Fill addresses, and authorize the script the first
time. It fills Address, Postcode, City, Region and Country in C to G.

- Rows that already have an address are skipped, so a second run carries on where the first
  stopped. A run stops after five minutes, because Apps Script ends any run at six.
- If the daily allowance runs out partway, the finished rows are kept.
- The postcode column is set to plain text first. Otherwise Sheets™ reads a postcode like 02139
  as the number 2139.
- It writes values back over columns A to G, so keep formulas out of those columns.

## Getting good results

- Latitude comes first, then longitude. Swapped, a point in Boston lands in Antarctica, and the
  answer is a Plus Code like `2HW4W946+82` instead of an address.
- Coordinates with a decimal comma, like `42,3601`, give an error. Replace the commas with points
  first (Edit > Find and replace).
- The geocoder answers with the nearest address it knows. For a landmark, a park or a field,
  that can be a neighbouring building or the road, so check any address that looks wrong on a map.
- A point in the sea, like 0, 0, has no address and shows "not found".

## 3. GeoFill (free for 100 a day)

[GeoFill](/geofill/) is the add-on I make for this, if you'd rather not keep a script. Go to
Extensions > GeoFill > Geocode addresses, choose "Coordinates to addresses", pick the Latitude
and Longitude columns, tick what you want, and click Geocode.

- It fills the full address, postcode, city, region, country and country code, in columns it
  adds and names.
- A Match column says how close each answer is (Exact, Street, Area or Approximate) or that
  nothing was found, so you know which rows to check.
- Under More options, it can give the results in another language.
- It carries on with a long list where it stopped, and skips rows that are already done.
- GeoFill Pro ($4.99 a month or $39 a year, 7 days free) adds the formula
  `=REVERSE_GEOCODE(B2:B100, C2:C100, "address, city")`, the `=GEOCODE()` formula for the other
  direction, and your own Google Maps Platform key past Google's daily allowance.

It has access only to the spreadsheet you open it in, not your other files.

For the other direction, addresses to coordinates, see
[Convert addresses to latitude and longitude in Google Sheets™](/geofill/address-to-lat-long-google-sheets/).
