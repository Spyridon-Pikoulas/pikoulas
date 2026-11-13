---
layout: page
title: "StyleFill: Custom Styles for Google Docs™ — Privacy Policy"
permalink: /privacy/stylefill/
---

# StyleFill: Custom Styles for Google Docs™ — Privacy Policy

Last updated: 6 November 2026

StyleFill is an add-on for Google Docs™ that keeps your own paragraph and character styles and
applies them in your documents. This policy says what it does with data, including the Google
user data it receives.

## What Google user data StyleFill accesses

- **The document you use it in** (scope `documents.currentonly`). StyleFill reads the formatting
  of the text you select, to make a style from it, and finds the named ranges it added, to count
  and update each style's places. When you apply or update a style, it changes the formatting of
  that text and adds or removes those named ranges. It has no access to your other documents or
  files.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: StyleFill
  looks up the Stripe customer with this email and, when you start a checkout, creates one. It is
  also shown in StyleFill so you can check which Google account is used for your styles, your
  free styles and your purchase. Google's installation screen may also say the add-on can
  'associate you with your personal info on Google'. That is Google's standard sign-in
  association; StyleFill does not request, read or store your profile information.
- **Sidebars and menus** (scope `script.container.ui`), to show StyleFill inside Docs.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How StyleFill uses that data

- **Your document** is read inside Google's Apps Script, and the formatting is written to it
  there. Its text is not read into a style, stored elsewhere or sent anywhere.
- **Your styles** are kept in your own Google account's storage for the add-on, so that every
  document you open StyleFill in has them: each style's name, as you typed it, and its settings
  (font name, size, colors, bold and the like, alignment, spacing, indents, outline level). They
  contain no document text.
- **In the document**: the formatting StyleFill applied, a named range at each place a style
  was applied (named by StyleFill with a random identifier for the style, not its name), and,
  in the document's own storage for StyleFill, each style's identifier with the version its
  places were last updated to. They contain no document text and no style names.
- **Exports and imports**: an export is shown in the sidebar as text, for you to copy; it leaves
  your browser only if you copy it somewhere. An import reads the text you choose or paste inside
  Apps Script and keeps only the styles in it.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own
  Google account's storage for the add-on.
- **Free allowance records**, in the same account storage, keep how many of your free styles are
  spent. The latest make or import adds a random identifier, a one-way fingerprint of the request
  and a random value, its status and the number of styles, so that a retry is not counted twice.
  No document text is stored in these records.
- **A count of your runs**: once StyleFill is on the Marketplace, your account storage counts the
  styles made or imported, so that after a few it can ask you, once, whether you would review it.
  It is used for nothing else.
- **MatchFill**: StyleFill takes the place of MatchFill on the same Google Workspace Marketplace
  listing. The first time StyleFill opens for your account, everything MatchFill kept in your account's
  storage is deleted: its free-run count and record of your latest run, its count of your runs and
  its billing cache.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; StyleFill never sees your card. We can see in Stripe your email, your billing country
  and your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

StyleFill uses Google user data only for the features above. It does not sell or rent it, does
not use it for advertising, and passes it to no one except as those features need: your email to
Stripe. StyleFill has no servers of its own. The contents of your documents are never sent to us
or to anyone else. StyleFill uses no analytics service; it counts in its own error log how many
accounts reach each usage step described below.

StyleFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

StyleFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who StyleFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no document content and no
  styles.
- **People you share the document with** see its formatting, as they see the rest of the
  document. Your styles are seen by no one else unless you export them and pass the text on.
- Your document never leaves Google's services.

Nothing else is shared, transferred or disclosed: StyleFill does not sell, rent or trade Google
user data, and does not give it to advertisers, data brokers, analytics providers or any other
third party. We would disclose it only if the law required us to, and only what it required.

## How StyleFill protects that data

- **Encryption in transit.** Everything StyleFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your document, StyleFill's storage in it, your styles, its settings and
  its error log are stored by Google, which encrypts the data it stores. Your customer record is
  stored by Stripe, which encrypts it too.
- **Access controls.** StyleFill runs inside Google's Apps Script, as you, with only the scopes
  above and only in the document you open it in. We have no access to your documents, your
  styles or your settings. Your customer record sits in our Stripe account, which only we can
  sign in to. StyleFill reaches Stripe with a restricted key that stays on Google's servers and
  never reaches your browser.
- **Never stored**: the text of your document, anywhere outside it; your card details; and your
  Google password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error) goes to
  StyleFill's error log in Google Cloud™, which only we can read.
- **Usage steps**: each of these steps adds one line to the same error log, naming only StyleFill
  and the step: the sidebar opens, it opens on the Pro offer, Unlock Pro is chosen, a style is
  made or imported, a make or import stops at the free allowance. The line holds no document
  content, style name, email address or file name. Google adds to every line in the log its own
  key for the account, which does not name you, is used only by StyleFill and changes every 30
  days. We use it only to count how many accounts reach each step, and never link it to
  payments, email addresses or other records.

## Keeping and deleting

- The error log, usage steps included, is deleted after 30 days.
- The formatting, the named ranges and StyleFill's storage in the document are part of the
  document and stay until you change or delete them. Deleting the document deletes them.
- Your styles stay in your Google account's storage for StyleFill until you delete them in its
  sidebar. Deleting a style there also removes its named ranges from the document it is open in;
  the formatting stays.
- Free allowance records have no automatic expiry; the next make or import replaces the latest
  one's record without resetting the count used.
- Your styles, settings and free allowance records contain no document text. Uninstalling
  StyleFill (Extensions > Add-ons > Manage add-ons) stops it; removing it at
  https://myaccount.google.com/connections also ends its access to your account, after which
  nothing reads them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
