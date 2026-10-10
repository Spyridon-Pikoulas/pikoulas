---
layout: page
title: "GeoFill: Geocode Address to Lat Long Coordinates — Privacy Policy"
permalink: /privacy/geofill/
---

# GeoFill: Geocode Address to Lat Long Coordinates — Privacy Policy

Last updated: 30 September 2026

GeoFill is an add-on for Google Sheets™ that turns the addresses in a spreadsheet into latitude and
longitude, and coordinates back into addresses. This policy says what it does with data, including
the Google user data it receives.

## What Google user data GeoFill accesses

- **The spreadsheet you use it in** (scope `spreadsheets.currentonly`). GeoFill reads the header
  row and the columns you choose in the open spreadsheet, and writes the results into columns it
  adds there. It has no access to your other spreadsheets or files.
- **Your email address** (scope `userinfo.email`). It is how your subscription is found: GeoFill
  looks up the Stripe customer with this email and, when you start a checkout, creates one.
- **Sidebars and menus** (scope `script.container.ui`), to show GeoFill inside Sheets™.
- **Connections to outside services** (scope `script.external_request`), to exactly two: Stripe
  (`api.stripe.com`), to check and sell subscriptions, and, only if you save your own Maps
  Platform key, Google's Geocoding API (`maps.googleapis.com`).

## How GeoFill uses that data

- **Addresses and coordinates** you geocode are sent to Google's geocoding service (Apps Script's
  Maps service, or the Geocoding API with your own key), which returns the results. Google's
  [Privacy Policy](https://policies.google.com/privacy) applies to that request.
- **Results** are kept in Apps Script's cache for up to 6 hours, under a one-way hash of the
  address, so that geocoding the same address again does not spend your quota.
- **Your settings** (the options you picked, your plan status, your free uses of the day, your
  Stripe customer number and, if you saved one, your Maps Platform key) are kept in your own
  Google account's storage for the add-on. A spreadsheet in which a subscriber used GeoFill keeps
  the date until which its formulas work.
- **A count of your runs**: once GeoFill is on the Marketplace, the same storage counts the runs that
  did their job, so that after the third it can ask you, once, whether you would review it. It
  is used for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; GeoFill never sees your card. We can see in Stripe your email, your billing country and
  your subscription, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

GeoFill uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your addresses to
Google's geocoding service and your email to Stripe. GeoFill has no servers of its own. The
contents of your spreadsheets are never sent to us, and GeoFill uses no analytics.

GeoFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

GeoFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who GeoFill shares Google user data with

GeoFill shares, transfers or discloses Google user data only to these, and only for the purposes given:

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your plan and, when you buy, to create your customer record and take the
  payment. Stripe receives nothing else of your Google user data: no spreadsheet content.
- **Google's geocoding service** (Apps Script's Maps service, or Google's Geocoding API with your
  own key) receives the addresses or coordinates you geocode, and returns the results. It is
  part of Google; nothing is sent to any other geocoder.

Nothing else is shared, transferred or disclosed: GeoFill does not sell, rent or trade Google user
data, and does not give it to advertisers, data brokers, analytics providers or any other third
party. We would disclose it only if the law required us to, and only what it required.

## How GeoFill protects that data

- **Encryption in transit.** Everything GeoFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Google's geocoding service and to
  Stripe.
- **Encryption at rest.** Your spreadsheet, GeoFill's settings, its cache and its error log are
  stored by Google, which encrypts the data it stores. Your customer record is stored by Stripe,
  which encrypts it too.
- **Access controls.** GeoFill runs inside Google's Apps Script, as you, with only the scopes
  above and only in the spreadsheet you open it in. We have no access to your spreadsheets or to
  your settings; only GeoFill, running as you, reads them. Your customer record sits in our Stripe
  account, which only we can sign in to. GeoFill reaches Stripe with a restricted key that stays on
  Google's servers and never reaches your browser.
- **Never stored**: the contents of your spreadsheet outside it, your card details, and your
  Google password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error, or the name of a
  sheet it could not find) goes to GeoFill's error log in Google Cloud™, which only we can read.

## Keeping and deleting

- Geocoding results leave the cache within 6 hours, and the error log is deleted after 30 days.
- Your settings stay in your Google account's storage for GeoFill; they hold nothing from your
  spreadsheets. Uninstalling GeoFill (Extensions > Add-ons > Manage add-ons) stops it; removing it
  at https://myaccount.google.com/connections also ends its access to your account, after which
  nothing reads them. The formulas' date kept in a spreadsheet stays in it and is deleted with it.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
