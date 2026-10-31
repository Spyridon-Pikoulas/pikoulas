---
layout: page
title: "QRFill: Form QR Code Creator for Google Forms™ — Privacy Policy"
permalink: /privacy/qrfill/
---

# QRFill: Form QR Code Creator for Google Forms™ — Privacy Policy

Last updated: 27 October 2026

QRFill is an add-on for Google Forms™ that makes QR codes for the form you open it in. This policy
says what it does with data, including the Google user data it receives.

## What Google user data QRFill accesses

- **The form you use it in** (scope `forms.currentonly`). QRFill reads the form's title, its
  published link, whether it is published and accepting responses, and the titles, types and
  choices of its questions, to make the codes. For a prefilled set it asks Forms for a prefilled
  link per answer; nothing is submitted. It writes to the form only when you click **Add a sample
  question**: it then adds a dropdown question "Table" with three choices at the end. It does not
  change the questions already there, and does not read the form's responses or any other form.
  QRFill is used by the form's editor. It never collects anything from the people who scan the
  codes or answer the form.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: QRFill looks
  up the Stripe customer with this email and, when you start a checkout, creates one. It is also
  shown in QRFill so you can check which Google account is used for your free sets and purchase.
  Google's installation screen may also say the add-on can 'associate you with your personal info
  on Google'. That is Google's standard sign-in association; QRFill does not request, read or store
  your profile information.
- **Dialogs and menus** (scope `script.container.ui`), to show QRFill inside Forms.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How QRFill uses that data

- **The codes** are drawn in the dialog, in your browser, from the form's links and your labels.
  The PNG, SVG and ZIP files are made there and saved by your browser; printing goes to your
  browser's print window. They are not sent to us or to anyone else.
- **A logo you choose** is read in your browser and stays there. Only a one-way fingerprint of it
  goes to Apps Script, for the free allowance below; the image is never uploaded or kept after the
  dialog closes.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own
  Google account's storage for the add-on.
- **Free allowance records**, in the same storage, keep how many of your free sets are used, and
  the latest set's random identifier, a one-way fingerprint of its links, labels, colors and logo,
  how many codes it had and its status, so that a set is not counted twice. No links, labels or
  images are stored in these records.
- **A count of your runs**: once QRFill is on the Marketplace, the same storage counts the
  downloads and prints that worked, so that after the third it can ask you, once, whether you would
  review it. It is used for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; QRFill never sees your card. We can see in Stripe your email, your billing country and
  your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

QRFill uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your email to
Stripe. QRFill has no servers of its own. Your forms, codes and logos are never sent to us or to
anyone else, and QRFill uses no analytics.

QRFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

QRFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who QRFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no form content, links or
  codes.
- **People you give the codes to** get your form's link, with a prefilled answer for a prefilled
  set, as they would from the form's own Send button.

Nothing else is shared, transferred or disclosed: QRFill does not sell, rent or trade Google user
data, and does not give it to advertisers, data brokers, analytics providers or any other third
party. We would disclose it only if the law required us to, and only what it required.

## How QRFill protects that data

- **Encryption in transit.** Everything QRFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your form, QRFill's settings and its error log are stored by Google,
  which encrypts the data it stores. Your customer record is stored by Stripe, which encrypts it
  too.
- **Access controls.** QRFill runs inside Google's Apps Script, as you, with only the scopes above,
  in the form you open it in. We have no access to your forms or settings. Your customer record
  sits in our Stripe account, which only we can sign in to. QRFill reaches Stripe with a restricted
  key that stays on Google's servers and never reaches your browser.
- **Never stored**: your codes, labels and logos, your card details, and your Google password or
  sign-in tokens.
- **Errors**: when something fails, its error message (such as a Forms or Stripe error) goes to
  QRFill's error log in Google Cloud™, which only we can read.

## Keeping and deleting

- The error log is deleted after 30 days.
- A sample question QRFill added stays in your form until you delete it.
- Free allowance records have no automatic expiry; the next set replaces the latest one's record
  without resetting the count used.
- Your settings and records stay in your Google account's storage for QRFill and contain no links,
  labels or images. Uninstalling QRFill stops it; removing it at
  https://myaccount.google.com/connections also ends its access to your account.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
