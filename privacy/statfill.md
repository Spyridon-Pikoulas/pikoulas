---
layout: page
title: "StatFill: Statistics & Data Analysis Tools — Privacy Policy"
permalink: /privacy/statfill/
---

# StatFill: Statistics & Data Analysis Tools — Privacy Policy

Last updated: 28 October 2026

StatFill is an add-on for Google Sheets™ that computes statistics tables from a spreadsheet's
data. This policy says what it does with data, including the Google user data it receives.

## What Google user data StatFill accesses

- **The spreadsheet you use it in** (scope `spreadsheets.currentonly`). StatFill reads the ranges
  you enter or select, and writes each table to a new sheet or to the Output Range you choose
  there, after asking you if that range has filled cells. It has no access to your other
  spreadsheets or files.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: StatFill looks
  up the Stripe customer with this email and, when you start a checkout, creates one. It is also
  shown in StatFill so you can check which Google account is used for your free analyses and
  purchase. Google's installation screen may also say the add-on can 'associate you with your
  personal info on Google'. That is Google's standard sign-in association; StatFill does not
  request, read or store your profile information.
- **Sidebars and menus** (scope `script.container.ui`), to show StatFill inside Sheets™.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How StatFill uses that data

- **Your cells** are read inside Google's Apps Script, and the tables and charts computed from them are
  written to your spreadsheet. They are not sent anywhere else and not stored by StatFill outside
  your spreadsheet.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own
  Google account's storage for the add-on.
- **Free allowance records**, in the same storage, keep how many of your free analyses are used.
  The latest analysis adds a random identifier, a one-way fingerprint of its ranges, options and
  output place, and its status, so that a retry is not counted twice. No cell values, sheet names
  or results are stored in these records.
- **A count of your runs**: once StatFill is on the Marketplace, the same storage counts the
  analyses that worked, so that after the third it can ask you, once, whether you would review it.
  It is used for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; StatFill never sees your card. We can see in Stripe your email, your billing country and
  your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

StatFill uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your email to
Stripe. StatFill has no servers of its own. The contents of your spreadsheets are never sent to us
or to anyone else, and StatFill uses no analytics.

StatFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

StatFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who StatFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no spreadsheet content.
- Your cells never leave Google's services.

Nothing else is shared, transferred or disclosed: StatFill does not sell, rent or trade Google user
data, and does not give it to advertisers, data brokers, analytics providers or any other third
party. We would disclose it only if the law required us to, and only what it required.

## How StatFill protects that data

- **Encryption in transit.** Everything StatFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your spreadsheet, StatFill's settings and its error log are stored by
  Google, which encrypts the data it stores. Your customer record is stored by Stripe, which
  encrypts it too.
- **Access controls.** StatFill runs inside Google's Apps Script, as you, with only the scopes above
  and only in the spreadsheet you open it in. We have no access to your spreadsheets or to your
  settings. Your customer record sits in our Stripe account, which only we can sign in to. StatFill
  reaches Stripe with a restricted key that stays on Google's servers and never reaches your
  browser.
- **Never stored**: the contents of your spreadsheet outside it, your card details, and your Google
  password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error, or a sheet name or cell
  reference StatFill could not use) goes to StatFill's error log in Google Cloud™, which only we can read.

## Keeping and deleting

- The error log is deleted after 30 days.
- Free allowance records have no automatic expiry; the next analysis replaces the latest one's
  record without resetting the count used.
- Your settings and free allowance records stay in your Google account's storage for StatFill and
  contain no cell contents. Uninstalling StatFill (Extensions > Add-ons > Manage add-ons) stops it;
  removing it at https://myaccount.google.com/connections also ends its access to your account,
  after which nothing reads them. The tables StatFill wrote stay in your spreadsheet until you
  delete them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
