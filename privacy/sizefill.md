---
layout: page
title: "SizeFill: Resize All Images & Image Size — Privacy Policy"
permalink: /privacy/sizefill/
---

# SizeFill: Resize All Images & Image Size — Privacy Policy

Last updated: 11 November 2026

SizeFill is an add-on for Google Docs™ that sets the size of the images in a document: the one you
select, or every image at once. This policy says what it does with data, including the Google user
data it receives.

## What Google user data SizeFill accesses

- **The document you use it in** (scope `documents.currentonly`). SizeFill finds the images you
  select, or every image in the document's tabs, and reads their width and height and the page's width
  and margins. When you click Resize, it sets those images' width and height. It does not read or
  change the document's text, and has no access to your other documents or files.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: SizeFill looks up
  the Stripe customer with this email and, when you start a checkout, creates one. It is also shown in
  SizeFill so you can check which Google account is used for your free runs and purchase. Google's
  installation screen may also say the add-on can 'associate you with your personal info on Google'.
  That is Google's standard sign-in association; SizeFill does not request, read or store your profile
  information.
- **Sidebars and menus** (scope `script.container.ui`), to show SizeFill inside Docs™.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How SizeFill uses that data

- **Your images** are resized inside Google's Apps Script. Only their displayed size changes; the
  pictures themselves are not read, copied, stored or sent anywhere.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own Google
  account's storage for the add-on, with a mark that the deletion described under PacketFill below has
  been done.
- **Free allowance records**, in the same account storage, keep how many of your free runs for
  several images at once are spent. The latest one adds a random identifier, a one-way fingerprint
  made from the document's ID and a random value, its status and its number of images resized, so that
  a retry is not counted twice. No document content is stored in these records.
- **A count of your runs**: once SizeFill is on the Marketplace, your account storage counts your
  resizes, so that after a few it can ask you, once, whether you would review it. It is used for
  nothing else.
- **PacketFill**: SizeFill takes the place of PacketFill on the same Google Workspace Marketplace
  listing. The first time SizeFill opens for your account, everything PacketFill kept in your
  account's storage is deleted: its free allowance and generation records, the list of temporary
  copies it was about to delete, its count of your runs and its billing cache.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; SizeFill never sees your card. We can see in Stripe your email, your billing country and
  your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

SizeFill uses Google user data only for the features above. It does not sell or rent it, does not use
it for advertising, and passes it to no one except as those features need: your email to Stripe.
SizeFill has no servers of its own. The contents of your documents are never sent to us or to anyone
else. SizeFill uses no analytics service; it counts in its own error log how many accounts reach each
usage step described below.

SizeFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

SizeFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who SizeFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your email
  address, to find your purchase and, when you buy, to create your customer record and take the
  payment. Stripe receives nothing else of your Google user data: no document content.
- Your document never leaves Google's services.

Nothing else is shared, transferred or disclosed: SizeFill does not sell, rent or trade Google user
data, and does not give it to advertisers, data brokers, analytics providers or any other third
party. We would disclose it only if the law required us to, and only what it required.

## How SizeFill protects that data

- **Encryption in transit.** Everything SizeFill sends or receives travels over HTTPS (TLS): between
  your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your document, SizeFill's settings and its error log are stored by Google,
  which encrypts the data it stores. Your customer record is stored by Stripe, which encrypts it too.
- **Access controls.** SizeFill runs inside Google's Apps Script, as you, with only the scopes above
  and only in the document you open it in. We have no access to your documents or to your settings.
  Your customer record sits in our Stripe account, which only we can sign in to. SizeFill reaches
  Stripe with a restricted key that stays on Google's servers and never reaches your browser.
- **Never stored**: the contents of your document outside it, your card details, and your Google
  password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error) goes to SizeFill's
  error log in Google Cloud™, which only we can read.
- **Usage steps**: each of these steps adds one line to the same error log, naming only SizeFill and
  the step: the sidebar opens, it opens on the Pro offer, Unlock Pro is chosen, images are resized, a
  resize stops at the free allowance. The line holds no document content, size, email address or file
  name. Google adds to every line in the log its own key for the account, which does not name you, is
  used only by SizeFill and changes every 30 days. We use it only to count how many accounts reach
  each step, and never link it to payments, email addresses or other records.

## Keeping and deleting

- The error log, usage steps included, is deleted after 30 days.
- The sizes SizeFill set are part of the document and stay until you change them or delete the
  document.
- Free allowance records have no automatic expiry; the next counted run replaces the latest one's
  record without resetting the count used.
- Your settings and free allowance records stay in your Google account's storage for SizeFill and
  contain no document content. Uninstalling SizeFill (Extensions > Add-ons > Manage add-ons) stops it;
  removing it at https://myaccount.google.com/connections also ends its access to your account, after
  which nothing reads them.
- What PacketFill made in your Google Drive™ (PDFs, folders and sample templates, and any "PacketFill
  temporary copy" an interrupted run left) stays there until you delete it: SizeFill has no access to
  Drive.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records of
  your payments are kept for five years after the end of the financial year they belong to, as Danish
  bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
