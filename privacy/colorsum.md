---
layout: page
title: "ColorSum: Count & Sum Colored Cells by Color — Privacy Policy"
permalink: /privacy/colorsum/
---

# ColorSum: Count & Sum Colored Cells by Color — Privacy Policy

Last updated: 30 September 2026

ColorSum is an add-on for Google Sheets™ that counts and sums the cells of a spreadsheet by color.
This policy says what it does with data, including the Google user data it receives.

## What Google user data ColorSum accesses

- **The spreadsheet you use it in** (scope `spreadsheets.currentonly`). ColorSum reads the values
  and colors of the cells you select or name in its formulas, writes the formulas you ask for
  into the cell you select, and rewrites its own formulas to refresh them. It has no access to
  your other spreadsheets or files.
- **Your email address** (scope `userinfo.email`). It is how your subscription is found: ColorSum
  looks up the Stripe customer with this email and, when you start a checkout, creates one.
- **Sidebars and menus** (scope `script.container.ui`), to show ColorSum inside Sheets™.
- **A trigger in that spreadsheet** (scope `script.scriptapp`), only if you tick "Refresh them
  when a color changes": it refreshes ColorSum's formulas when a format changes there, and is
  deleted when you untick the box.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check and sell subscriptions.

## How ColorSum uses that data

- **Your cells** are read inside Google's Apps Script and the results are written back to your
  spreadsheet. They are not sent anywhere else and not stored by ColorSum outside your
  spreadsheet.
- **Your settings** (your plan status, your free uses of the day and your Stripe customer number)
  are kept in your own Google account's storage for the add-on. A spreadsheet in which a
  subscriber used ColorSum keeps the date until which its formulas work.
- **A count of your runs**: once ColorSum is on the Marketplace, the same storage counts the runs that
  did their job, so that after the third it can ask you, once, whether you would review it. It
  is used for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; ColorSum never sees your card. We can see in Stripe your email, your billing country
  and your subscription, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

ColorSum uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your email to
Stripe. ColorSum has no servers of its own. The contents of your spreadsheets are never sent to us
or to anyone else, and ColorSum uses no analytics.

ColorSum does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

ColorSum's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who ColorSum shares Google user data with

ColorSum shares, transfers or discloses Google user data only to these, and only for the purposes given:

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your plan and, when you buy, to create your customer record and take the
  payment. Stripe receives nothing else of your Google user data: no spreadsheet content.
- Your cells never leave Google's services: ColorSum reads them and writes its results back to
  your spreadsheet inside Google's Apps Script.

Nothing else is shared, transferred or disclosed: ColorSum does not sell, rent or trade Google user
data, and does not give it to advertisers, data brokers, analytics providers or any other third
party. We would disclose it only if the law required us to, and only what it required.

## How ColorSum protects that data

- **Encryption in transit.** Everything ColorSum sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your spreadsheet, ColorSum's settings and its error log are stored by
  Google, which encrypts the data it stores. Your customer record is stored by Stripe, which
  encrypts it too.
- **Access controls.** ColorSum runs inside Google's Apps Script, as you, with only the scopes
  above and only in the spreadsheet you open it in. We have no access to your spreadsheets or to
  your settings; only ColorSum, running as you, reads them. Your customer record sits in our
  Stripe account, which only we can sign in to. ColorSum reaches Stripe with a restricted key that
  stays on Google's servers and never reaches your browser.
- **Never stored**: the contents of your spreadsheet outside it, your card details, and your
  Google password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error, or the name of a
  sheet it could not find) goes to ColorSum's error log in Google Cloud™, which only we can read.

## Keeping and deleting

- The error log is deleted after 30 days.
- Your settings stay in your Google account's storage for ColorSum; they hold nothing from your
  spreadsheets. Uninstalling ColorSum (Extensions > Add-ons > Manage add-ons) stops it; removing it
  at https://myaccount.google.com/connections also ends its access to your account and its
  trigger, after which nothing reads them. The formulas' date kept in a spreadsheet stays in it and is deleted with it.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
