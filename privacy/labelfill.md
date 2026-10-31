---
layout: page
title: "LabelFill: Print Address & Mailing Labels - Privacy Policy"
permalink: /privacy/labelfill/
---

# LabelFill: Print Address & Mailing Labels - Privacy Policy

Last updated: 21 October 2026

LabelFill turns address rows in the Google Sheets™ spreadsheet where you use it into a printable
PDF. This policy explains its use of data.

## What Google user data LabelFill accesses

- **The current spreadsheet** (`spreadsheets.currentonly`): the range you select, or the current
  tab's used range if you explicitly choose it, its displayed cell values and headings, and
  identifiers needed to check that the source has not changed.
  This does not grant access to the rest of your spreadsheets or Drive.
- **Your email address** (`userinfo.email`): to find your plan in Stripe and create a customer
  when you start checkout. LabelFill displays it so you can check which Google account is used
  for your selected source, free allowance and billing.
  Google's installation screen may also say the add-on can 'associate you with your personal info on
  Google'. That is Google's standard sign-in association; LabelFill does not request, read or store
  your profile information.
- **Menus and sidebars** (`script.container.ui`): to show LabelFill inside Sheets™.
- **External connections** (`script.external_request`): only to `api.stripe.com`, to check your
  purchase and create a hosted checkout. No spreadsheet content is sent to Stripe.

## How LabelFill uses that data

LabelFill reads the displayed values of the selected range without changing its cells. You choose
the address columns, line arrangement, supported label stock and starting slot. Addresses and the
PDF are processed within Google's services and your browser, using bundled fonts and PDF software.
They are not sent to a separate address, font, PDF or AI service. The PDF downloads only when you
click its download link; it is not saved to Drive by LabelFill.

- The selected addresses, preview and generated PDF remain in the open sidebar's memory. Closing
  it clears that working copy; a file you downloaded remains on your device until you delete it.
- Your Google account's add-on storage holds the total free-sheet usage and one latest output
  record. That record contains a random job identifier, a one-way fingerprint derived from the
  selected data and output settings, page/row counts and timestamps. It contains no raw addresses,
  cell values, headings or email address. It lets an unchanged output retry after an interrupted
  reply without consuming the free allowance again.
- Your plan status and Stripe customer identifier are cached in your Google account's add-on
  storage. A successful-run count lets LabelFill ask for an honest review once, after the third
  successful run, when its Marketplace listing is live.
- Payments happen on Stripe's checkout page. Stripe receives your email, payment details and
  billing address. LabelFill never receives your card details. We can see your customer and
  payment records in Stripe for support and accounting. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

LabelFill has no address database or PDF server of its own. We cannot read your spreadsheets or
their add-on storage. Spreadsheet content is not sent to us or an analytics provider. It is not
sold, rented, used for advertising, or used to develop, improve or train AI or machine-learning
models, generalized or personalized.

LabelFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Sharing, transfer and disclosure of Google user data

LabelFill does not sell or rent Google user data. It shares, transfers or discloses that data only
as described here:

- **Google** processes your spreadsheet and account sign-in, runs LabelFill on Google Apps Script,
  and hosts its sidebar, add-on storage and operational error logs. Selected addresses are
  delivered to your own browser to prepare the preview and PDF.
- **Stripe** receives your Google account email to look up your purchase and, if you start
  checkout, create its customer and payment records. Purchase checks can happen when you open
  LabelFill, even without starting checkout. Stripe also receives the payment information you
  supply directly. It receives no spreadsheet addresses, headings, content, source identifiers
  or links.
- **Spyridon Pikoulas, LabelFill's developer**, can access the Stripe customer/payment records
  and Google Cloud operational error logs described in this policy for support, accounting and
  troubleshooting. We cannot read your spreadsheets or their add-on storage.

LabelFill does not send Google user data to any other service. We do not disclose it to advertisers,
data brokers or analytics providers. We would disclose information we hold only if the law
required it, and only what it required.

## How LabelFill protects data

Connections between your browser, Google and Stripe use HTTPS (TLS). Google and Stripe encrypt
the data they store. LabelFill runs as you with access to the current spreadsheet, rather than
all your spreadsheets. The restricted Stripe key stays on Google's servers and never reaches
your browser. Only we can sign in to our Stripe account.

Operational errors are recorded in Google Cloud™ logs, accessible to us, with 30-day retention.
LabelFill does not deliberately log selected cell contents. It never stores your Google password,
card details or sign-in tokens in its output records.

## Keeping and deleting

- Closing the sidebar clears its working addresses, preview and PDF. Delete downloaded files
  from your device when you no longer need them.
- The latest output record has no automatic expiry. A different output replaces it, or
  **Forget retry history** deletes it. Forgetting it does not reset your total free-sheet usage
  or remove your purchase; the old output then loses its retry recognition.
- Free usage and account-level plan caches remain in your Google account's add-on storage.
  They contain no raw spreadsheet contents. We cannot read that storage.
- Uninstalling LabelFill stops it; removing its connection at
  https://myaccount.google.com/connections ends its account access. Neither action deletes your
  spreadsheet or PDFs you downloaded.
- Error logs are deleted after 30 days.
- To request deletion of your Stripe customer record, write to us. Payment records are retained
  for five years after the end of their financial year, as Danish bookkeeping law requires.
  Deleting the customer record can prevent restoring your paid entitlement.

## Contact

[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com)
