---
layout: page
title: "AppendFill: Combine & Consolidate Google Sheets™ - Privacy Policy"
permalink: /privacy/appendfill/
---

# AppendFill: Combine & Consolidate Google Sheets™ - Privacy Policy

Last updated: 6 November 2026

AppendFill combines rows from chosen tabs into one new snapshot tab in the Google Sheets™
spreadsheet where you use it. When AppendFill version 7 goes live, the tabs can also be in other
spreadsheets you pick in Google Drive™. This policy explains its use of data.

## What Google user data AppendFill accesses

- **The current spreadsheet** (`spreadsheets.currentonly`): tab names and identifiers, selected
  ranges, headings, typed values, displayed text, formulas and number formats. It reads these
  to review mappings, detect relevant source changes and create/check one new output tab.
  It cannot browse Google Drive™. Until AppendFill version 7 is live, it cannot access your other spreadsheets; when version 7 goes live, it can open only those you pick (below).
- **Spreadsheets you pick** (`drive.file`), when AppendFill version 7 goes live: when you click
  Add another spreadsheet, Google's Drive™ Picker lets you choose a spreadsheet, and AppendFill
  can then open that file, and only files picked for it. It reads the file's name, tab names
  and identifiers and, for the ranges you select, the same cell details as above, through
  Google's Sheets API. It never changes, shares or deletes a picked file. Google asks for this
  permission the first time you add another spreadsheet.
- **Your email** (`userinfo.email`): to find your purchase in Stripe and create a customer when
  you start checkout. It is shown in AppendFill so you can check which account is used for
  source access, free allowance and billing. Operations check that displayed account.
  Google's installation screen may also say the add-on can 'associate you with your personal info on
  Google'. That is Google's standard sign-in association; AppendFill does not request, read or store
  your profile information.
- **Menus and sidebars** (`script.container.ui`): to show AppendFill inside Sheets™.
- **External requests** (`script.external_request`): to `api.stripe.com`, for entitlement
  checks and hosted checkout, and, when AppendFill version 7 goes live, to Google's Sheets API
  (`sheets.googleapis.com`), to read spreadsheets you picked. No rows, headings, tab names,
  mappings, previews or outputs are sent to Stripe.

## How AppendFill uses that data

Google's Apps Script and Sheets services read your selected source ranges, review approved
column mappings and append calculated values with number formats into a new tab. When AppendFill version 7 goes live, a picked spreadsheet's selected ranges are read the same way through Google's Sheets API, and a job can sum rows by a key column instead. Source names, with the file name for a picked spreadsheet, are included in a Source tab column. Selected hidden/filtered rows are included only after your
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
  source tab/range order and typed output headings/title. It does not delete Google cache, receipt or tabs. When AppendFill version 7 goes live, the names and tab lists of spreadsheets you pick are kept there too.
- **Your Google user cache:** preview configuration includes selected tab IDs/ranges, mappings,
  approval choices, output-heading text, proposed output title, document ID, fingerprints and
  previous job ID; when AppendFill version 7 goes live, also the file IDs of picked spreadsheets
  and the sum settings, and, for up to ten minutes while the Picker hands a pick to the sidebar,
  the picked file's ID. It contains no captured data-row arrays or email. It lasts up to ten
  minutes after Preview or the latest successful generation request; failed requests do not
  renew it, and Google may evict it earlier.
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
  and hosts execution, preview cache, sidebar, add-on storage and operational error logs. When
  AppendFill version 7 goes live, Google also shows the Drive™ Picker and serves picked
  spreadsheets through its Sheets API. Preview details reach your browser. Generated tabs stay in
  your spreadsheet under its existing sharing permissions. When AppendFill version 7 goes live:
  Rows combined from a picked spreadsheet become part of this spreadsheet and are visible to
  everyone who can open it, whatever the picked file's own sharing.
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

Each of these usage steps adds one line to the same logs, naming only AppendFill and the step:
the sidebar opens, it opens on the Pro offer, Unlock Pro is chosen, an append job is started, a
job is refused at the free allowance. The line holds no spreadsheet content, heading, tab name,
email address or file name. Google adds to every line in the log its own key for the account,
which does not name you, is used only by AppendFill and changes every 30 days. We use it only to
count how many accounts reach each step, and never link it to payments, email addresses or other
records.

## Keeping and deleting

Closing the sidebar clears its working copy. Cached preview configuration expires as described
above; a fresh Preview of unchanged sources/options can recognize the latest job after expiry.
A different admitted job replaces a completed receipt. An unfinished job blocks a different
one until completion or explicit Forget.

**Forget latest retry receipt**, after confirmation, deletes only that receipt. Usage, completed
counts, purchase, source/output tabs and output ownership tags remain. The forgotten job loses
automatic recovery; existing INCOMPLETE names remain. AppendFill does not repair/delete tabs.
Billing caches and usage stay in your account's add-on storage, which we cannot read.

Source and output tabs remain until you delete them. Uninstalling stops the add-on; removing its connection at https://myaccount.google.com/connections ends account access. When AppendFill version 7 goes live, that also ends its access to spreadsheets you picked. Neither deletes your
tabs. Error logs, usage steps included, are deleted after 30 days. For Stripe customer-record
deletion, contact us; payment records are retained for five years after their financial year
ends under Danish bookkeeping law. Deleting a customer record can prevent restoring the
purchase.

## Contact

[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com)
