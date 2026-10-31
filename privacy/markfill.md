---
layout: page
title: "MarkFill: Highlight Words & Phrases — Privacy Policy"
permalink: /privacy/markfill/
---

# MarkFill: Highlight Words & Phrases — Privacy Policy

Last updated: 27 October 2026

MarkFill is an add-on for Google Docs™ that highlights the words on your lists in a document. This
policy says what it does with data, including the Google user data it receives.

## What Google user data MarkFill accesses

- **The document you use it in** (scope `documents.currentonly`). MarkFill reads the document's
  text (body, tables, headers, footers and footnotes, in every tab or the one you choose) to find
  the words on your lists, and reads its highlight colours so that your own highlights are left
  alone. When you highlight, it sets a highlight colour on each match and removes its own
  highlight colours from the last run; Clear removes only its own colours. It never changes the
  text. When you add the sample in an empty tab, it writes a few paragraphs there. It has no
  access to your other documents or files.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: MarkFill
  looks up the Stripe customer with this email and, when you start a checkout, creates one. It is
  also shown in MarkFill so you can check which Google account is used for your free runs and
  purchase. Google's installation screen may also say the add-on can 'associate you with your
  personal info on Google'. That is Google's standard sign-in association; MarkFill does not
  request, read or store your profile information.
- **Sidebars and menus** (scope `script.container.ui`), to show MarkFill inside Docs™.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How MarkFill uses that data

- **Your document** is read inside Google's Apps Script, and the highlight colours are written to
  it. Its contents are not sent anywhere else and not stored outside it.
- **In the document**: the highlight colours MarkFill set, which everyone who can open the
  document sees, until you clear them.
- **Your word lists and options** (the lists' names, colours and words, whether each is on, and
  the matching options) are kept in your own Google account's storage for the add-on, so every
  document you open MarkFill in uses them. They hold what you typed or pasted into the lists, not
  document text.
- **Your settings** (your purchase status and your Stripe customer number) are kept in the same
  account storage.
- **Free allowance records**, in the same account storage, keep how many of your free runs are
  spent. The latest run adds a random identifier, a one-way fingerprint of the document's ID, the
  lists and the options, its status and the number of matches, so that a retry is not counted
  twice. No document text is stored in these records.
- **A count of your runs**: once MarkFill is on the Marketplace, your account storage counts your
  runs, so that after a few it can ask you, once, whether you would review it. It is used for
  nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; MarkFill never sees your card. We can see in Stripe your email, your billing country
  and your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

MarkFill uses Google user data only for the features above. It does not sell or rent it, does
not use it for advertising, and passes it to no one except as those features need: your email to
Stripe. MarkFill has no servers of its own. The contents of your documents and your word lists are
never sent to us or to anyone else, and MarkFill uses no analytics.

MarkFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

MarkFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who MarkFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no document content and no
  word lists.
- **People you share the document with** see the highlights, as they see the rest of the
  document.
- Your document never leaves Google's services.

Nothing else is shared, transferred or disclosed: MarkFill does not sell, rent or trade Google
user data, and does not give it to advertisers, data brokers, analytics providers or any other
third party. We would disclose it only if the law required us to, and only what it required.

## How MarkFill protects that data

- **Encryption in transit.** Everything MarkFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your document, your word lists, MarkFill's settings and its error log
  are stored by Google, which encrypts the data it stores. Your customer record is stored by
  Stripe, which encrypts it too.
- **Access controls.** MarkFill runs inside Google's Apps Script, as you, with only the scopes
  above and only in the document you open it in. We have no access to your documents, your word
  lists or your settings. Your customer record sits in our Stripe account, which only we can sign
  in to. MarkFill reaches Stripe with a restricted key that stays on Google's servers and never
  reaches your browser.
- **Never stored**: the contents of your document outside it, your card details, and your Google
  password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error) goes to
  MarkFill's error log in Google Cloud™, which only we can read.

## Keeping and deleting

- The error log is deleted after 30 days.
- The highlights are part of the document and stay until you clear them or delete the document.
- Your word lists stay until you change or remove them in the sidebar.
- Free allowance records have no automatic expiry; the next run replaces the latest one's record
  without resetting the count used.
- Your word lists, settings and free allowance records stay in your Google account's storage for
  MarkFill and contain no document text. Uninstalling MarkFill (Extensions > Add-ons > Manage
  add-ons) stops it; removing it at https://myaccount.google.com/connections also ends its access
  to your account, after which nothing reads them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
