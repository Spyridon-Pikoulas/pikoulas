---
layout: page
title: "PacketFill: PDF Mail Merge & Fill PDF Forms - Privacy Policy"
permalink: /privacy/packetfill/
---

# PacketFill: PDF Mail Merge & Fill PDF Forms - Privacy Policy

Last updated: 28 October 2026

PacketFill makes one PDF per row of the Google Sheets™ spreadsheet where you use it, either by
filling a local PDF's named form fields or, from version 6, from a Google Docs™ template you
choose. This policy explains its use of data; what is marked "from version 6" applies once that
version is live.

## What Google user data PacketFill accesses

- **The current spreadsheet** (`spreadsheets.currentonly`): the cells you select, or the current
  tab's used range when you explicitly choose it; displayed values, optional headings, typed
  checkbox values and identifiers needed to check the source before output. It does not grant
  access to the rest of your spreadsheets or Drive.
- **From version 6, files you choose or PacketFill creates** (`drive.file`): the Google Docs™
  template you pick in Google's file picker, a Drive folder you pick for the PDFs, and the files
  PacketFill creates: a temporary copy of the template for each PDF, a folder you ask it to
  create, the PDFs it saves there and an optional sample template. PacketFill cannot open your
  other Drive files, and it does not change your template.
- **Your email address** (`userinfo.email`): to find your purchase in Stripe and create a customer
  when you start checkout. PacketFill displays it so you can check which Google account is used
  for your source, total free allowance and billing. It checks that account before operations.
  Google's installation screen may also say the add-on can 'associate you with your personal info on
  Google'. That is Google's standard sign-in association; PacketFill does not request, read or store
  your profile information.
- **Menus and sidebars** (`script.container.ui`): to show PacketFill inside Sheets™.
- **External connections** (`script.external_request`): to `api.stripe.com`, to check your
  purchase and create a hosted checkout, and, from version 6, to Google's Drive™ and Docs™ APIs,
  only for the template mode's files described above. No spreadsheet or PDF content is sent to
  Stripe.

## How PacketFill uses that data

PacketFill reads source rows without changing their cells. For a PDF form, you choose a local
ordinary AcroForm PDF, map columns to named fields, choose how unmapped fields are handled, check fit and values,
and review actual filled pages. PDF filling, preview and ZIP generation happen in your browser,
using bundled PDF software and fonts. Your local form and completed PDFs are not uploaded to
Drive, our servers, a separate PDF processor or an AI service. The ZIP downloads when you click
its download link; PacketFill does not save it to Drive or email it.

From version 6, for a Google Docs™ template, PacketFill reads the template's text to find its
tags, such as `{{Name}}`, and checks them against your column headings. For each row it copies
the template into your My Drive, replaces the tags in the copy with that row's displayed values,
exports the copy as a PDF and deletes the copy, usually within seconds. The PDFs come back to the
sidebar for a ZIP download, or are saved in the Drive folder you choose or ask PacketFill to
create. This runs as you, through Google's services, without our servers, a separate PDF
processor or an AI service.

- The selected rows, local PDF, mapping, previews and generated files remain in the open sidebar's
  memory. Closing it clears that working copy. Downloaded files remain on your device until you
  delete them.
- Your Google account's add-on storage holds total free-output usage and one latest generation
  record. It contains a random job identifier, a one-way SHA-256 fingerprint derived from the
  source and output settings, a PDF count, created/completed times and a completion flag. It
  contains no raw PDF, cells, headings, field names, mapping, filenames or email address. It lets
  the same unchanged latest job retry after an interrupted reply or reopening without consuming
  the free allowance again. You reselect the same PDF, rows and options to regenerate its files.
  From version 6, for a template run, the record also counts the PDFs made so far, so a stopped
  run can go on without counting them again, and the fingerprint covers the template's
  identifier and version. While a template PDF is being made, the identifiers of its temporary
  copies are kept there too, so a copy left by an interrupted run is deleted the next time you
  use a template.
- Plan status and the Stripe customer identifier are cached in your Google account's add-on
  storage. A successful-run count lets PacketFill ask for an honest review once, after the third
  successful run, when its Marketplace listing is live.
- Payments happen on Stripe's checkout page. Stripe receives your email, payment details and
  billing address. PacketFill never receives your card details. We can see your customer and
  payment records in Stripe for support and accounting. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

PacketFill has no spreadsheet database or PDF server of its own. We cannot read your spreadsheets
or their add-on storage. Spreadsheet and PDF content is not sent to us or an analytics provider.
It is not sold, rented, used for advertising, or used to develop, improve or train AI or
machine-learning models, generalized or personalized.

PacketFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who receives Google user data

- **Google** hosts the spreadsheet, sidebar, add-on storage and, from version 6, the Drive™ files
  described above. Selected rows are delivered to your own browser to prepare completed forms;
  for a template they are written into the temporary copies in your Drive.
- **Stripe** receives your email for billing and the payment information you supply directly.
  It receives no spreadsheet content, headings, identifiers or links, and no PDF documents.

No other party receives your Google user data for these features. We do not give it to advertisers,
data brokers or analytics providers. We would disclose information we hold only if the law
required it, and only what it required.

## How PacketFill protects data

Connections between your browser, Google and Stripe use HTTPS (TLS). Google and Stripe encrypt
the data they store. PacketFill runs as you with access to the current spreadsheet, rather than
all your spreadsheets. The restricted Stripe key stays on Google's servers and never reaches
your browser. Only we can sign in to our Stripe account.

Operational errors are recorded in Google Cloud™ logs, accessible to us, with 30-day retention.
PacketFill does not deliberately log selected cell contents, PDF bytes or raw requests. It never
stores your Google password, card details or sign-in tokens in its generation record.

## Keeping and deleting

- Closing the sidebar clears its working rows, local PDF, mapping, previews and generated files.
  Delete downloaded files from your device when you no longer need them.
- The latest generation record has no automatic expiry. Authorizing a different batch replaces
  it before completion; a source-changed or over-allowance refusal does not. **Forget retry
  history** deletes it without resetting total free-output usage or removing your purchase.
  The old job then loses its retry recognition.
- Free usage and account-level plan caches remain in your Google account's add-on storage.
  They contain no raw spreadsheet or PDF contents. We cannot read that storage.
- Uninstalling PacketFill stops it; removing its connection at
  https://myaccount.google.com/connections ends its account access. Neither action deletes your
  spreadsheet, original PDF or files you downloaded.
- From version 6, each temporary copy is named "PacketFill temporary copy - <PDF name>" and is
  deleted permanently, not moved to your bin, as soon as its PDF is made. A copy left by an
  interrupted run is deleted the next time you use a template. If you don't use one again, you
  can delete any such copy yourself. Your template, the folders and the PDFs saved in Drive stay
  in your Drive until you delete them; uninstalling PacketFill does not delete them.
- Error logs are deleted after 30 days.
- To request deletion of your Stripe customer record, write to us. Payment records are retained
  for five years after the end of their financial year, as Danish bookkeeping law requires.
  Deleting the customer record can prevent restoring your paid entitlement.

## Contact

[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com)
