---
layout: page
title: "SplitFill: Split by Column for Google Sheets™ - Privacy Policy"
permalink: /privacy/splitfill/
---

# SplitFill: Split by Column for Google Sheets™ - Privacy Policy

Last updated: 21 October 2026

SplitFill groups rows from a chosen range in the Google Sheets™ spreadsheet where you use it.
It previews the groups and, on confirmation, creates one snapshot tab per group in that same
spreadsheet. This policy explains its use of data.

## What Google user data SplitFill accesses

- **The current spreadsheet** (`spreadsheets.currentonly`): tab names and identifiers, your chosen
  range and grouping column, typed values/formula results, displayed text, source formulas,
  optional headings, base cell styles and column widths. These copied-data/style checks and
  chosen settings recognize relevant source changes. It checks output typed values, displayed
  text, absence of formulas, managed grid dimensions and tab identities/names/ownership when
  verifying completion or recovering a job. It creates new tabs without changing the source or
  overwriting existing tabs. When you explicitly choose Create sample tab, it also creates a new
  tab with fictional practice rows in that spreadsheet.
  It cannot access your other spreadsheets or browse Drive.
- **Your email address** (`userinfo.email`): to find your purchase in Stripe and create a customer
  when you start checkout. SplitFill displays it so you can check which Google account is used
  for source access, total free allowance and billing. It checks that account before operations.
  Google's installation screen may also say the add-on can 'associate you with your personal info on
  Google'. That is Google's standard sign-in association; SplitFill does not request, read or store
  your profile information.
- **Menus and sidebars** (`script.container.ui`): to show SplitFill inside Sheets™.
- **External connections** (`script.external_request`): only to `api.stripe.com`, to check your
  purchase and create hosted checkout. No cell contents, group labels, source ranges, previews
  or generated tabs are sent to Stripe.

## How SplitFill uses that data

Google's Apps Script and Sheets services group rows by the exact displayed value of your chosen
column. Preview delivers group labels, counts, source row membership and proposed output names
to your open sidebar. Confirmation creates new tabs containing copied values and base styles,
with an optional repeated header. Those tabs follow the spreadsheet's existing sharing
permissions; grouping does not make separate private files or invite recipients.

Formulas become their calculated values. Embedded source hyperlink targets, notes, validation,
conditional formatting, filters, hidden states, protection and mixed rich-text decoration are not
copied. Google Sheets may detect and style plain URL text in the output as it normally does.
Hidden source rows appear visibly in outputs.
Changes solely to omitted source notes, links or rich-text annotations do not invalidate Preview.
Values, displayed text and formulas are read afresh each generation request. Source formatting
and widths may use the cache below between Preview and a fresh full check before completion.
Style-only source changes can therefore be detected after some output tabs have been written;
those tabs are preserved and no completion is recorded.
Supported styles and widths are copied at creation. Output formatting/annotation edits are not
independently audited or overwritten and may remain when checked data and grid stay exact.
The affected output is checked before each write. Other previously written outputs may be
checked only at whole-set completion or when reopening a completed job. Edits or deletions can
therefore be detected later, with partial tabs preserved. Every output must pass the whole-set
check before success or a free-use debit.

- Current choices, previews and output links remain in the open sidebar's memory. Closing it
  clears that working copy. **Clear preview** removes the local result and output links while
  leaving your chosen controls, source, generated tabs and server-side retry record unchanged.
- Google's user cache holds preview configuration: source tab/range, grouping-column index,
  heading/include-hidden choices, document identifier, source/output-name digests and previous
  job identifier. An optional compact source-formatting snapshot also holds number formats,
  base styles, per-cell style indexes and column widths. It contains no cell values, formulas or
  extracted group labels; custom number formats can contain literal text. It lasts up to ten
  minutes after Preview or the latest successful generation request. Failed requests do not renew
  it; Google may evict it earlier. Clearing the visible preview does not delete this cache.
  If formatting metadata is missing, invalid or too large to cache, SplitFill reads it afresh and
  requires a match to the original source signature before further writes.
