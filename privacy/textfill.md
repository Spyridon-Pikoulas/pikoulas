---
layout: page
title: "TextFill: Pasted Text Cleaner, Remove Line Breaks — Privacy Policy"
permalink: /privacy/textfill/
---

# TextFill: Pasted Text Cleaner, Remove Line Breaks — Privacy Policy

Last updated: 30 October 2026

TextFill is an add-on for Google Docs™ that finds and replaces, cleans pasted text, changes its
case and sorts paragraphs, lists and table rows. This policy says what it does with data, including the Google
user data it receives.

## What Google user data TextFill accesses

- **The document you use it in** (scope `documents.currentonly`). TextFill reads the text you
  select or, with nothing selected, the tab you are in, and rewrites it there when you find and
  replace in it, clean it, change its case or sort it. It has no access to your other documents or files.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: TextFill
  looks up the Stripe customer with this email and, when you start a checkout, creates one. It is
  also shown in TextFill so you can check which Google account is used for your free runs and
  purchase. Google's installation screen may also say the add-on can 'associate you with your
  personal info on Google'. That is Google's standard sign-in association; TextFill does not
  request, read or store your profile information.
- **Sidebars and menus** (scope `script.container.ui`), to show TextFill inside Docs™.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How TextFill uses that data

- **Your document** is read inside Google's Apps Script and changed there. Its contents are not
  stored, and not sent anywhere else.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own
  Google account's storage for the add-on.
- **Free allowance records**, in the same account storage, keep how many of your free runs are
  spent. The latest counted run adds a random identifier, a one-way fingerprint of the document's
  ID and the kind of run, and its status and counts (how many paragraphs, items, rows or
  replacements), so that
  a retry is not counted twice. No document text is stored in these records.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; TextFill never sees your card. We can see in Stripe your email, your billing country
  and your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

TextFill uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your email to
Stripe. TextFill has no servers of its own. The contents of your documents are never sent to us or
to anyone else, and TextFill uses no analytics.

TextFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

TextFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who TextFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no document content.
- Your document never leaves Google's services.

Nothing else is shared, transferred or disclosed: TextFill does not sell, rent or trade Google
user data, and does not give it to advertisers, data brokers, analytics providers or any other
third party. We would disclose it only if the law required us to, and only what it required.

## How TextFill protects that data

- **Encryption in transit.** Everything TextFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your document, TextFill's settings and its error log are stored by
  Google, which encrypts the data it stores. Your customer record is stored by Stripe, which
  encrypts it too.
- **Access controls.** TextFill runs inside Google's Apps Script, as you, with only the scopes
  above and only in the document you open it in. We have no access to your documents or to your
  settings. Your customer record sits in our Stripe account, which only we can sign in to.
  TextFill reaches Stripe with a restricted key that stays on Google's servers and never reaches
  your browser.
- **Never stored**: the contents of your document outside it, your card details, and your Google
  password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error) goes to TextFill's
  error log in Google Cloud™, which only we can read.

## Keeping and deleting

- The error log is deleted after 30 days.
- Free allowance records have no automatic expiry; the next counted run replaces the latest
  one's record without resetting the count used.
- Your settings and free allowance records stay in your Google account's storage for TextFill and
  contain no document text. Uninstalling TextFill (Extensions > Add-ons > Manage add-ons) stops
  it; removing it at https://myaccount.google.com/connections also ends its access to your
  account, after which nothing reads them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
