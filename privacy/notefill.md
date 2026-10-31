---
layout: page
title: "NoteFill: Endnotes for Google Docs™ — Privacy Policy"
permalink: /privacy/notefill/
---

# NoteFill: Endnotes for Google Docs™ — Privacy Policy

Last updated: 26 October 2026

NoteFill is an add-on for Google Docs™ that adds numbered endnotes to a document, listed at its
end and linked both ways. This policy says what it does with data, including the Google user data
it receives.

## What Google user data NoteFill accesses

- **The document you use it in** (scope `documents.currentonly`). NoteFill reads the document's
  text, to find its endnote references and its list of notes, and moves the cursor to a note or
  reference you click. When you insert, renumber or remove a note, or convert footnotes, it writes
  the reference numbers into the text, writes the notes under a heading at the end of the document
  or tab, and adds a bookmark at each reference and each note for their links. It has no access to
  your other documents or files.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: NoteFill
  looks up the Stripe customer with this email and, when you start a checkout, creates one. It is
  also shown in NoteFill so you can check which Google account is used for your free notes and
  purchase. Google's installation screen may also say the add-on can 'associate you with your
  personal info on Google'. That is Google's standard sign-in association; NoteFill does not
  request, read or store your profile information.
- **Sidebars and menus** (scope `script.container.ui`), to show NoteFill inside Docs™.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How NoteFill uses that data

- **Your document** is read inside Google's Apps Script, and the notes, their numbers and
  bookmarks are written to it. Its contents are not sent anywhere else.
- **In the document**: the reference numbers, the list of notes under its heading (marked with a
  named range), and the bookmarks NoteFill added, which everyone who can edit the document sees as
  Docs shows them. The options (where the notes go, the number style, the heading and the page
  break) are kept in the document's own storage for NoteFill, so a renumber by anyone who uses
  NoteFill in that document writes the same notes. They contain no document text.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own
  Google account's storage for the add-on.
- **Free allowance records**, in the same account storage, keep how many of your free notes are
  spent. The latest insert or conversion adds a random identifier, a one-way fingerprint of the
  document's ID, the options and the note, its status and the number of notes, so that a retry is
  not counted twice. No document text is stored in these records.
- **A count of your runs**: once NoteFill is on the Marketplace, your account storage counts the
  notes written, so that after a few it can ask you, once, whether you would review it. It is
  used for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; NoteFill never sees your card. We can see in Stripe your email, your billing country
  and your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

NoteFill uses Google user data only for the features above. It does not sell or rent it, does
not use it for advertising, and passes it to no one except as those features need: your email to
Stripe. NoteFill has no servers of its own. The contents of your documents are never sent to us
or to anyone else, and NoteFill uses no analytics.

NoteFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

NoteFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who NoteFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no document content.
- **People you share the document with** see the notes and the bookmarks, as they see the rest
  of the document.
- Your document never leaves Google's services.

Nothing else is shared, transferred or disclosed: NoteFill does not sell, rent or trade Google
user data, and does not give it to advertisers, data brokers, analytics providers or any other
third party. We would disclose it only if the law required us to, and only what it required.

## How NoteFill protects that data

- **Encryption in transit.** Everything NoteFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your document, NoteFill's storage in it, its settings and its error
  log are stored by Google, which encrypts the data it stores. Your customer record is stored by
  Stripe, which encrypts it too.
- **Access controls.** NoteFill runs inside Google's Apps Script, as you, with only the scopes
  above and only in the document you open it in. We have no access to your documents or to your
  settings. Your customer record sits in our Stripe account, which only we can sign in to.
  NoteFill reaches Stripe with a restricted key that stays on Google's servers and never
  reaches your browser.
- **Never stored**: the contents of your document outside it, your card details, and your Google
  password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error) goes to
  NoteFill's error log in Google Cloud™, which only we can read.

## Keeping and deleting

- The error log is deleted after 30 days.
- The notes, the bookmarks and NoteFill's storage in the document are part of the document and
  stay until you remove or delete them. Deleting the document deletes them.
- Free allowance records have no automatic expiry; the next insert or conversion replaces the
  latest one's record without resetting the count used.
- Your settings and free allowance records stay in your Google account's storage for NoteFill
  and contain no document text. Uninstalling NoteFill (Extensions > Add-ons > Manage add-ons)
  stops it; removing it at https://myaccount.google.com/connections also ends its access to your
  account, after which nothing reads them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
