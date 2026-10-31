---
layout: page
title: "PrintFill: QR Code & Barcode Labels - Privacy Policy"
permalink: /privacy/printfill/
---

# PrintFill: QR Code & Barcode Labels - Privacy Policy

Last updated: 21 October 2026

PrintFill turns rows in the Google Sheets™ spreadsheet where you use it into QR or Code 128
labels and downloadable PDF/PNG files. This policy explains its use of data.

## What Google user data PrintFill accesses

- **The current spreadsheet** (`spreadsheets.currentonly`): the cells you select, or the current
  tab's used range when you explicitly choose it; displayed values, optional headings and
  identifiers needed to check the source before output. It does not grant access to the rest
  of your spreadsheets or Drive.
- **Your email address** (`userinfo.email`): to find your purchase in Stripe and create a customer
  when you start checkout. PrintFill displays it so you can check which Google account is used
  for your source, total free allowance and billing. It checks that account before operations.
  Google's installation screen may also say the add-on can 'associate you with your personal info on
  Google'. That is Google's standard sign-in association; PrintFill does not request, read or store
  your profile information.
- **Menus and sidebars** (`script.container.ui`): to show PrintFill inside Sheets™.
- **External connections** (`script.external_request`): only to `api.stripe.com`, to check your
  purchase and create a hosted checkout. No spreadsheet contents or codes are sent to Stripe.

## How PrintFill uses that data

PrintFill reads source rows without changing their cells. You map columns to the exact displayed
code payload, one-line caption and output filename ID, choose a supported label layout and check
the actual prepared labels. Encoding, preview and PDF/PNG/ZIP generation happen in your browser,
using bundled software and fonts. Your source values and generated codes are not uploaded to
Drive, our servers, an external encoder or an AI service. Downloads are explicit; PrintFill does
not save files to Drive or email them.

- The selected rows, column mapping, previews and generated files remain in the open sidebar's
  memory. Closing it or using **Clear working data** clears that working copy. Downloaded files
  remain on your device until you delete them. The ZIP's manifest contains source payloads,
  captions, filenames and label positions; handle and share it with the same care as your Sheet.
- Your Google account's add-on storage holds total free-code usage and one latest generation
  record. It contains a random job identifier, a one-way SHA-256 fingerprint derived from the
  source and output settings, a row-code count, created/completed times and a completion flag.
  It contains no raw cells, payloads, captions, headings, mappings, filenames, source range or
  email address. It lets the same unchanged latest job retry after an interrupted reply or
  reopening without consuming the free allowance again. You reselect the same source and
  options to regenerate its files.
- Plan status and the Stripe customer identifier are cached in your Google account's add-on
  storage. A successful-run count lets PrintFill ask for an honest review once, after the third
  successful run, when its Marketplace listing is live.
- Payments happen on Stripe's checkout page. Stripe receives your email, payment details and
  billing address. PrintFill never receives your card details. We can see your customer and
  payment records in Stripe for support and accounting. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

PrintFill has no spreadsheet database or code-generation server of its own. We cannot read your
spreadsheets or their add-on storage. Spreadsheet content and generated codes are not sent to us
or an analytics provider. They are not sold, rented, used for advertising, or used to develop,
improve or train AI or machine-learning models, generalized or personalized. PrintFill does not
operate a redirect service or track scans of the generated codes.

PrintFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Sharing, transfer and disclosure of Google user data

PrintFill does not sell or rent Google user data. It shares, transfers or discloses that data only
as described here:

- **Google** processes your spreadsheet and account sign-in, runs PrintFill on Google Apps Script,
  and hosts its add-on storage and operational error logs. Selected rows are delivered to your
  own browser to prepare the codes and labels.
- **Stripe** receives your Google account email to look up your purchase and, if you start
  checkout, create its customer and payment records. Purchase checks can happen when you open
  PrintFill, even without starting checkout. Stripe also receives the payment information you
  supply directly. It receives no spreadsheet content, headings, source identifiers, code payloads
  or generated files.
- **Spyridon Pikoulas, PrintFill's developer**, can access the Stripe customer/payment records
  and Google Cloud operational error logs described in this policy for support, accounting and
  troubleshooting. We cannot read your spreadsheets or their add-on storage.

PrintFill does not send Google user data to any other service. We do not disclose it to advertisers,
data brokers or analytics providers. We would disclose information we hold only if the law
required it, and only what it required.

## How PrintFill protects data

Connections between your browser, Google and Stripe use HTTPS (TLS). Google and Stripe encrypt
the data they store. PrintFill runs as you with access to the current spreadsheet, rather than
all your spreadsheets. The restricted Stripe key stays on Google's servers and never reaches
your browser. Only we can sign in to our Stripe account.

Operational errors are recorded in Google Cloud™ logs, accessible to us, with 30-day retention.
PrintFill does not deliberately log selected cell contents, code payloads or raw requests. It
never stores your Google password, card details or sign-in tokens in its generation record.

## Keeping and deleting

- Closing the sidebar or using **Clear working data** clears its working rows, mapping, previews
  and generated files. Delete downloaded files from your device when you no longer need them.
- The latest generation record has no automatic expiry. Authorizing a different permitted batch
  replaces it before completion; a source-changed or over-allowance refusal does not.
  **Forget latest retry receipt** deletes it without resetting total free-code usage or removing your
  purchase. The old job then loses its retry recognition.
- Free usage and account-level plan caches remain in your Google account's add-on storage.
  They contain no raw spreadsheet contents or code payloads. We cannot read that storage.
- Uninstalling PrintFill stops it; removing its connection at
  https://myaccount.google.com/connections ends its account access. Neither action deletes your
  spreadsheet or files you downloaded.
- Error logs are deleted after 30 days.
- To request deletion of your Stripe customer record, write to us. Payment records are retained
  for five years after the end of their financial year, as Danish bookkeeping law requires.
  Deleting the customer record can prevent restoring your paid entitlement.

## Contact

[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com)
