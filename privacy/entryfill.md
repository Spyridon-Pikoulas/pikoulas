---
layout: page
title: "EntryFill: Data Entry Form & Input Form — Privacy Policy"
permalink: /privacy/entryfill/
---

# EntryFill: Data Entry Form & Input Form — Privacy Policy

Last updated: 26 November 2026

EntryFill is an add-on for Google Sheets™ that makes a data entry form for a table in a spreadsheet,
to add, find, change and delete its records one at a time. This policy says what it does with data,
including the Google user data it receives.

## What Google user data EntryFill accesses

- **The spreadsheet you use it in** (scope `spreadsheets.currentonly`). EntryFill reads the table you
  click in or select: its header row, the values and shown text of its records, the dropdown,
  checkbox and date rules of its columns, the formulas of its last record and, for a dropdown that
  takes its choices from a range, that range's values. It writes into that spreadsheet only when you
  click to, and only into the table:
  - **The values you type into the form**, as if you typed them into the cells: a new record in the
    row under the last one, a changed record only in the fields you changed.
  - **For a new record**, the formats, dropdown and checkbox rules and formulas of the record above
    it, copied onto the new row in the table's columns.
  - **For a deleted record**, the removal of its whole row from the sheet, after you click Delete
    twice. EntryFill first reads the rest of that row, and leaves a row with cells filled outside the
    table for you to delete yourself.

  EntryFill does not read the rest of your spreadsheet, and has no access to your other spreadsheets
  or files.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: EntryFill looks
  up the Stripe customer with this email and, when you start a checkout, creates one. It is also shown
  in EntryFill so you can check which Google account is used for your free saves and purchase.
  Google's installation screen may also say the add-on can 'associate you with your personal info on
  Google'. That is Google's standard sign-in association; EntryFill does not request, read or store
  your profile information.
- **Sidebars and menus** (scope `script.container.ui`), to show EntryFill inside Sheets™.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How EntryFill uses that data

- **Your cells** are read inside Google's Apps Script, to show the form and the record you open, and
  what EntryFill writes stays in your spreadsheet. Nothing from your spreadsheet is stored outside it
  or sent anywhere, apart from the form showing it to you in your browser. EntryFill keeps nothing in
  the spreadsheet beyond your records: no hidden tab, no hidden data and no trigger.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own Google
  account's storage for the add-on, with a mark that the deletion described under StyleFill below has
  been done.
- **Free allowance records**, in the same account storage, keep how many of your free saves are used.
  The latest one adds a random identifier, a one-way fingerprint made from the spreadsheet's ID, the
  tab's ID and a random value, and its status, so that a retry is not counted twice. No spreadsheet
  content is stored in these records.
- **A count of your runs**: once EntryFill is on the Marketplace, your account storage counts your
  saves, so that after a few it can ask you, at most twice, whether you would review it. It is used for
  nothing else.
- **StyleFill and MatchFill**: EntryFill takes the place of StyleFill, and before it MatchFill, on the
  same Google Workspace Marketplace listing. The first time EntryFill opens for your account,
  everything they kept in your account's storage is deleted: your StyleFill styles, their free
  allowance records, their count of your runs and their billing cache. What StyleFill left in your
  documents stays there: the formatting it applied, the named ranges marking where a style was
  applied, and its record of each style's version in the document's own storage, none of which holds
  your text or your styles' names. EntryFill has no access to your documents, so it neither reads nor
  removes them.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; EntryFill never sees your card. We can see in Stripe your email, your billing country and
  your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

EntryFill uses Google user data only for the features above. It does not sell or rent it, does not use
it for advertising, and passes it to no one except as those features need: your email to Stripe.
EntryFill has no servers of its own. The contents of your spreadsheets are never sent to us or to
anyone else. EntryFill uses no analytics service; it counts in its own error log how many accounts
reach each usage step described below.

EntryFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

EntryFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who EntryFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your email
  address, to find your purchase and, when you buy, to create your customer record and take the
  payment. Stripe receives nothing else of your Google user data: no spreadsheet content.
- **People who can open the spreadsheet** see the records you add or change, as they see the rest of
  it.
- Your spreadsheet never leaves Google's services.

Nothing else is shared, transferred or disclosed: EntryFill does not sell, rent or trade Google user
data, and does not give it to advertisers, data brokers, analytics providers or any other third
party. We would disclose it only if the law required us to, and only what it required.

## How EntryFill protects that data

- **Encryption in transit.** Everything EntryFill sends or receives travels over HTTPS (TLS): between
  your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your spreadsheet, EntryFill's settings and its error log are stored by
  Google, which encrypts the data it stores. Your customer record is stored by Stripe, which encrypts
  it too.
- **Access controls.** EntryFill runs inside Google's Apps Script, as you, with only the scopes above
  and only in the spreadsheet you open it in. We have no access to your spreadsheets or to your
  settings. Your customer record sits in our Stripe account, which only we can sign in to. EntryFill
  reaches Stripe with a restricted key that stays on Google's servers and never reaches your browser.
- **Never stored**: the contents of your spreadsheet outside it, your card details, and your Google
  password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error) goes to EntryFill's
  error log in Google Cloud™, which only we can read.
- **Usage steps**: each of these steps adds one line to the same error log, naming only EntryFill and
  the step: the sidebar opens, it opens on the Pro offer, Unlock Pro is chosen, a record is saved, a
  save stops at the free allowance, no table is found at the selection. The line holds no spreadsheet
  content, cell address, email address or file name. Google adds to every line in the log its own key
  for the account, which does not name you, is used only by EntryFill and changes every 30 days. We
  use it only to count how many accounts reach each step, and never link it to payments, email
  addresses or other records.

## Keeping and deleting

- The error log, usage steps included, is deleted after 30 days.
- The records you add or change are yours and stay in your spreadsheet like anything you type there;
  uninstalling EntryFill leaves them as they are. **Edit > Undo** and **File > Version history** bring
  back an earlier state, a deleted row included.
- Free allowance records have no automatic expiry; the next counted save replaces the latest one's
  record without resetting the count used.
- Your settings and free allowance records stay in your Google account's storage for EntryFill and
  contain no spreadsheet content. Uninstalling EntryFill (Extensions > Add-ons > Manage add-ons) stops
  it; removing it at https://myaccount.google.com/connections also ends its access to your account,
  after which nothing reads them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records of
  your payments are kept for five years after the end of the financial year they belong to, as Danish
  bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
