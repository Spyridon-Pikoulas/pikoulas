---
layout: page
title: "ListFill: Dependent Dropdown & Drop Down List — Privacy Policy"
permalink: /privacy/listfill/
---

# ListFill: Dependent Dropdown & Drop Down List — Privacy Policy

Last updated: 26 November 2026

ListFill is an add-on for Google Sheets™ that makes dependent dropdowns in a spreadsheet, the choices
in each cell following the choice to its left. This policy says what it does with data, including the
Google user data it receives.

## What Google user data ListFill accesses

- **The spreadsheet you use it in** (scope `spreadsheets.currentonly`). ListFill reads the choices
  table you select (its header row and the values in its columns), to work out how many choices each
  dropdown needs, and the position of the cells you select for the dropdowns. It then writes three
  things into that spreadsheet:
  - **A hidden tab named "ListFill lists"**, with one row of formulas per dropdown cell. Each row
    lists that cell's choices, taken from your choices table and from the choice to its left. Its
    first cell says what the tab is for, and it is protected with a warning, so anyone about to edit
    it is asked first. It holds nothing that is not already in your spreadsheet. Anyone who can edit
    the spreadsheet can show it, as with any hidden tab. When you remove the last ListFill dropdowns,
    the tab is deleted.
  - **Dropdown rules** (Google Sheets™' data validation) on the cells you selected, each pointing to
    its row on that tab.
  - **Emptied cells**, only if you turn on clearing (Pro): when a choice changes, the cells to its
    right on that row, in the same dropdowns, are emptied.

  ListFill does not read the rest of your spreadsheet, and has no access to your other spreadsheets
  or files.
- **A trigger in that spreadsheet** (scope `script.scriptapp`), only while dropdowns with clearing are
  in it: an edit trigger that runs as you whenever anyone edits the spreadsheet. It reads which cells
  were edited, never their values, and empties the cells described above when the edit is in
  ListFill's dropdowns. It is deleted when the last dropdowns with clearing are removed.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: ListFill looks up
  the Stripe customer with this email and, when you start a checkout, creates one. It is also shown in
  ListFill so you can check which Google account is used for your free setups and purchase. Google's
  installation screen may also say the add-on can 'associate you with your personal info on Google'.
  That is Google's standard sign-in association; ListFill does not request, read or store your profile
  information.
- **Sidebars and menus** (scope `script.container.ui`), to show ListFill inside Sheets™.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How ListFill uses that data

- **Your cells** are read inside Google's Apps Script, and what ListFill writes stays in your
  spreadsheet. Nothing from your spreadsheet is sent anywhere or stored outside it.
- **Your dropdowns**: the list of ListFill dropdowns in a spreadsheet (the tabs' ids, the cells'
  addresses, the levels and whether they clear) is kept in that spreadsheet as hidden data
  (developer metadata), so that ListFill can list, refresh and remove them for anyone who opens it
  there, and in copies of the spreadsheet too. It holds no cell values.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own Google
  account's storage for the add-on, with a mark that the deletion described under TranslateFill below
  has been done.
- **Free allowance records**, in the same account storage, keep how many of your free setups are used.
  The latest one adds a random identifier, a one-way fingerprint made from the spreadsheet's ID and a
  random value, its status and the number of rows it gave dropdowns, so that a retry is not counted twice. No
  spreadsheet content is stored in these records.
- **A count of your runs**: once ListFill is on the Marketplace, your account storage counts the
  dropdowns you add, so that after a few it can ask you, at most twice, whether you would review it. It is used
  for nothing else.
- **TranslateFill and MathFill**: ListFill takes the place of TranslateFill, and before it MathFill,
  on the same Google Workspace Marketplace listing. The first time ListFill opens for your account,
  everything they kept in your account's storage is deleted: the words you asked TranslateFill to
  keep as they are, their free allowance records, their count of your runs and their billing cache.
  ListFill does not use the access to a form you may have given TranslateFill in Google's file
  picker; it ends when you remove the add-on at https://myaccount.google.com/connections.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; ListFill never sees your card. We can see in Stripe your email, your billing country and
  your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

ListFill uses Google user data only for the features above. It does not sell or rent it, does not use
it for advertising, and passes it to no one except as those features need: your email to Stripe.
ListFill has no servers of its own. The contents of your spreadsheets are never sent to us or to
anyone else. ListFill uses no analytics service; it counts in its own error log how many accounts
reach each usage step described below.

ListFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

ListFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who ListFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your email
  address, to find your purchase and, when you buy, to create your customer record and take the
  payment. Stripe receives nothing else of your Google user data: no spreadsheet content.
- **People who can open the spreadsheet** see the dropdowns and, if they edit it, can show the
  "ListFill lists" tab, as with the rest of the spreadsheet.
- Your spreadsheet never leaves Google's services.

Nothing else is shared, transferred or disclosed: ListFill does not sell, rent or trade Google user
data, and does not give it to advertisers, data brokers, analytics providers or any other third
party. We would disclose it only if the law required us to, and only what it required.

## How ListFill protects that data

- **Encryption in transit.** Everything ListFill sends or receives travels over HTTPS (TLS): between
  your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your spreadsheet, ListFill's settings and its error log are stored by
  Google, which encrypts the data it stores. Your customer record is stored by Stripe, which encrypts
  it too.
- **Access controls.** ListFill runs inside Google's Apps Script, as you, with only the scopes above
  and only in the spreadsheet you open it in. We have no access to your spreadsheets or to your
  settings. Your customer record sits in our Stripe account, which only we can sign in to. ListFill
  reaches Stripe with a restricted key that stays on Google's servers and never reaches your browser.
- **Never stored**: the contents of your spreadsheet outside it, your card details, and your Google
  password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error) goes to ListFill's
  error log in Google Cloud™, which only we can read.
- **Usage steps**: each of these steps adds one line to the same error log, naming only ListFill and
  the step: the sidebar opens, it opens on the Pro offer, Unlock Pro is chosen, dropdowns are added,
  a setup stops at the free allowance, a choices table is refused for having no rows under its
  header. The line holds no spreadsheet content, cell address, email address or file name. Google adds
  to every line in the log its own key for the account, which does not name you, is used only by
  ListFill and changes every 30 days. We use it only to count how many accounts reach each step, and
  never link it to payments, email addresses or other records.

## Keeping and deleting

- The error log, usage steps included, is deleted after 30 days.
- The "ListFill lists" tab, the dropdown rules and the list of dropdowns stay in your spreadsheet,
  and in its copies, until you remove the dropdowns in ListFill or delete the spreadsheet. Uninstalling ListFill leaves
  them, and the dropdowns keep working; you can also delete the tab and the rules yourself, as any
  other. Values chosen in the dropdowns are yours, and stay when dropdowns are removed.
- Free allowance records have no automatic expiry; the next counted setup replaces the latest one's
  record without resetting the count used.
- Your settings and free allowance records stay in your Google account's storage for ListFill and
  contain no spreadsheet content. Uninstalling ListFill (Extensions > Add-ons > Manage add-ons) stops
  it; removing it at https://myaccount.google.com/connections also ends its access to your account
  and stops its edit triggers, after which nothing reads them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records of
  your payments are kept for five years after the end of the financial year they belong to, as Danish
  bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
