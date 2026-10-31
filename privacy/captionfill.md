---
layout: page
title: "CaptionFill: Captions & Cross-References - Privacy Policy"
permalink: /privacy/captionfill/
---

# CaptionFill: Captions & Cross-References - Privacy Policy

Last updated: 23 October 2026

CaptionFill adds and maintains figure/table captions, linked references and lists in the Google
Docs™ document you use it in, including its nested tabs. This policy explains its use of data.

## What Google user data CaptionFill accesses

- **The current document** (`documents.currentonly`): its tabs, text, images, tables, formatting,
  links, named ranges and bookmarks, to identify objects and preview/apply the changes you request.
  This does not grant access to the rest of your documents or Drive.
- **Your email address** (`userinfo.email`): to find your plan in Stripe and create a customer when
  you start checkout. CaptionFill also displays it so you can check which Google account is being
  used for the document and billing.
  Google's installation screen may also say the add-on can 'associate you with your personal info on
  Google'. That is Google's standard sign-in association; CaptionFill does not request, read or
  store your profile information.
- **Menus and sidebars** (`script.container.ui`): to show CaptionFill inside Docs™.
- **External connections** (`script.external_request`): only to `api.stripe.com`, to check your
  purchase and create a hosted checkout. No document content is sent to Stripe.

## How CaptionFill uses that data

Document content is processed inside Google's services to inspect the current document, prepare
a preview and apply your confirmed changes. CaptionFill uses native named ranges and bookmarks
to keep captions and references associated with their targets.

- A preview is cached for up to **10 minutes** in your Google account's add-on cache. It contains
  the proposed captions, reference changes and identifiers needed for Apply.
- An unfinished Apply keeps its operation state, affected text and target descriptions in that
  document's add-on storage so it can resume. Successful completion deletes the detailed operation
  records and target-description chunks, leaving a small last-job summary and bookmark identifiers.
  An unfinished operation has no automatic time-based deletion.
- Named ranges, bookmarks and tracking identifiers remain with the document for future updates.
  Collaborators who can edit the document can use its CaptionFill tracking too.
- Your plan status and Stripe customer identifier are cached in your own Google account's add-on
  storage. Once the Marketplace listing is live, a successful-run count in the same storage lets
  CaptionFill ask for an honest review once, after the third successful run.
- Free allowance records in the same account storage keep which allowance applies and why.
  For the total allowance, a separate record keeps random target identifiers,
  confirmed creation, uncertain attempted targets and one pending job's identifiers and hashed
  document identifier. It reserves space before Apply and prevents a resumed job or another
  document from spending the same free uses twice. It contains no document text, titles, ranges,
  email or raw document identifiers.
- Payments happen on Stripe's checkout page. Stripe receives your email, payment details and
  billing address. CaptionFill never receives your card details. We can see your customer and
  payment records in Stripe for support and accounting. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

CaptionFill has no servers or document database of its own. We cannot read your documents or their
add-on storage. Document content is not sent to us, an AI service or an analytics provider. It is
not sold, rented, used for advertising, or used to develop, improve or train AI or machine-learning
models, generalized or personalized.

CaptionFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Sharing, transfer and disclosure of Google user data

CaptionFill does not sell or rent Google user data. It shares, transfers or discloses that data only
as described here:

- **Google** processes your document and account sign-in, runs CaptionFill on Google Apps Script,
  and hosts its generated content, tracking information, temporary previews, add-on storage
  and operational error logs. Document processing stays within Google's services.
- **Stripe** receives your Google account email to look up your purchase and, if you start
  checkout, create its customer and payment records. Purchase checks can happen when you open
  CaptionFill, even without starting checkout. Stripe also receives the payment information you
  supply directly. It receives no document text, images, captions, document identifiers or links.
- **Spyridon Pikoulas, CaptionFill's developer**, can access the Stripe customer/payment records
  and Google Cloud operational error logs described in this policy for support, accounting and
  troubleshooting. We cannot read your documents or their add-on storage.

CaptionFill does not send Google user data to any other service. We do not disclose it to advertisers,
data brokers or analytics providers. We would disclose information we hold only if the law
required it, and only what it required.

## How CaptionFill protects data

Connections between your browser, Google and Stripe use HTTPS (TLS). Google and Stripe encrypt
the data they store. CaptionFill runs as you with access to the current document, rather than
all your documents. The restricted Stripe key stays on Google's servers and never reaches your
browser. Only we can sign in to our Stripe account.

Operational errors are recorded in Google Cloud™ logs, accessible to us, with 30-day retention.
CaptionFill does not deliberately log document contents. It never stores your Google password,
card details or sign-in tokens in its document tracking.

## Keeping and deleting

- Preview cache entries expire after at most 10 minutes. Removing tracking invalidates old
  previews; it does not immediately erase another editor's already cached preview.
- **Abandon unfinished Apply** deletes the pending operation details and leaves the visible edits
  already made in place. Inspect the document afterwards; partially applied edits are not undone.
- Account-level allowance and target records have no automatic expiry. Abandoning Apply can release
  reserved targets only if creation was never attempted. Confirmed and uncertain attempted targets
  remain counted or reserved; deleting a target or removing document tracking does not restore them.
- **Remove CaptionFill tracking** removes its named ranges and document-storage records. Visible
  captions, text and native bookmark links remain, but CaptionFill stops maintaining them.
  Only a random reset marker remains in the document's add-on storage to reject old cached previews; it contains
  no document content or account identity.
  Deleting the document removes its content and tracking under Google's deletion rules.
- Uninstalling CaptionFill stops it; removing its connection at
  https://myaccount.google.com/connections ends its account access. Neither action deletes the
  captions you created or the document's tracking records. Use Remove tracking first if wanted.
- Error logs are deleted after 30 days. Account-level plan caches and allowance records remain in
  your Google account's add-on storage; they contain no document contents. Removing tracking,
  uninstalling or disconnecting the add-on does not erase the account-level allowance records.
- To request deletion of your Stripe customer record, write to us. Payment records are retained
  for five years after the end of their financial year, as Danish bookkeeping law requires.
  Deleting the customer record can prevent restoring your paid entitlement.

## Contact

[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com)
