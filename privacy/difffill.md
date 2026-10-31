---
layout: page
title: "DiffFill: Compare Two Columns, Tabs or Sheets - Privacy Policy"
permalink: /privacy/difffill/
---

# DiffFill: Compare Two Columns, Tabs or Sheets - Privacy Policy

Last updated: 28 October 2026

DiffFill compares two tab ranges in the Google Sheets™ spreadsheet where you use it. It previews
keyed differences, or the values two lists do not share, and, on confirmation, creates a separate report tab. This policy explains its
use of data.

## What Google user data DiffFill accesses

- **The current spreadsheet** (`spreadsheets.currentonly`): tab names and identifiers, the two
  explicit ranges you choose, displayed cell values, optional headings and, for two
  tabs, the mapped key and field columns. It rereads the sources before generating a report and reads the report to verify
  completion or recognize a retry. It creates a new report tab without changing the sources or
  overwriting existing reports. At your request, Create sample tabs adds two new tabs of fictional
  rows. It cannot access the rest of your spreadsheets or Drive.
- **Your email address** (`userinfo.email`): to find your purchase in Stripe and create a customer
  when you start checkout. DiffFill displays it so you can check which Google account is used for
  source access, the total free allowance and billing. It checks that account before operations.
  Google's installation screen may also say the add-on can 'associate you with your personal info on
  Google'. That is Google's standard sign-in association; DiffFill does not request, read or store
  your profile information.
- **Menus and sidebars** (`script.container.ui`): to show DiffFill inside Sheets™.
- **External connections** (`script.external_request`): only to `api.stripe.com`, to check your
  purchase and create hosted checkout. No spreadsheet contents, keys, mappings or reports are
  sent to Stripe.

## How DiffFill uses that data

You choose two tabs with their ranges, unique keys and the fields to compare, or two
single-column lists. Google's Apps Script
and Sheets services read and compare displayed values. The preview delivers counts and field
differences to your open sidebar. A confirmed report copies relevant comparison data into a new
tab in your own spreadsheet: keys, field labels, before/after values, source rows and links, or, for lists,
each value with its counts and first rows; and source names/ranges, counts and generation time. That tab follows the spreadsheet's existing
sharing permissions. DiffFill does not invite recipients or merge changes into the sources.

- Preview details and current choices remain in the open sidebar's memory. Closing it clears
  that working copy. **Clear preview** removes the local result and report link, while leaving
  your chosen ranges/mappings, source tabs and completed reports unchanged.
- Google's user cache holds preview configuration, including tab/document identifiers, ranges,
  mapped column indices and user-supplied field labels, plus a content digest and the previous
  job identifier. It contains no source rows or raw cell values. It lasts up to ten minutes and
  may be evicted earlier. Clearing the visible preview does not delete that server cache.
- Your Google account's add-on storage holds total free-report usage and one latest report
  record: a random job identifier, a content/settings fingerprint, document/report identifiers,
  report row count, output hash, timestamps, phase and completion status. It contains no raw
  source values, field labels, source ranges, formulas or email address. It lets the unchanged
  latest job recognize and reopen its verified report without consuming free usage again.
- Plan status and the Stripe customer identifier are cached in your Google account's add-on
  storage. A successful-run count lets DiffFill ask for an honest review once, after the third
  successful run, when its Marketplace listing is live.
- Payments happen on Stripe's checkout page. Stripe receives your email, payment details and
  billing address. DiffFill never receives your card details. We can see your customer and
  payment records in Stripe for support and accounting. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

DiffFill has no spreadsheet database or comparison server of its own. We cannot read your
spreadsheets or their add-on storage. Source values and reports are not sent to us or an analytics
provider. They are not sold, rented, used for advertising, or used to develop, improve or train
AI or machine-learning models, generalized or personalized.

DiffFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Sharing, transfer and disclosure of Google user data

DiffFill does not sell or rent Google user data. It shares, transfers or discloses that data only
as described here:

- **Google** processes your spreadsheet and account sign-in, runs DiffFill on Google Apps Script,
  and hosts comparison/report execution, preview cache, sidebar, add-on storage and operational
  error logs. Preview details are delivered to your browser. Report data remains in your
  spreadsheet under its existing sharing permissions.
- **Stripe** receives your Google account email to look up your purchase and, if you start
  checkout, create its customer and payment records. Purchase checks can happen when you open
  DiffFill, even without starting checkout. Stripe also receives the payment information you
  supply directly. It receives no tab names, cell values, keys, mappings or reports.
- **Spyridon Pikoulas, DiffFill's developer**, can access the Stripe customer/payment records
  and Google Cloud operational error logs described in this policy for support, accounting and
  troubleshooting. We cannot read your spreadsheets or their add-on storage.

DiffFill does not send Google user data to any other service. We do not disclose it to advertisers,
data brokers or analytics providers. We would disclose information we hold only if the law
required it, and only what it required.

## How DiffFill protects data

Connections between your browser, Google and Stripe use HTTPS (TLS). Google and Stripe encrypt
the data they store. DiffFill runs as you with access to the current spreadsheet, rather than
all your spreadsheets. The restricted Stripe key stays on Google's servers and never reaches
your browser. Only we can sign in to our Stripe account.

Operational errors are recorded in Google Cloud™ logs, accessible to us, with 30-day retention.
DiffFill does not deliberately log selected cell contents, raw comparison details or requests.
It never stores your Google password, card details or sign-in tokens in its report record.

## Keeping and deleting

- Closing the sidebar clears its working choices and preview details. **Clear preview** clears
  the local preview, not the chosen mappings, the short-lived server cache or spreadsheet tabs.
- Cached preview settings/digests expire within ten minutes, or sooner if Google's cache evicts
  them. A fresh preview is required after expiry.
- The latest report record has no automatic expiry. A different permitted report replaces it
  before completion; a source-changed or over-allowance refusal does not. **Forget latest retry
  receipt** removes it without restoring free usage, deleting report tabs or removing a purchase.
  The forgotten report loses retry recognition.
- Free usage and account-level plan caches remain in your Google account's add-on storage.
  They contain no raw spreadsheet contents. We cannot read that storage.
- Generated report tabs stay in your spreadsheet until you delete them. Uninstalling DiffFill
  stops it; removing its connection at https://myaccount.google.com/connections ends account
  access. Neither action deletes your sources or generated reports.
- Error logs are deleted after 30 days.
- To request deletion of your Stripe customer record, write to us. Payment records are retained
  for five years after the end of their financial year, as Danish bookkeeping law requires.
  Deleting the customer record can prevent restoring your paid entitlement.

## Contact

[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com)
