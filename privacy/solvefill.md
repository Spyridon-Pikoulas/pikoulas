---
layout: page
title: "SolveFill: What-If Analysis, Goal Seek & Solver — Privacy Policy"
permalink: /privacy/solvefill/
---

# SolveFill: What-If Analysis, Goal Seek & Solver — Privacy Policy

Last updated: 3 November 2026

SolveFill is an add-on for Google Sheets™ with Goal Seek, data tables,
scenarios and a solver for linear and integer models. This policy says what it does with data, including the Google user data it receives.

## What Google user data SolveFill accesses

- **The spreadsheet you use it in** (scope `spreadsheets.currentonly`). SolveFill reads the cells you name: the objective or Set cell, the cells to change and the
  constraint cells; a data table and its input cells; and the changing and result cells of
  scenarios. It changes the cells to change to read the model or fill the table, and puts them back.
  It then writes the answer, the table's results or a scenario's values there, which you keep or
  restore. If you ask for them, it adds an Answer Report sheet, a Scenario Summary sheet and a
  sample model sheet. It has no access to your other spreadsheets or files.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: SolveFill looks
  up the Stripe customer with this email and, when you start a checkout, creates one. It is also
  shown in SolveFill so you can check which Google account is used for your free runs and purchase. Google's installation screen may also say the add-on can 'associate you with your
  personal info on Google'. That is Google's standard sign-in association; SolveFill does not
  request, read or store your profile information.
- **Sidebars and menus** (scope `script.container.ui`), to show SolveFill inside Sheets™.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How SolveFill uses that data

- **Your cells** are read inside Google's Apps Script, and models are solved there by Google's
  LinearOptimizationService. Answers are written to your spreadsheet. Your cells are not sent
  anywhere else.
- **The saved models, in the spreadsheet.** The last Goal Seek, solver model and data
  table you ran, and the result cells of your last Scenario Summary
  (their cell references, sheet names, target values and options, but no cell contents) are saved
  in the spreadsheet's own storage for SolveFill, as Excel saves a Solver model in its workbook, so
  the sidebar opens on them. **Everyone who uses SolveFill in that spreadsheet can see them.** To
  remove them, open SolveFill in the spreadsheet and choose **Clear saved models**.
- **Scenarios, in the spreadsheet.** Each scenario you save keeps its name, its cell references and
  the values those cells held when you saved it, in the same storage, as Excel keeps scenarios in
  its workbook. **Everyone who uses SolveFill in that spreadsheet can see them, values included.**
  To remove one, delete it in SolveFill's Scenarios tab. Clear saved models leaves scenarios alone.
- **Original values, in the spreadsheet.** From the moment SolveFill first changes the cells to change, or the
  cells of a data table or scenario, until you keep the answer or restore, their original values are kept in the same storage,
  so they can be put back even if the solve is interrupted. They are deleted when you choose Keep or
  Restore, or when you start the next run that changes cells.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own
  Google account's storage for the add-on.
- **Free allowance records**, in the same account storage, keep how many of your free runs are used. The latest run adds a random identifier, a one-way fingerprint of the spreadsheet and its
  model, table or scenarios, and its status, so that a retry is not counted twice. No cell values, sheet names or
  results are stored in these records.
- **A count of your runs**: once SolveFill is on the Marketplace, your account storage counts the
  runs that worked: solves, data tables and Scenario Summaries, so that after the third it can ask you, once, whether you would review it.
  It is used for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; SolveFill never sees your card. We can see in Stripe your email, your billing country
  and your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

SolveFill uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your email to Stripe.
SolveFill has no servers of its own. The contents of your spreadsheets are never sent to us or to
anyone else. SolveFill uses no analytics service; it counts in its own error log how many accounts
reach each usage step described below.

SolveFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

SolveFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who SolveFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no spreadsheet content.
- **People you share the spreadsheet with** who use SolveFill in it see its saved models, its scenarios with
  their values, and, until
  you keep or restore, the original values of the last answer's cells, as they can see the cells
  themselves.
- Your cells never leave Google's services.

Nothing else is shared, transferred or disclosed: SolveFill does not sell, rent or trade Google
user data, and does not give it to advertisers, data brokers, analytics providers or any other
third party. We would disclose it only if the law required us to, and only what it required.

## How SolveFill protects that data

- **Encryption in transit.** Everything SolveFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your spreadsheet, its saved models, scenarios and original values, SolveFill's
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
- **Usage steps**: each of these steps adds one line to the same error log, naming only SolveFill
  and the step: the sidebar opens, it opens on the Pro offer, Unlock Pro is chosen, a solve, a data
  table or a scenario summary starts, one stops at the free allowance. The line holds no spreadsheet
  content, cell reference, sheet name, email address or file name. Google adds to every line in the
  log its own key for the account, which does not name you, is used only by SolveFill and changes
  every 30 days. We use it only to count how many accounts reach each step, and never link it to
  payments, email addresses or other records.

## Keeping and deleting

- The error log, usage steps included, is deleted after 30 days.
- The saved models stay in the spreadsheet until you choose Clear saved models or the next model
  replaces them; original values, until you keep or restore. Deleting the spreadsheet deletes both.
- Scenarios stay in the spreadsheet until you delete them in SolveFill or delete the spreadsheet.
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
