---
layout: page
title: "ScoreFill: Music Notation & Sheet Music — Privacy Policy"
permalink: /privacy/scorefill/
---

# ScoreFill: Music Notation & Sheet Music — Privacy Policy

Last updated: 10 November 2026

ScoreFill is an add-on for Google Docs™ and Google Slides™ that writes music on a staff and puts it in
your file as a picture. This policy says what it does with data, including the Google user data it
receives.

## What Google user data ScoreFill accesses

- **The document or presentation you use it in** (scopes `documents.currentonly` and
  `presentations.currentonly`). ScoreFill reads what is selected, to see whether it is one of its own
  pictures, and that picture's alt text, to open its notes again; in a document, the cursor, the page's
  size and margins; in a presentation, the current slide and the slide's size. When you insert, it puts
  the picture in and sets its alt text; with one of its pictures selected, it removes that picture after
  the new one is in. It has no access to your other files, and it reads no other text or pictures in this
  one.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: ScoreFill looks up
  the Stripe customer with this email and, when you start a checkout, creates one. It is also shown in
  ScoreFill so you can check which Google account is used for your free uses and purchase. Google's
  installation screen may also say the add-on can 'associate you with your personal info on Google'.
  That is Google's standard sign-in association; ScoreFill does not request, read or store your profile
  information.
- **Dialogs and menus** (scope `script.container.ui`), to show ScoreFill inside Docs and Slides.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How ScoreFill uses that data

- **Your music** is drawn in your browser, by code that comes with ScoreFill. The picture and the notes
  go to Google's Apps Script, which puts them in your file. They are not sent anywhere else.
- **In the file**: the picture and its alt text, which describes the music in words and holds its notes,
  so that ScoreFill can open it again. Everyone who can open the file can see them, as they see the rest
  of it. ScoreFill keeps nothing in the file's own add-on storage.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own Google
  account's storage for the add-on.
- **Free allowance records**, in the same account storage, keep how many of your free uses are spent. The
  latest insert adds a random identifier, a one-way fingerprint of the music and its status, so that a
  run that fails is not counted. No music is stored in these records.
- **A count of your runs**: once ScoreFill is on the Marketplace, your account storage counts the
  snippets inserted or changed, so that after the third it can ask you, once, whether you would review it. It
  is used for nothing else.
- **ContentsFill**: ScoreFill takes the place of ContentsFill on the same Google Workspace Marketplace
  listing. The first time ScoreFill opens for your account, everything ContentsFill kept in your account's
  storage is deleted: its count of free uses and the records behind it, its count of your runs and its
  billing cache. What ContentsFill kept in a document's own storage, the table's options and the
  bookmarks' IDs, stays with the document, and ScoreFill neither reads nor deletes it. ContentsFill's
  tables and bookmarks are part of your documents, and ScoreFill leaves them alone.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing address;
  ScoreFill never sees your card. We can see in Stripe your email, your billing country and your
  purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

ScoreFill uses Google user data only for the features above. It does not sell or rent it, does not use it
for advertising, and passes it to no one except as those features need: your email to Stripe. ScoreFill
has no servers of its own. The contents of your files are never sent to us or to anyone else. ScoreFill
uses no analytics service; it counts in its own error log how many accounts reach each usage step
described below.

ScoreFill does not use Google user data, including data received from Google Workspace™ APIs, to develop,
improve or train AI or machine-learning models, generalized or personalized.

ScoreFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who ScoreFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your email
  address, to find your purchase and, when you buy, to create your customer record and take the payment.
  Stripe receives nothing else of your Google user data: no file contents and no music.
- **People you share the file with** see the picture and its alt text, as they see the rest of it.
- Your file never leaves Google's services.

Nothing else is shared, transferred or disclosed: ScoreFill does not sell, rent or trade Google user data,
and does not give it to advertisers, data brokers, analytics providers or any other third party. We would
disclose it only if the law required us to, and only what it required.

## How ScoreFill protects that data

- **Encryption in transit.** Everything ScoreFill sends or receives travels over HTTPS (TLS): between your
  browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your file, ScoreFill's settings and its error log are stored by Google, which
  encrypts the data it stores. Your customer record is stored by Stripe, which encrypts it too.
- **Access controls.** ScoreFill runs inside Google's Apps Script, as you, with only the scopes above and
  only in the file you open it in. We have no access to your files or to your settings. Your customer
  record sits in our Stripe account, which only we can sign in to. ScoreFill reaches Stripe with a
  restricted key that stays on Google's servers and never reaches your browser.
- **Never stored**: your music outside your file, your card details, and your Google password or sign-in
  tokens.
- **Errors**: when something fails, its error message (such as a Stripe error) goes to ScoreFill's error
  log in Google Cloud™, which only we can read.
- **Usage steps**: each of these steps adds one line to the same error log, naming only ScoreFill and the
  step: the dialog opens, it opens on the Pro offer, Unlock Pro is chosen, a snippet is inserted or
  changed, one stops at the free allowance. The line holds no file content, music, email address or file
  name. Google adds to every line in the log its own key for the account, which does not name you, is used
  only by ScoreFill and changes every 30 days. We use it only to count how many accounts reach each step,
  and never link it to payments, email addresses or other records.

## Keeping and deleting

- The error log, usage steps included, is deleted after 30 days.
- The picture and its alt text are part of the file and stay until you delete them. Deleting the file
  deletes them.
- What ContentsFill kept in a document's storage stays until the document is deleted. It contains no
  document text, and nothing reads it.
- Free allowance records have no automatic expiry; the next new snippet replaces the latest one's record
  without resetting the count used.
- Your settings and free allowance records stay in your Google account's storage for ScoreFill and contain
  no music or file content. Uninstalling ScoreFill (Extensions > Add-ons > Manage add-ons) stops it;
  removing it at https://myaccount.google.com/connections also ends its access to your account, after
  which nothing reads them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records of your
  payments are kept for five years after the end of the financial year they belong to, as Danish
  bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
