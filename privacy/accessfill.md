---
layout: page
title: "AccessFill: Accessibility Checker & Alt Text — Privacy Policy"
permalink: /privacy/accessfill/
---

# AccessFill: Accessibility Checker & Alt Text — Privacy Policy

Last updated: 10 November 2026

**Retiring on 5 January 2027.** That day AccessFill becomes OrgFill on the same Google Workspace
Marketplace listing, and OrgFill's [privacy policy](/privacy/orgfill/) applies to it. This policy
stays up for any copy of AccessFill still installed.

AccessFill is an add-on for Google Docs™, Google Slides™ and Google Sheets™ that checks the file you
open it in for common accessibility issues and fixes the ones you choose. It replaces DiffFill on
the same Google Workspace Marketplace listing. This policy says what it does with data, including
the Google user data it receives.

## What Google user data AccessFill accesses

- **The file you use it in** (scopes `documents.currentonly`, `presentations.currentonly` and
  `spreadsheets.currentonly`, one for each editor). When you check a file, AccessFill reads its
  text, headings, links, colours, images' alt text, slide titles, sheet names, header rows and
  merged cells, to find issues. It changes the file only when you choose a fix, and only that
  fix: an image's alt text, a heading level, a link's text, a text colour or size, typed lines
  made into a list, a title or name, freezing a header row, or unmerging cells. When you choose
  Go to, it selects the issue in the file. It has no access to your other files.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: AccessFill
  looks up the Stripe customer with this email and, when you start a checkout, creates one. It is
  also shown in AccessFill so you can check which Google account is used for your free fixes and
  purchase. Google's installation screen may also say the add-on can 'associate you with your
  personal info on Google'. That is Google's standard sign-in association; AccessFill does not
  request, read or store your profile information.
- **Sidebars and menus** (scope `script.container.ui`), to show AccessFill inside the editors.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How AccessFill uses that data

- **The check** runs in Google's Apps Script. Its results (a short excerpt of the text each issue
  is about, and where it is) are shown in the sidebar and kept nowhere else; closing the sidebar
  discards them.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own
  Google account's storage for the add-on.
- **Free allowance records**, in the same storage, keep how many of your free fixes are used. The
  latest fix adds a random identifier, a one-way fingerprint of the file and the fix, and its
  status, so that a retry is not counted twice. No file contents or names are stored in these
  records.
- **A count of your runs**: once AccessFill is on the Marketplace, the same storage counts the
  fixes that worked, so that after the third it can ask you, once, whether you would review it.
  It is used for nothing else.
- **What DiffFill stored**: if you used DiffFill, the first time AccessFill opens for you it
  deletes what DiffFill kept in your account's storage for the add-on (its free-report count, its
  latest report record and its billing cache). The reports DiffFill made stay in your
  spreadsheets until you delete them.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; AccessFill never sees your card. We can see in Stripe your email, your billing country
  and your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

AccessFill uses Google user data only for the features above. It does not sell or rent it, does
not use it for advertising, and passes it to no one except as those features need: your email to
Stripe. AccessFill has no servers of its own. The contents of your files are never sent to us or to anyone else. AccessFill uses no analytics
service and no AI; it counts in its own error log how many accounts reach each usage step
described below.

AccessFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

AccessFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who AccessFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no file content.
- Your files never leave Google's services.

Nothing else is shared, transferred or disclosed: AccessFill does not sell, rent or trade Google
user data, and does not give it to advertisers, data brokers, analytics providers or any other
third party. We would disclose it only if the law required us to, and only what it required.

## How AccessFill protects that data

- **Encryption in transit.** Everything AccessFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your files, AccessFill's settings and its error log are stored by
  Google, which encrypts the data it stores. Your customer record is stored by Stripe, which
  encrypts it too.
- **Access controls.** AccessFill runs inside Google's Apps Script, as you, with only the scopes
  above and only in the file you open it in. We have no access to your files or to your settings.
  Your customer record sits in our Stripe account, which only we can sign in to. AccessFill
  reaches Stripe with a restricted key that stays on Google's servers and never reaches your
  browser.
- **Never stored**: the contents of your files outside them, the check's results, your card
  details, and your Google password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error, or the editor
  refusing a change) goes to AccessFill's error log in Google Cloud™, which only we can read.
- **Usage steps**: each of these steps adds one line to the same error log, naming only
  AccessFill and the step: the sidebar opens, it opens on the Pro offer, Unlock Pro is chosen, a
  fix is made, a fix stops at the free allowance. The line holds no file content, check result,
  email address or file name. Google adds to every line in the log its own key for the account,
  which does not name you, is used only by AccessFill and changes every 30 days. We use it only
  to count how many accounts reach each step, and never link it to payments, email addresses or
  other records.

## Keeping and deleting

- The error log, usage steps included, is deleted after 30 days.
- Free allowance records have no automatic expiry; the next fix replaces the latest one's record
  without resetting the count used.
- Your settings and free allowance records stay in your Google account's storage for AccessFill
  and contain no file contents. Uninstalling AccessFill (Extensions > Add-ons > Manage add-ons)
  stops it; removing it at https://myaccount.google.com/connections also ends its access to your
  account, after which nothing reads them. The fixes AccessFill made stay in your files like any
  other edit.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
