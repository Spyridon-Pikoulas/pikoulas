---
layout: page
title: "AmountFill: Spell Number, Money to Words & Rupees — Privacy Policy"
permalink: /privacy/amountfill/
---

# AmountFill: Spell Number, Money to Words & Rupees — Privacy Policy

Last updated: 10 November 2026

AmountFill is an add-on for Google Sheets™ that spells the amounts in your spreadsheet in words. This
policy says what it does with data, including the Google user data it receives.

## What Google user data AmountFill accesses

- **The spreadsheet you use it in** (scope `spreadsheets.currentonly`). AmountFill reads the cells you
  select and the cells its formulas are given, the cells to the right of a selection to find an empty
  column, and the spreadsheet's locale, to choose a currency and a way of counting. It finds its own
  formulas and the cells showing its Pro line. When you spell a column it writes one formula, or the
  words as text, in that column; it rewrites its own formulas to recalculate them once a purchase is
  confirmed; and it adds a sample tab if you ask for one. It has no access to your other spreadsheets
  or files.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: AmountFill looks
  up the Stripe customer with this email and, when you start a checkout, creates one. It is also shown
  in AmountFill so you can check which Google account is used for your purchase. Google's installation
  screen may also say the add-on can 'associate you with your personal info on Google'. That is
  Google's standard sign-in association; AmountFill does not request, read or store your profile
  information.
- **Sidebars and menus** (scope `script.container.ui`), to show AmountFill inside Sheets.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How AmountFill uses that data

- **Your amounts** are read inside Google's Apps Script, and the words are made there and written to
  your spreadsheet. They are not stored elsewhere or sent anywhere.
- **In the spreadsheet**: the formulas or words AmountFill wrote, a sample tab if you asked for one,
  and, in the spreadsheet's own storage for AmountFill, once a purchase has been checked in it, a date
  30 days on. Until that date its formulas spell amounts over 999 for anyone who can open the
  spreadsheet. The date contains no email or cell contents. It does not say who bought AmountFill.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own Google
  account's storage for the add-on, with a mark that the deletion described under PrintFill below has
  been done.
- **A count of your runs**: once AmountFill is on the Marketplace, your account storage counts the
  columns spelled, so that after a few it can ask you, once, whether you would review it. It is used
  for nothing else.
- **PrintFill**: AmountFill takes the place of PrintFill on the same Google Workspace Marketplace
  listing. Until the end of 22 December 2026, PrintFill's QR codes, barcodes and labels stay in
  AmountFill's menu, and what they use and keep is as [PrintFill's privacy policy](/privacy/printfill/)
  says. The first time AmountFill opens for your account after 22 December 2026, everything PrintFill
  kept in your account's storage is deleted: its free-code counts and the records of your latest labels
  and codes in cells, its count of your runs and its billing cache.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; AmountFill never sees your card. We can see in Stripe your email, your billing country and
  your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

AmountFill uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your email to Stripe.
AmountFill has no servers of its own. The contents of your spreadsheets are never sent to us or to
anyone else. AmountFill uses no analytics service; it counts in its own error log how many accounts
reach each usage step described below.

AmountFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

AmountFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who AmountFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your email
  address, to find your purchase and, when you buy, to create your customer record and take the
  payment. Stripe receives nothing else of your Google user data: no amounts and no words.
- **People you share the spreadsheet with** see the formulas and words, as they see the rest of it.
- Your spreadsheet never leaves Google's services.

Nothing else is shared, transferred or disclosed: AmountFill does not sell, rent or trade Google user
data, and does not give it to advertisers, data brokers, analytics providers or any other third
party. We would disclose it only if the law required us to, and only what it required.

## How AmountFill protects that data

- **Encryption in transit.** Everything AmountFill sends or receives travels over HTTPS (TLS): between
  your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your spreadsheet, AmountFill's storage in it, its settings and its error log
  are stored by Google, which encrypts the data it stores. Your customer record is stored by Stripe,
  which encrypts it too.
- **Access controls.** AmountFill runs inside Google's Apps Script, with only the scopes above and only
  in the spreadsheet you open it in. We have no access to your spreadsheets or your settings. Your
  customer record sits in our Stripe account, which only we can sign in to. AmountFill reaches Stripe
  with a restricted key that stays on Google's servers and never reaches your browser.
- **Never stored**: your amounts, anywhere outside your spreadsheet; your card details; and your Google
  password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error) goes to AmountFill's
  error log in Google Cloud™, which only we can read.
- **Usage steps**: each of these steps adds one line to the same error log, naming only AmountFill and
  the step: the sidebar opens, it opens on the Pro offer, Unlock Pro is chosen, a column is spelled, a
  column stops at the free size, a formula shows the Pro line. The line holds no spreadsheet content,
  amount, email address or file name. Google adds to every line in the log its own key for the
  account, which does not name you, is used only by AmountFill and changes every 30 days. We use it
  only to count how many accounts reach each step, and never link it to payments, email addresses or
  other records.

## Keeping and deleting

- The error log, usage steps included, is deleted after 30 days.
- The formulas, words and sample tab are part of the spreadsheet and stay until you change or delete
  them. So does the date in its storage, which does nothing once it has passed. Deleting the
  spreadsheet deletes them.
- Your settings contain no spreadsheet content. Uninstalling AmountFill (Extensions > Add-ons > Manage
  add-ons) stops it; removing it at https://myaccount.google.com/connections also ends its access to
  your account, after which nothing reads them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records of
  your payments are kept for five years after the end of the financial year they belong to, as Danish
  bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
