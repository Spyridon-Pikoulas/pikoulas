---
layout: page
title: "MathFill: Equation Editor for Slides™ & Docs™ — Privacy Policy"
permalink: /privacy/mathfill/
---

# MathFill: Equation Editor for Slides™ & Docs™ — Privacy Policy

Last updated: 26 October 2026

MathFill is an add-on for Google Slides™ and Google Docs™ that inserts equations into the file you
open it in, and edits the ones it inserted. This policy says what it does with data, including the
Google user data it receives.

## What Google user data MathFill accesses

- **The file you use it in** (scopes `presentations.currentonly` and `documents.currentonly`, one
  for each editor). MathFill reads only your selection: the current slide and the box selected on
  it, or the cursor in a document, to know where a new equation goes; and, when one image is
  selected, that image's alt text, to tell whether it is an equation MathFill inserted and, if so,
  to read the equation back for editing. It then inserts the equation there as an image, or
  replaces the equation you edit, and writes the equation's source (its LaTeX), size and color into
  that image's alt text, where they stay in your file. Anyone who can open the file can read them,
  as with any alt text, including in copies of it. It does not read the text or other images in
  your file and has no access to your other files.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: MathFill looks
  up the Stripe customer with this email and, when you start a checkout, creates one. It is also
  shown in MathFill so you can check which Google account is used for your free equations and
  purchase. Google's installation screen may also say the add-on can 'associate you with your
  personal info on Google'. That is Google's standard sign-in association; MathFill does not
  request, read or store your profile information.
- **Sidebars, dialogs and menus** (scope `script.container.ui`), to show MathFill inside the
  editors.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How MathFill uses that data

- **Your equations** are written and drawn inside the sidebar in your browser. They are not sent to
  us or to anyone else.
- **The editor and drawing libraries** (MathLive, MathJax and their fonts) are loaded by the
  sidebar from jsDelivr (`cdn.jsdelivr.net`), a public network that serves open-source files. Like
  any website your browser visits, it receives the address of each file loaded and your browser's
  standard request details, such as your IP address; it receives no Google user data, nothing from
  your files and not your equations. jsDelivr's
  [Privacy Policy](https://www.jsdelivr.com/terms/privacy-policy-jsdelivr-net) applies.
- **The equation you insert or edit** is drawn as an image in your browser and passed, with its
  source, size and color, to Google's Apps Script, which places it in your file. It is not stored
  anywhere else.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own
  Google account's storage for the add-on.
- **Free allowance records**, in the same storage, keep how many of your free equations and edits
  are used. The latest insert or edit adds a random identifier, a one-way fingerprint of the file,
  the equation and its size and color, and its status, so that a retry is not counted twice. No file
  contents or names are stored in these records.
- **A count of your runs**: once MathFill is on the Marketplace, the same storage counts the
  inserts that worked, so that after the third it can ask you, once, whether you would review it. It is used
  for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; MathFill never sees your card. We can see in Stripe your email, your billing country and
  your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

MathFill uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your email to
Stripe. MathFill has no servers of its own. The contents of your files are never sent to us or to
anyone else, and MathFill uses no analytics.

MathFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

MathFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who MathFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no file content.
- Your files never leave Google's services.

Nothing else is shared, transferred or disclosed: MathFill does not sell, rent or trade Google user
data, and does not give it to advertisers, data brokers, analytics providers or any other third
party. We would disclose it only if the law required us to, and only what it required.

## How MathFill protects that data

- **Encryption in transit.** Everything MathFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, between your browser and jsDelivr, and from Apps Script to
  Stripe.
- **Encryption at rest.** Your files, MathFill's settings and its error log are stored by Google,
  which encrypts the data it stores. Your customer record is stored by Stripe, which encrypts it
  too.
- **Access controls.** MathFill runs inside Google's Apps Script, as you, with only the scopes above
  and only in the file you open it in. We have no access to your files or to your settings. Your
  customer record sits in our Stripe account, which only we can sign in to. MathFill reaches Stripe
  with a restricted key that stays on Google's servers and never reaches your browser.
- **Never stored**: the contents of your files outside them, your card details, and your Google
  password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error, or the editor
  refusing an image) goes to MathFill's error log in Google Cloud™, which only we can read.

## Keeping and deleting

- The error log is deleted after 30 days.
- Free allowance records have no automatic expiry; the next insert replaces the latest one's
  record without resetting the count used.
- Your settings and free allowance records stay in your Google account's storage for MathFill and
  contain no file contents. Uninstalling MathFill (Extensions > Add-ons > Manage add-ons) stops it;
  removing it at https://myaccount.google.com/connections also ends its access to your account,
  after which nothing reads them. The equations MathFill inserted, with their alt text, stay in
  your files until you delete them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
