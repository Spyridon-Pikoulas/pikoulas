---
layout: page
title: "RandomFill: Random Number, Name & Team Generator — Privacy Policy"
permalink: /privacy/randomfill/
---

# RandomFill: Random Number, Name & Team Generator — Privacy Policy

Last updated: 27 October 2026

RandomFill is an add-on for Google Sheets™ that fills cells with random values, shuffles rows and
makes random teams. This policy says what it does with data, including the Google user data it
receives.

## What Google user data RandomFill accesses

- **The spreadsheet you use it in** (scope `spreadsheets.currentonly`). RandomFill reads the cells
  you select: whether they are filled, the list to pick from, the rows to shuffle or the column of
  names. When you write, it puts the values into the selected cells, reorders the selected rows,
  or adds a new tab of teams. It has no access to your other spreadsheets or files.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: RandomFill
  looks up the Stripe customer with this email and, when you start a checkout, creates one. It is
  also shown in RandomFill so you can check which Google account is used for your free fills and
  purchase. Google's installation screen may also say the add-on can 'associate you with your
  personal info on Google'. That is Google's standard sign-in association; RandomFill does not
  request, read or store your profile information.
- **Sidebars and menus** (scope `script.container.ui`), to show RandomFill inside Sheets™.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How RandomFill uses that data

- **Your cells** are read and the values made inside Google's Apps Script. For the preview, the
  values (and, for a shuffle or teams, the rows or names) are shown in the sidebar in your
  browser, and kept there only while it is open. What you write stays in your spreadsheet.
  Nothing from your cells is stored anywhere else or sent anywhere.
- **Passwords** are made inside Google's Apps Script with a cryptographically secure random
  source and written into the cells you select. We never see them, and they are not stored
  anywhere but your spreadsheet. There, anyone who can open the spreadsheet can see them, and
  its version history keeps them, even after the cells are cleared: move them to a password
  manager, then clear the cells.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own
  Google account's storage for the add-on.
- **Free allowance records**, in the same account storage, keep how many of your free fills are
  spent. The latest free fill adds a random identifier and fingerprint, its status and which kind
  of fill it was (such as numbers or teams), so that a fill is not counted twice. No cell
  contents, values or tab names are stored in these records.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; RandomFill never sees your card. We can see in Stripe your email, your billing country
  and your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

RandomFill uses Google user data only for the features above. It does not sell or rent it, does
not use it for advertising, and passes it to no one except as those features need: your email to
Stripe. RandomFill has no servers of its own. The contents of your spreadsheets, passwords
included, are never sent to us or to anyone else, and RandomFill uses no analytics.

RandomFill does not use Google user data, including data received from Google Workspace™ APIs,
to develop, improve or train AI or machine-learning models, generalized or personalized.

RandomFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who RandomFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no spreadsheet content.
- Your spreadsheet never leaves Google's services.

Nothing else is shared, transferred or disclosed: RandomFill does not sell, rent or trade Google
user data, and does not give it to advertisers, data brokers, analytics providers or any other
third party. We would disclose it only if the law required us to, and only what it required.

## How RandomFill protects that data

- **Encryption in transit.** Everything RandomFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your spreadsheet, RandomFill's settings and its error log are stored by
  Google, which encrypts the data it stores. Your customer record is stored by Stripe, which
  encrypts it too.
- **Access controls.** RandomFill runs inside Google's Apps Script, as you, with only the scopes
  above and only in the spreadsheet you open it in. We have no access to your spreadsheets or to
  your settings. Your customer record sits in our Stripe account, which only we can sign in to.
  RandomFill reaches Stripe with a restricted key that stays on Google's servers and never reaches
  your browser.
- **Never stored** outside your spreadsheet: your cells' contents and the passwords made. Never
  stored at all: your card details, and your Google password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error) goes to
  RandomFill's error log in Google Cloud™, which only we can read.

## Keeping and deleting

- The error log is deleted after 30 days.
- Free allowance records have no automatic expiry; the next free fill replaces the latest one's
  record without resetting the count used.
- Your settings and free allowance records stay in your Google account's storage for RandomFill
  and contain no cell contents. Uninstalling RandomFill (Extensions > Add-ons > Manage add-ons)
  stops it; removing it at https://myaccount.google.com/connections also ends its access to your
  account, after which nothing reads them.
- What RandomFill writes, passwords and teams tabs included, stays in your spreadsheet and its
  version history until you delete it.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The
  records of your payments are kept for five years after the end of the financial year they
  belong to, as Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
