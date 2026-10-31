---
layout: page
title: "AppendFill: Combine Tabs for Google Sheets™ - Privacy Policy"
permalink: /privacy/appendfill/
---

# AppendFill: Combine Tabs for Google Sheets™ - Privacy Policy

Last updated: 27 October 2026

AppendFill combines rows from chosen tabs into one new snapshot tab in the Google Sheets™
spreadsheet where you use it. This policy explains its use of data.

## What Google user data AppendFill accesses

- **The current spreadsheet** (`spreadsheets.currentonly`): tab names and identifiers, selected
  ranges, headings, typed values, displayed text, formulas and number formats. It reads these
  to review mappings, detect relevant source changes and create/check one new output tab.
  It cannot browse Google Drive™ or access your other spreadsheets.
- **Your email** (`userinfo.email`): to find your purchase in Stripe and create a customer when
  you start checkout. It is shown in AppendFill so you can check which account is used for
  source access, free allowance and billing. Operations check that displayed account.
  Google's installation screen may also say the add-on can 'associate you with your personal info on
  Google'. That is Google's standard sign-in association; AppendFill does not request, read or store
  your profile information.
- **Menus and sidebars** (`script.container.ui`): to show AppendFill inside Sheets™.
- **External requests** (`script.external_request`): only to `api.stripe.com`, for entitlement
  checks and hosted checkout. No rows, headings, tab names, mappings, previews or outputs are
  sent to Stripe.

## How AppendFill uses that data

Google's Apps Script and Sheets services read your selected source ranges, review approved
column mappings and append calculated values with number formats into a new tab. Source names
are included in a Source tab column. Selected hidden/filtered rows are included only after your
explicit acknowledgement; output rows are visible. New tabs follow the spreadsheet's existing
sharing permissions. AppendFill does not modify source cells, overwrite existing tabs, create
separate files or invite recipients. At your request, Create sample tabs adds two new tabs of
fictional rows, and Add heading row above inserts one new row across the tab above a selected
range (Column A, Column B, …); everything below it moves down one row, unchanged.

The sidebar receives source headings, counts, mapping choices and output links, not full source
data-row arrays. Formulas become calculated values. Embedded source hyperlinks, notes, font/
layout formatting, validation, conditional formatting, filters, protection and rich-text
decoration are not copied. Google Sheets™ may detect plain URL text normally.

- **Sidebar memory:** selected controls, review/preview details and output links remain while
  the sidebar is open, without browser storage. Closing it clears that working copy. Clear
  review removes loaded inspection, mappings, preview token and confirmations, while keeping
  source tab/range order and typed output headings/title. It does not delete Google cache,
  receipt or tabs.
- **Your Google user cache:** preview configuration includes selected tab IDs/ranges, mappings,
  approval choices, output-heading text, proposed output title, document ID, fingerprints and
  previous job ID. It contains no captured data-row arrays or email. It lasts up to ten minutes
  after Preview or the latest successful generation request; failed requests do not renew it,
  and Google may evict it earlier.
- **Your Google account's add-on storage:** total free usage, completion count and one latest
  retry receipt. That receipt contains random job ID, document/output IDs, fingerprints/title
  hash, authorization decision, phase, timestamps and output progress. It contains no raw cell
  values, formulas, headings, tab names or email. It has no automatic expiry. Output ownership
  metadata contains job identifiers, not billing identity. From version 3, a free allowance
  record in the same storage notes which free allowance applies to the account, the reason
  (earlier AppendFill records found, or none) and the usage against it. It contains no cell
  contents or email and has no automatic expiry.
- **Billing:** plan/customer caches and the successful-job review counter use the shared add-on
  billing storage. Stripe receives your email and the payment/billing information you supply
  on its checkout page. We can see Stripe customer/payment records for support and accounting;
  AppendFill never receives card details. [Stripe's privacy policy](https://stripe.com/privacy)
  applies.

AppendFill has no spreadsheet database or data-processing server of its own. We cannot read
your spreadsheets or their add-on storage. Your rows are not sent to us or an analytics
provider, sold, rented, used for advertising, or used to develop or train AI/machine-learning
models. Its use and transfer of Google API information adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including Limited Use requirements.

## Sharing, transfer, disclosure and protection

AppendFill does not sell or rent Google user data. It shares, transfers or discloses that data only
as described here:

- **Google** processes your spreadsheet and account sign-in, runs AppendFill on Google Apps Script,
  and hosts execution, preview cache, sidebar, add-on storage and operational error logs. Preview
  details reach your browser. Generated tabs stay in your spreadsheet under its existing
  sharing permissions.
- **Stripe** receives your Google account email to look up your purchase and, if you start
  checkout, create its customer and payment records. Purchase checks can happen when you open
  AppendFill, even without starting checkout. Stripe also receives the payment information you
  supply directly. It receives no spreadsheet contents, source identifiers, headings, mappings,
  previews or output tabs.
- **Spyridon Pikoulas, AppendFill's developer**, can access the Stripe customer/payment records
  and Google Cloud operational error logs described in this policy for support, accounting and
  troubleshooting. We cannot read your spreadsheets or their add-on storage.

AppendFill does not send Google user data to any other service. We do not disclose it to advertisers,
data brokers or analytics providers. We would disclose information we hold only if the law
required it, and only what it required.

Connections use HTTPS/TLS. Google and Stripe encrypt stored data. The restricted Stripe key
stays on Google's servers, never in the browser; only we can access our Stripe account.
Operational errors use Google Cloud™ logs accessible to us, with 30-day retention. AppendFill
does not deliberately log source contents or raw source errors, and does not store your Google
password, card details or sign-in tokens in its receipt.

## Keeping and deleting

Closing the sidebar clears its working copy. Cached preview configuration expires as described
above; a fresh Preview of unchanged sources/options can recognize the latest job after expiry.
A different admitted job replaces a completed receipt. An unfinished job blocks a different
one until completion or explicit Forget.

**Forget latest retry receipt**, after confirmation, deletes only that receipt. Usage, completed
counts, purchase, source/output tabs and output ownership tags remain. The forgotten job loses
automatic recovery; existing INCOMPLETE names remain. AppendFill does not repair/delete tabs.
Billing caches and usage stay in your account's add-on storage, which we cannot read.

Source and output tabs remain until you delete them. Uninstalling stops the add-on; removing its
connection at https://myaccount.google.com/connections ends account access. Neither deletes
your tabs. Error logs are deleted after 30 days. For Stripe customer-record deletion, contact
us; payment records are retained for five years after their financial year ends under Danish
bookkeeping law. Deleting a customer record can prevent restoring the purchase.

## Contact

[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com)
