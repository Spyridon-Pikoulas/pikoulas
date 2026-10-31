---
layout: page
title: "CodeFill: Syntax Highlighting for Code — Privacy Policy"
permalink: /privacy/codefill/
---

# CodeFill: Syntax Highlighting for Code — Privacy Policy

Last updated: 26 October 2026

CodeFill is an add-on for Google Docs™ that highlights code: a monospace font, each token in its
color, on a shaded block. This policy says what it does with data, including the Google
user data it receives.

## What Google user data CodeFill accesses

- **The document you use it in** (scope `documents.currentonly`). CodeFill reads the lines of code
  you select, or the CodeFill block your cursor is in, and writes them back there as a highlighted
  block, marked by a named range. A snippet you paste in the sidebar is inserted the same way. It
  has no access to your other documents or files.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: CodeFill
  looks up the Stripe customer with this email and, when you start a checkout, creates one. It is
  also shown in CodeFill so you can check which Google account is used for your free blocks and
  purchase. Google's installation screen may also say the add-on can 'associate you with your
  personal info on Google'. That is Google's standard sign-in association; CodeFill does not
  request, read or store your profile information.
- **Sidebars and menus** (scope `script.container.ui`), to show CodeFill inside Docs™.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How CodeFill uses that data

- **Your code** is highlighted in the sidebar, in your browser, by highlight.js, which is part of
  CodeFill: no request goes out for it. The document is read and changed inside Google's Apps
  Script. Its contents are not stored, and not sent anywhere else.
- **Your settings** (the theme, font and size you last used, your purchase status and your Stripe
  customer number) are kept in your own Google account's storage for the add-on.
- **Free allowance records**, in the same account storage, keep how many of your free blocks are
  spent. The latest new block adds a random identifier, a one-way fingerprint of the document's
  ID, and its status, line count and language, so that a retry is not counted twice. No document
  text is stored in these records.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; CodeFill never sees your card. We can see in Stripe your email, your billing country
  and your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

CodeFill uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your email to
Stripe. CodeFill has no servers of its own. The contents of your documents are never sent to us or
to anyone else, and CodeFill uses no analytics.

CodeFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

CodeFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who CodeFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no document content.
- Your document never leaves Google's services.

Nothing else is shared, transferred or disclosed: CodeFill does not sell, rent or trade Google
user data, and does not give it to advertisers, data brokers, analytics providers or any other
third party. We would disclose it only if the law required us to, and only what it required.

## How CodeFill protects that data

- **Encryption in transit.** Everything CodeFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your document, CodeFill's settings and its error log are stored by
  Google, which encrypts the data it stores. Your customer record is stored by Stripe, which
  encrypts it too.
- **Access controls.** CodeFill runs inside Google's Apps Script, as you, with only the scopes
  above and only in the document you open it in. We have no access to your documents or to your
  settings. Your customer record sits in our Stripe account, which only we can sign in to.
  CodeFill reaches Stripe with a restricted key that stays on Google's servers and never reaches
  your browser.
- **Never stored**: the contents of your document outside it, your card details, and your Google
  password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error) goes to CodeFill's
  error log in Google Cloud™, which only we can read.

## Keeping and deleting

- The error log is deleted after 30 days.
- Free allowance records have no automatic expiry; the next new block replaces the latest one's
  record without resetting the count used.
- Your settings and free allowance records stay in your Google account's storage for CodeFill and
  contain no document text. Uninstalling CodeFill (Extensions > Add-ons > Manage add-ons) stops
  it; removing it at https://myaccount.google.com/connections also ends its access to your
  account, after which nothing reads them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
