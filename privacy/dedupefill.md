---
layout: page
title: "DedupeFill: Find & Remove Duplicates for Sheets™ - Privacy Policy"
permalink: /privacy/dedupefill/
---

# DedupeFill: Find & Remove Duplicates for Sheets™ - Privacy Policy

Last updated: 25 October 2026

DedupeFill reviews duplicate rows in the spreadsheet where you use it and creates separate
retained-row and discarded-row snapshots. This policy explains its use of data.

## Google access and processing

- **The current spreadsheet** (`spreadsheets.currentonly`): tab names and IDs, your selected
  range, headings, typed values, formulas, displayed text and number formats. Google's Apps
  Script and Sheets services use them to review matching, check for changes and create/check
  two new tabs. DedupeFill cannot browse Drive or access your other spreadsheets.
- **Your email** (`userinfo.email`): displayed so you can check the account used for source
  access, free allowance and purchases. Operations check that account. Stripe uses it to find
  your purchase and create a customer when you start checkout.
  Google's installation screen may also say the add-on can 'associate you with your personal info on
  Google'. That is Google's standard sign-in association; DedupeFill does not request, read or store
  your profile information.
- **Menus and sidebars** (`script.container.ui`): the review, progress and billing controls
  inside Sheets.
- **External requests** (`script.external_request`): only to `api.stripe.com`, for entitlement
  checks and hosted checkout. Spreadsheet contents, keys, tab names and outputs are not sent
  to Stripe.

Selected hidden and filtered rows participate. DedupeFill leaves source cells and existing tabs
intact. The two outputs contain calculated values and number formats; the discarded report adds
original and retained source-row numbers. They inherit the spreadsheet's existing sharing
permissions. DedupeFill does not create separate files or invite recipients. Optional Create
sample tab adds a new tab with fictional practice data; it does not change your existing tabs.

## Working copies and storage

- **Sidebar memory:** source headings, matching choices, complete retained/discarded review
  values (for a free trial Preview, the counts and the first 25 rows of each side), counts and
  output links reach your browser. They are held in the open sidebar, without
  browser storage. Closing it clears that working copy.
- **Your Google user cache:** preview configuration contains document/source IDs, range,
  selected key-column indices, matching choices, proposed output titles, fingerprints and job
  identifiers. It contains no data-row arrays or email. It lasts up to ten minutes after Preview
  or the latest successful generation request; failed requests do not renew it. Google may evict
  it earlier.
- **Your account's add-on storage:** total free usage, completion count and one latest recovery
  receipt. The receipt holds random job ID, document/output IDs, fingerprints, title hash,
  authorization decision, phase and progress cursors. It contains no raw cell values, formulas,
  headings, key text, tab names or email. It has no automatic expiry. Output ownership tags
  contain job identifiers, not billing identity. From version 2, a free allowance record in the
  same storage notes which free allowance applies to the account, the reason (earlier DedupeFill
  records found, or none) and the usage against it. It contains no cell contents or email and has
  no automatic expiry.
- **Billing:** the shared billing code stores plan/customer caches and a successful-job review
  counter in your account's add-on storage. Stripe receives your email and the payment/billing
  information you enter on its checkout page. DedupeFill never receives card details.
  [Stripe's privacy policy](https://stripe.com/privacy) applies.

## Sharing, transfer, disclosure and protection

DedupeFill does not sell or rent Google user data. It shares, transfers or discloses data only
as described here:

- **Google** processes your spreadsheet and account sign-in, runs DedupeFill on Apps Script,
  and hosts its sidebar, preview cache, add-on storage and operational error logs. Review values
  reach your browser. Generated tabs remain under the spreadsheet's existing sharing permissions.
- **Stripe** receives your Google account email to look up your purchase and, if you start
  checkout, create its customer/payment records. Purchase checks can happen when you open
  DedupeFill without starting checkout. Stripe receives payment information you supply directly;
  it receives no spreadsheet contents, source identifiers, keys, previews or output tabs.
- **Spyridon Pikoulas, DedupeFill's developer**, can access Stripe customer/payment records and
  Google Cloud operational error logs for support, accounting and troubleshooting. We cannot
  read your spreadsheets or their add-on storage.

DedupeFill has no spreadsheet database or data-processing server of its own. It does not send
Google user data to other services, advertisers, data brokers or analytics providers, or use it
for advertising or developing/training AI models. We would disclose information we hold only
if the law required it, and only what it required. Use and transfer of Google API information
adheres to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including Limited Use requirements.

Connections use HTTPS/TLS. Google and Stripe encrypt stored data. The restricted Stripe key
stays on Google's servers, never in the browser. Operational errors use Google Cloud logs
accessible to us, with 30-day retention. DedupeFill does not deliberately log row contents or
raw source errors, or store your Google password, card details or sign-in tokens in its receipt.

## Keeping and deleting

A fresh Preview of unchanged source/options can recognize the latest job after cache expiry.
A different admitted job replaces a completed receipt; an unfinished one blocks a different
job until completion or explicit Forget.

**Forget latest retry receipt**, after confirmation, deletes only that receipt. It leaves
usage, completion count, purchase, source/output tabs and ownership tags intact. The forgotten
job loses automatic recovery; existing INCOMPLETE names remain. DedupeFill does not repair or
delete tabs. Source/output tabs remain until you delete them.

Uninstalling stops the add-on; removing its connection at https://myaccount.google.com/connections
ends account access. Neither deletes your tabs. Error logs are deleted after 30 days. For Stripe
customer-record deletion, contact us; payment records are retained for five years after their
financial year ends under Danish bookkeeping law. Deleting a customer record can prevent
restoring the purchase.

## Contact

[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com)
