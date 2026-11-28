---
layout: page
title: "IconFill: Insert Icons in Slides™, Docs™, Sheets™ — Privacy Policy"
permalink: /privacy/iconfill/
---

# IconFill: Insert Icons in Slides™, Docs™, Sheets™ — Privacy Policy

Last updated: 27 November 2026

IconFill is an add-on for Google Slides™, Google Docs™ and Google Sheets™ that inserts icons into
the file you open it in. This policy says what it does with data, including the Google user data
it receives.

## What Google user data IconFill accesses

- **The file you use it in** (scopes `presentations.currentonly`, `documents.currentonly` and
  `spreadsheets.currentonly`, one for each editor). IconFill reads only where the icon should go:
  the current slide and the page's size, the cursor in a document, or the selected cell in a
  spreadsheet, the value and formula there, only to see whether it is empty, and, when you choose
  Match the text, the font size there, in a document the paragraph's style too. It then inserts
  the icon there as an image, its name as alt text. It does not read the text or images already in
  your file, or any other cell's value, never changes a cell that has content, and has no access
  to your other files.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: IconFill looks
  up the Stripe customer with this email and, when you start a checkout, creates one. It is also
  shown in IconFill so you can check which Google account is used for your purchase. Google's
  installation screen may also say the add-on can 'associate you with your personal info on Google'.
  That is Google's standard sign-in association; IconFill does not request, read or store your
  profile information.
- **Sidebars, dialogs and menus** (scope `script.container.ui`), to show IconFill inside the
  editors.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How IconFill uses that data

- **Your searches**, and the list you write for icons, run inside the sidebar in your browser,
  against a list of icon names and tags that comes with IconFill. They are not sent to us or to
  anyone else.
- **Icon images** are loaded by the sidebar from jsDelivr (`cdn.jsdelivr.net`), a public network
  that serves the open-source icon files. Like any website your browser visits, it receives the
  address of each icon file shown and your browser's standard request details, such as your IP
  address; it receives no Google user data and nothing from your files. jsDelivr's
  [Privacy Policy](https://www.jsdelivr.com/terms/privacy-policy-jsdelivr-net) applies.
- **The icon you insert** is drawn, on its shape when you choose one, in your color and size in your
  browser and passed to Google's Apps Script, which places it in your file. It is not stored
  anywhere else.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own
  Google account's storage for the add-on.
- **The free-insert record is gone.** Until 27 November 2026, IconFill kept a count of your free
  inserts and the latest insert's identifier, one-way fingerprint and status in the same storage.
  From 27 November 2026 it deletes them the next time it opens, and counts no free inserts.
- **A count of your runs**: once IconFill is on the Marketplace, the same storage counts the
  inserts that worked, so that after the third it can ask you, at most twice, whether you would review it. It is used
  for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; IconFill never sees your card. We can see in Stripe your email, your billing country and
  your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

IconFill uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your email to
Stripe. IconFill has no servers of its own. The contents of your files are never sent to us or to anyone else. IconFill uses no analytics
service; it counts in its own error log how many accounts reach each usage step described below.

IconFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

IconFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who IconFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no file content.
- Your files are sent to no service but Google's.

Nothing else is shared, transferred or disclosed: IconFill does not sell, rent or trade Google user
data, and does not give it to advertisers, data brokers, analytics providers or any other third
party. We would disclose it only if the law required us to, and only what it required.

## How IconFill protects that data

- **Encryption in transit.** Everything IconFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, between your browser and jsDelivr, and from Apps Script to
  Stripe.
- **Encryption at rest.** Your files, IconFill's settings and its error log are stored by Google,
  which encrypts the data it stores. Your customer record is stored by Stripe, which encrypts it
  too.
- **Access controls.** IconFill runs inside Google's Apps Script, as you, with only the scopes above
  and only in the file you open it in. We have no access to your files or to your settings. Your
  customer record sits in our Stripe account, which only we can sign in to. IconFill reaches Stripe
  with a restricted key that stays on Google's servers and never reaches your browser.
- **Never stored**: the contents of your files outside them, your card details, and your Google
  password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error, or the editor
  refusing an image) goes to IconFill's error log in Google Cloud™, which only we can read.
- **Usage steps**: each of these steps adds one line to the same error log, naming only IconFill and
  the step: the sidebar opens, Unlock Pro is chosen, an icon is inserted, an insert stops at Pro.
  The line holds no file content, icon, email address or file name. Google adds to every line in the
  log its own key for the account, which does not name you, is used only by IconFill and changes
  every 30 days. We use it only to count how many accounts reach each step, and never link it to
  payments, email addresses or other records.

## Keeping and deleting

- The error log, usage steps included, is deleted after 30 days.
- Your settings stay in your Google account's storage for IconFill and contain no file contents.
  Uninstalling IconFill (Extensions > Add-ons > Manage add-ons) stops it; removing it at
  https://myaccount.google.com/connections also ends its access to your account, after which nothing
  reads them. The icons IconFill inserted stay in your files until you delete them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
