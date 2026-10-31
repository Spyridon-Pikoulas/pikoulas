---
layout: page
title: "QuizFill: Import Quiz Questions with Answer Key — Privacy Policy"
permalink: /privacy/quizfill/
---

# QuizFill: Import Quiz Questions with Answer Key — Privacy Policy

Last updated: 26 October 2026

QuizFill is an add-on for Google Forms™ that adds questions you paste, or questions from one Google
Docs™ document or Google Sheets™ spreadsheet you choose, to the form you open it in as a quiz. This
policy says what it does with data, including the Google user data it receives.

## What Google user data QuizFill accesses

- **The form you use it in** (scope `forms.currentonly`). QuizFill reads the form's title and how
  many items it has, to say where the questions go. When you add questions, it writes them at the
  end of the form with their right answers, points and feedback, and turns on the form's quiz
  setting. It does not change the questions already there, and does not read the form's responses
  or any other form. QuizFill is used by the form's editor. It never reads responses or collects
  anything from the people who answer the form.
- **The files you choose** (scope `drive.file`). Google's file picker gives QuizFill access only to
  the files you choose for it there:
  - **A Doc or Sheet of your questions.** QuizFill reads it once, when you choose it, to build the
    preview. Its contents go only into your form, as the questions you add; they are not stored
    anywhere else.
  - **The form itself.** Google's Forms API sets short-answer answer keys only in a form you have
    chosen for the add-on, so QuizFill asks you to choose the form in the picker when an import
    has short-answer keys. It then reads the form's questions to add those keys.

  **This access lasts**: Google keeps a file you chose available to QuizFill after the import,
  until you remove QuizFill at https://myaccount.google.com/connections. QuizFill does not use it
  beyond the import and the answer keys. It has no access to the rest of your Drive.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: QuizFill looks
  up the Stripe customer with this email and, when you start a checkout, creates one. It is also
  shown in QuizFill so you can check which Google account is used for your free imports and
  purchase. Google's installation screen may also say the add-on can 'associate you with your
  personal info on Google'. That is Google's standard sign-in association; QuizFill does not
  request, read or store your profile information.
- **Dialogs and menus** (scope `script.container.ui`), to show QuizFill inside Forms.
- **Connections to outside services** (scope `script.external_request`), to exactly these: Google's
  Drive and Sheets APIs, to read the Doc or Sheet you choose; Google's Forms API, to set
  short-answer keys in your form; and Stripe (`api.stripe.com`), to check purchases and sell the
  one-time unlock.

## How QuizFill uses that data

- **Questions you paste** are read in the dialog, in your browser, for the preview. **A Doc or
  Sheet you choose** is read inside Google's Apps Script and passed to the dialog for the preview.
  When you click Add, the questions go through Apps Script into your form. Neither is sent to us,
  to an AI service or to anyone else, and neither is kept after the dialog closes.
- **Google's file picker** is loaded by the dialog from Google (`apis.google.com`) in your browser,
  with QuizFill's API key, which identifies QuizFill to Google's Picker API. Google's
  [Privacy Policy](https://policies.google.com/privacy) applies to it.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own
  Google account's storage for the add-on.
- **Free allowance and import records**, in the same storage, keep how many of your free imports
  are used, and the latest import's random identifier, a one-way fingerprint of the form's ID and
  the questions, how many questions it added and its status, so that an import is neither counted
  nor written twice. No question text or file names are stored in these records.
- **A count of your runs**: once QuizFill is on the Marketplace, the same storage counts the
  imports that worked, so that after the third it can ask you, once, whether you would review it.
  It is used for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; QuizFill never sees your card. We can see in Stripe your email, your billing country and
  your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

QuizFill uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your email to
Stripe. QuizFill has no servers of its own. Your questions, files and forms are never sent to us
or to anyone else, and QuizFill uses no analytics.

QuizFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

QuizFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who QuizFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no questions, files or form
  content.
- **People you share the form with** see the questions QuizFill added, as they see the rest of the
  form.
- Your questions, files and forms never leave Google's services.

Nothing else is shared, transferred or disclosed: QuizFill does not sell, rent or trade Google user
data, and does not give it to advertisers, data brokers, analytics providers or any other third
party. We would disclose it only if the law required us to, and only what it required.

## How QuizFill protects that data

- **Encryption in transit.** Everything QuizFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Google's APIs and to Stripe.
- **Encryption at rest.** Your form and files, QuizFill's settings and its error log are stored by
  Google, which encrypts the data it stores. Your customer record is stored by Stripe, which
  encrypts it too.
- **Access controls.** QuizFill runs inside Google's Apps Script, as you, with only the scopes
  above, in the form you open it in and the files you choose. We have no access to your forms,
  files or settings. Your customer record sits in our Stripe account, which only we can sign in
  to. QuizFill reaches Stripe with a restricted key that stays on Google's servers and never
  reaches your browser.
- **Never stored**: your questions and file contents outside your form, your card details, and
  your Google password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Forms or Stripe error) goes to
  QuizFill's error log in Google Cloud™, which only we can read.

## Keeping and deleting

- The error log is deleted after 30 days.
- The questions QuizFill added stay in your form until you delete them. Deleting the form deletes
  them.
- Free allowance and import records have no automatic expiry; the next import replaces the latest
  one's record without resetting the count used.
- Your settings and records stay in your Google account's storage for QuizFill and contain no
  question text. Uninstalling QuizFill stops it; removing it at
  https://myaccount.google.com/connections also ends its access to your account and to the files
  you chose for it, after which nothing reads them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
