---
layout: page
title: "Geocode by Awesome Table stopped working: geocoding addresses in Google Sheets™ now"
permalink: /geofill/geocode-by-awesome-table-alternative/
---

# Geocode by Awesome Table stopped working: geocoding addresses in Google Sheets™ now

For years, Geocode by Awesome Table was the add-on most people used to turn addresses in Google
Sheets™ into latitude and longitude, with almost 1.5 million installs. Its listing was last updated
in April 2024. If you install it today, it shows only a Help menu, and most of its reviews since
July 2026 say it no longer works.

If your map or delivery sheet depended on it, these are the ways that work today.

## 1. A few lines of Apps Script (free, up to 1,000 addresses a day)

Google Sheets™ can geocode without an API key through Apps Script's built-in Maps service. Go to
Extensions > Apps Script, replace everything in `Code.gs` with the code below, and save:

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

Then type `=LATLNG(A2)` and fill down. The latitude and longitude fill that cell and the one to its
right. This runs on your Google account's daily allowance: 1,000 addresses a day on a personal
account, 10,000 on Workspace. It gives only latitude and longitude, not the postcode or a cleaned-up
address. Sheets™ recalculates custom functions from time to time, and every recalculation geocodes
again, so keep the cache lines in.

[Convert addresses to latitude and longitude in Google Sheets™](/geofill/address-to-lat-long-google-sheets/)
has two more pieces of code: one that fills the columns once as plain values from a menu (better
for long lists), and one that turns coordinates back into addresses.

## 2. GeoFill (free for 100 a day, $4.99 a month for more)

I built [GeoFill](/geofill/) as the replacement I wanted. Go to Extensions > GeoFill > Geocode
addresses, pick the address column, tick what you want, and click Geocode. It fills in:

- latitude and longitude, the full formatted address, postcode or zip code, city, region, country
- a Match column (Exact, Street, Area, Approximate or Not found), so you know which rows to check

It also:

- joins an address split over two columns (street and city, say) and carries on with a long list
  where it stopped
- does reverse geocoding, from coordinates back to addresses
- adds, in Pro, `=GEOCODE()` and `=REVERSE_GEOCODE()` formulas and the option to use your own Maps
  Platform key past Google's daily allowance

It has access only to the spreadsheet you open it in, not your other files.

## 3. The US Census Geocoder (free, US addresses only)

The US Census Bureau's [Census Geocoder](https://geocoding.geo.census.gov/geocoder/) takes a CSV
file of up to 10,000 US addresses at a time (ID, street, city, state, ZIP) and gives it back with
coordinates. Download the sheet as CSV, upload it there, and paste the results back.

## Whichever you pick

Keep the coordinates as plain values once you have them. A formula that geocodes each time the
file opens spends your allowance again and again. To turn formulas into values, copy the cells,
then Edit > Paste special > Values only.
