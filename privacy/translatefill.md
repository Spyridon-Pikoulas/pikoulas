---
layout: page
title: "TranslateFill: Translate for Forms™ Quiz & Slides™ — Privacy Policy"
permalink: /privacy/translatefill/
---

# TranslateFill: Translate for Forms™ Quiz & Slides™ — Privacy Policy

Last updated: 3 November 2026

TranslateFill is an add-on for Google Slides™ and Google Forms™ that translates the presentation or
form you open it in, keeping its formatting, answer keys and pictures. It is built on the same
Google Workspace Marketplace listing that was MathFill's. This policy says what it does with data,
including the Google user data it receives.

## What Google user data TranslateFill accesses

- **The presentation you use it in** (scope `presentations.currentonly`). TranslateFill reads the
  text of the slides you choose to translate (this slide, the selected slides or all of them): the
  text in their boxes, groups and tables and, if you leave the option on, their speaker notes,
  with each piece of text's formatting. It writes the translation in place of that text, or into
  a copy of each slide placed after it, keeping the formatting. It does not read images, comments
  or your other files.
- **The form you use it in** (scope `forms.currentonly`). TranslateFill reads the form's title and
  description and its items: questions, help text, choices, answer keys, points, feedback, scale
  labels and section titles, and writes their translation back into the form. It does not read
  the form's responses or collect anything from the people who answer it.
- **The form, chosen once in Google's file picker** (scope `drive.file`). The first time you
  translate a form, TranslateFill opens Google's file picker showing only that form, and asks you
  to choose it. Choosing it lets TranslateFill change the form through Google's Forms API, which
  is the way that keeps the pictures on choices and translates short-answer keys; Google allows
  that only for a form you have chosen. TranslateFill uses this access only for the form you
  translate, and has no access to the rest of your Drive. **This access lasts**: Google keeps the
  form available to TranslateFill until you remove TranslateFill at
  https://myaccount.google.com/connections.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: TranslateFill
  looks up the Stripe customer with this email and, when you start a checkout, creates one. It is
  also shown in TranslateFill so you can check which Google account is used for your free
  translations and purchase. Google's installation screen may also say the add-on can 'associate
  you with your personal info on Google'. That is Google's standard sign-in association;
  TranslateFill does not request, read or store your profile information.
- **Sidebars, dialogs and menus** (scope `script.container.ui`), to show TranslateFill inside
  Slides and Forms.
- **Connections to outside services** (scope `script.external_request`), to exactly these: Google's
  Forms API (`forms.googleapis.com`), to translate the form you chose; and Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How TranslateFill uses that data

- **The text to translate** is sent by Google's Apps Script to Google's own translation service
  (Apps Script's Language service, which uses Google Translate), and the translation comes back
  into your file. The text stays within Google; it is not sent to us, to an AI service outside
  Google or to anyone else. Google's [Privacy Policy](https://policies.google.com/privacy)
  applies to it.
- **A preview** shows the first paragraphs or questions translated in the sidebar, and changes
  nothing. It is kept only while the sidebar is open.
- **Google's file picker** is loaded by the dialog from Google (`apis.google.com`) in your
  browser, with TranslateFill's API key, which identifies TranslateFill to Google's Picker API.
- **Your keep-as-is list**, the names and words you ask TranslateFill not to translate, is kept in
  your own Google account's storage for the add-on, so it is there next time.
- **Your settings** (your purchase status and your Stripe customer number) are kept in the same
  storage.
- **Free allowance records**, in the same storage, keep how many of your free slides and
  questions are used. The latest run adds a random identifier, a one-way fingerprint of the file
  and the slides or form translated, and its status, so that a retry is not counted twice. No
  text, file contents or names are stored in these records.
- **A count of your runs**: once TranslateFill is on the Marketplace, the same storage counts the
  translations that worked, so that after the third it can ask you, once, whether you would
  review it. It is used for nothing else.
- **What MathFill kept is deleted.** This listing was MathFill's, an equation editor. When an
  account that used MathFill opens TranslateFill, the settings and free allowance records MathFill
  kept in that account's storage for the add-on are deleted. A MathFill purchase also unlocks
  TranslateFill: it is found in Stripe with your email as above.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; TranslateFill never sees your card. We can see in Stripe your email, your billing
  country and your purchase, which we need to provide the service and to account for tax.
  Stripe's [Privacy Policy](https://stripe.com/privacy) applies.

TranslateFill uses Google user data only for the features above. It does not sell or rent it,
does not use it for advertising, and passes it to no one except as those features need: your text
to Google's translation service, and your email to Stripe. TranslateFill has no servers of its
own. The contents of your files are never sent to us or to anyone outside Google. TranslateFill uses
no analytics service; it counts in its own error log how many accounts reach each usage step
described below.

TranslateFill does not use Google user data, including data received from Google Workspace™ APIs,
to develop, improve or train AI or machine-learning models, generalized or personalized.

TranslateFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who TranslateFill shares Google user data with

- **Google's translation service**, within Google, receives the text you translate, as above.
- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no file content.
- **People you share the file with** see the translation, as they see the rest of the file.
- Your files never leave Google's services.

Nothing else is shared, transferred or disclosed: TranslateFill does not sell, rent or trade Google
user data, and does not give it to advertisers, data brokers, analytics providers or any other
third party. We would disclose it only if the law required us to, and only what it required.

## How TranslateFill protects that data

- **Encryption in transit.** Everything TranslateFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Google's APIs and to Stripe.
- **Encryption at rest.** Your files, TranslateFill's settings and its error log are stored by
  Google, which encrypts the data it stores. Your customer record is stored by Stripe, which
  encrypts it too.
- **Access controls.** TranslateFill runs inside Google's Apps Script, as you, with only the scopes
  above, in the file you open it in and the form you choose. We have no access to your files or
  settings. Your customer record sits in our Stripe account, which only we can sign in to.
  TranslateFill reaches Stripe with a restricted key that stays on Google's servers and never
  reaches your browser.
- **Never stored**: your text and its translation outside your file, your card details, and your
  Google password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Forms, translation or Stripe
  error) goes to TranslateFill's error log in Google Cloud™, which only we can read.
- **Usage steps**: each of these steps adds one line to the same error log, naming only
  TranslateFill and the step: the sidebar or dialog opens, it opens on the Pro offer, Unlock Pro
  is chosen, slides or a form are translated, a translation stops at the free allowance. The line
  holds no file content, text, language, email address or file name. Google adds to every line in
  the log its own key for the account, which does not name you, is used only by TranslateFill and
  changes every 30 days. We use it only to count how many accounts reach each step, and never link
  it to payments, email addresses or other records.

## Keeping and deleting

- The error log, usage steps included, is deleted after 30 days.
- The translation stays in your file until you change or delete it; in Slides, Edit > Undo
  takes it back while the presentation is open.
- Free allowance records have no automatic expiry; the next run replaces the latest one's record
  without resetting the count used.
- Your keep-as-is list, settings and records stay in your Google account's storage for
  TranslateFill. Uninstalling TranslateFill stops it; removing it at
  https://myaccount.google.com/connections also ends its access to your account and to the form
  you chose for it, after which nothing reads them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
