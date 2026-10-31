---
layout: page
title: "SolveFill: Goal Seek & Linear Solver — Privacy Policy"
permalink: /privacy/solvefill/
---

# SolveFill: Goal Seek & Linear Solver — Privacy Policy

Last updated: 25 October 2026

SolveFill is an add-on for Google Sheets™ with Goal Seek and a solver for linear and integer
models. This policy says what it does with data, including the Google user data it receives.

## What Google user data SolveFill accesses

- **The spreadsheet you use it in** (scope `spreadsheets.currentonly`). SolveFill reads the cells of
  the model you enter: the objective or Set cell, the cells to change and the constraint cells. It
  changes the cells to change to read the model, puts them back, and writes the answer there, which
  you keep or restore. If you ask for them, it adds an Answer Report sheet and a sample model sheet.
  It has no access to your other spreadsheets or files.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: SolveFill looks
  up the Stripe customer with this email and, when you start a checkout, creates one. It is also
  shown in SolveFill so you can check which Google account is used for your free solves and
  purchase. Google's installation screen may also say the add-on can 'associate you with your
  personal info on Google'. That is Google's standard sign-in association; SolveFill does not
  request, read or store your profile information.
- **Sidebars and menus** (scope `script.container.ui`), to show SolveFill inside Sheets™.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How SolveFill uses that data

- **Your cells** are read inside Google's Apps Script, and models are solved there by Google's
  LinearOptimizationService. Answers are written to your spreadsheet. Your cells are not sent
  anywhere else.
- **The saved models, in the spreadsheet.** The last Goal Seek and the last solver model you ran
  (their cell references, sheet names, target values and options, but no cell contents) are saved
  in the spreadsheet's own storage for SolveFill, as Excel saves a Solver model in its workbook, so
  the sidebar opens on them. **Everyone who uses SolveFill in that spreadsheet can see them.** To
  remove them, open SolveFill in the spreadsheet and choose **Clear saved models**.
- **Original values, in the spreadsheet.** From the moment SolveFill first changes the cells to
  change until you keep the answer or restore, their original values are kept in the same storage,
  so they can be put back even if the solve is interrupted. They are deleted when you choose Keep or
  Restore, or when you start the next Goal Seek or solve.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own
  Google account's storage for the add-on.
- **Free allowance records**, in the same account storage, keep how many of your free solves are
  used. The latest solve adds a random identifier, a one-way fingerprint of the spreadsheet and its
  model, and its status, so that a retry is not counted twice. No cell values, sheet names or
  results are stored in these records.
- **A count of your runs**: once SolveFill is on the Marketplace, your account storage counts the
  solves that worked, so that after the third it can ask you, once, whether you would review it.
  It is used for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; SolveFill never sees your card. We can see in Stripe your email, your billing country
  and your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

SolveFill uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your email to
Stripe. SolveFill has no servers of its own. The contents of your spreadsheets are never sent to us
or to anyone else, and SolveFill uses no analytics.

SolveFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

SolveFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who SolveFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no spreadsheet content.
- **People you share the spreadsheet with** who use SolveFill in it see its saved models and, until
  you keep or restore, the original values of the last answer's cells, as they can see the cells
  themselves.
- Your cells never leave Google's services.

Nothing else is shared, transferred or disclosed: SolveFill does not sell, rent or trade Google
user data, and does not give it to advertisers, data brokers, analytics providers or any other
third party. We would disclose it only if the law required us to, and only what it required.

## How SolveFill protects that data

- **Encryption in transit.** Everything SolveFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your spreadsheet, its saved models and original values, SolveFill's
  settings and its error log are stored by Google, which encrypts the data it stores. Your customer
  record is stored by Stripe, which encrypts it too.
- **Access controls.** SolveFill runs inside Google's Apps Script, as you, with only the scopes
  above and only in the spreadsheet you open it in. We have no access to your spreadsheets or to
  your settings. Your customer record sits in our Stripe account, which only we can sign in to.
  SolveFill reaches Stripe with a restricted key that stays on Google's servers and never reaches
  your browser.
- **Never stored**: the contents of your spreadsheet outside it, your card details, and your Google
  password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error, or a sheet name or
  cell reference SolveFill could not use) goes to SolveFill's error log in Google Cloud™, which only
  we can read.

## Keeping and deleting

- The error log is deleted after 30 days.
- The saved models stay in the spreadsheet until you choose Clear saved models or the next model
  replaces them; original values, until you keep or restore. Deleting the spreadsheet deletes both.
- Free allowance records have no automatic expiry; the next solve replaces the latest one's record
  without resetting the count used.
- Your settings and free allowance records stay in your Google account's storage for SolveFill and
  contain no cell contents. Uninstalling SolveFill (Extensions > Add-ons > Manage add-ons) stops it;
  removing it at https://myaccount.google.com/connections also ends its access to your account,
  after which nothing reads them. The answers and sheets SolveFill wrote stay in your spreadsheet
  until you change or delete them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