- Your Google account's add-on storage holds total free-job usage, a completed-job count and
  one latest job record. The record contains a random identifier, document identifier,
  source/options SHA-256 fingerprint, approved-name hashes, timestamps, phase, starting allowance
  decision and output tab identifiers/progress/content hashes. It contains no raw cell text,
  group labels or email address. It lets the unchanged latest job resume or reopen its verified
  tabs without consuming another free job. Output tabs carry job/index metadata for ownership
  checks; this contains no billing identity.
- Plan status and the Stripe customer identifier are cached in your Google account's add-on
  storage. A successful-run count lets SplitFill ask for an honest review once, after the third
  successful run, when its Marketplace listing is live.
- Payments happen on Stripe's checkout page. Stripe receives your email, payment details and
  billing address. SplitFill never receives your card details. We can see your customer and
  payment records in Stripe for support and accounting. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

SplitFill has no spreadsheet database or data-processing server of its own. We cannot read your
spreadsheets or their add-on storage. Cell contents, group labels and output tabs are not sent to
us or an analytics provider. They are not sold, rented, used for advertising, or used to develop,
improve or train AI or machine-learning models, generalized or personalized.

SplitFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Sharing, transfer and disclosure of Google user data

SplitFill does not sell or rent Google user data. It shares, transfers or discloses that data only
as described here:

- **Google** processes your spreadsheet and account sign-in, runs SplitFill on Google Apps Script,
  and hosts grouping/snapshot execution, preview cache, sidebar, add-on storage and operational
  error logs. Preview details are delivered to your browser. Generated tabs stay in your
  spreadsheet under its existing sharing permissions.
- **Stripe** receives your Google account email to look up your purchase and, if you start
  checkout, create its customer and payment records. Purchase checks can happen when you open
  SplitFill, even without starting checkout. Stripe also receives the payment information you
  supply directly. It receives no spreadsheet contents, group labels, previews or output tabs.
- **Spyridon Pikoulas, SplitFill's developer**, can access the Stripe customer/payment records
  and Google Cloud operational error logs described in this policy for support, accounting and
  troubleshooting. We cannot read your spreadsheets or their add-on storage.

SplitFill does not send Google user data to any other service. We do not disclose it to advertisers,
data brokers or analytics providers. We would disclose information we hold only if the law
required it, and only what it required.

## How SplitFill protects data

Connections between your browser, Google and Stripe use HTTPS (TLS). Google and Stripe encrypt
the data they store. SplitFill runs as you with access to the current spreadsheet, rather than
all your spreadsheets. The restricted Stripe key stays on Google's servers and never reaches
your browser. Only we can sign in to our Stripe account.

Operational errors are recorded in Google Cloud™ logs, accessible to us, with 30-day retention.
SplitFill does not deliberately log selected cell contents, group labels, raw requests or raw
source errors. It never stores your Google password, card details or sign-in tokens in its job
record.

## Keeping and deleting

- Closing the sidebar clears its working choices and preview. **Clear preview** clears the local
  result, not the chosen controls, short-lived server cache, job record or spreadsheet tabs.
- Cached preview/formatting metadata expire within ten minutes of Preview or the latest
  successful generation request, or sooner if Google evicts them. Failed requests do not renew
  that period. Preview the unchanged source/options to recognize the latest job after expiry.
- The latest job record has no automatic expiry. A different authorized job replaces a completed
  record; source-changed and over-allowance refusals do not. An unfinished job must be finished
  or explicitly forgotten before beginning a different job.
- **Forget latest retry receipt**, after confirmation, clears that record without restoring free
  usage, removing a purchase or deleting tabs. The old job loses recovery/retry recognition.
  Existing tabs and names stay as they are, including any **INCOMPLETE** names; ownership job/index
  tags on those tabs also remain. SplitFill does not repair or delete them.
- Free usage, completed-job counts and account-level plan caches remain in your Google account's
  add-on storage. They contain no raw spreadsheet contents. We cannot read that storage.
- Source and output tabs stay in your spreadsheet until you delete them. Uninstalling SplitFill
  stops it; removing its connection at https://myaccount.google.com/connections ends account
  access. Neither action deletes your sources or generated tabs.
- Error logs are deleted after 30 days.
- To request deletion of your Stripe customer record, write to us. Payment records are retained
  for five years after the end of their financial year, as Danish bookkeeping law requires.
  Deleting the customer record can prevent restoring your paid entitlement.

## Contact

[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com)
