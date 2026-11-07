---
layout: page
title: "PaperFill: Print Forms™, Answer Keys & Responses — Privacy Policy"
permalink: /privacy/paperfill/
---

# PaperFill: Print Forms™, Answer Keys & Responses — Privacy Policy

Last updated: 6 November 2026

PaperFill is an add-on for Google Forms™ that prints the form you open it in, its answer key and
its responses, and adds questions you paste, or questions from one Google Docs™ document or Google
Sheets™ spreadsheet you choose, to that form as a quiz. This policy says what it does with data, including the Google user
data it receives.

## What Google user data PaperFill accesses

- **The form you use it in** (scope `forms.currentonly`). PaperFill is used by the form's editor.
  - **To print**, it reads the form's title, description and items: questions, choices, right
    answers, points, feedback and pictures. When you choose to print responses, it reads the
    form's responses: each one's time, the respondent's email if the form collects it, the answers
    and the points Forms gave. It does not change the form to print it.
  - **To import**, it reads the form's title and how many items it has, to say where the questions
    go, writes the questions at the end of the form with their right answers, points and feedback,
    and turns on the form's quiz setting. It does not change the questions already there.

  It accesses no other form.
- **The files you choose** (scope `drive.file`). Google's file picker gives PaperFill access only
  to the files you choose for it there:
  - **A Doc or Sheet of your questions.** PaperFill reads it once, when you choose it, to build the
    import's preview. Its contents go only into your form, as the questions you add; they are not
    stored anywhere else.
  - **The form itself.** Google's Forms API answers only for a form you have chosen for the
    add-on. Once you choose the form in the picker, PaperFill reads through that API what Forms
    gives add-ons no other way: short-answer answer keys, the pictures on questions and choices
    and video links, for printing, and it sets the short-answer keys of the questions you import.

  **This access lasts**: Google keeps a file you chose available to PaperFill until you remove
  PaperFill at https://myaccount.google.com/connections. PaperFill does not use it beyond the
  features above. It has no access to the rest of your Drive.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: PaperFill
  looks up the Stripe customer with this email and, when you start a checkout, creates one. It is
  also shown in PaperFill so you can check which Google account is used for your free prints and
  imports and your purchase. Google's installation screen may also say the add-on can 'associate
  you with your personal info on Google'. That is Google's standard sign-in association; PaperFill
  does not request, read or store your profile information.
- **Dialogs and menus** (scope `script.container.ui`), to show PaperFill inside Forms.
- **Connections to outside services** (scope `script.external_request`), to exactly these: Google's
  Forms API, to read the form you chose as above and set short-answer keys in it; Google's Drive
  and Sheets APIs, to read the Doc or Sheet you choose; and Stripe (`api.stripe.com`), to check
  purchases and sell the one-time unlock.

## How PaperFill uses that data

- **The form and its responses** are read inside Google's Apps Script and passed to PaperFill's
  dialog in your browser, which lays out the pages. When you print, your browser's print dialog
  shows them; where you print or save them is your choice. PaperFill keeps no copy: closing the
  dialog discards them. Pictures in the form are shown in the dialog from Google's servers, or
  from the copy Apps Script reads.
- Responses hold your respondents' personal data, such as their emails and answers. PaperFill reads
  them only when you choose to print them, and only for that print. Whether you collect and print
  them, and what happens to the printed pages, is yours to decide as the form's owner.
- **Questions you paste** are read in the dialog, in your browser, for the import's preview. **A
  Doc or Sheet you choose** is read inside Apps Script and passed to the dialog for the preview.
  When you click Add, the questions go through Apps Script into your form.
- None of these are sent to us, to an AI service or to anyone else.
- **Google's file picker** is loaded by the dialog from Google (`apis.google.com`) in your browser,
  with PaperFill's API key, which identifies PaperFill to Google's Picker API. Google's
  [Privacy Policy](https://policies.google.com/privacy) applies to it.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own
  Google account's storage for the add-on.
- **Free allowance records**, in the same storage, keep how many of your free prints and free
  imports are used. The latest print adds a random identifier, a one-way fingerprint of the form's
  ID, the layout, its options and the responses chosen, the layout's name and its status, so that
  printing the same again is free and a retry is not counted twice. The latest import adds a
  random identifier, a one-way fingerprint of the form's ID and the questions, how many questions
  it added and its status, so that an import is neither counted nor written twice. No question
  text, answers, emails or file names are stored in these records.
- **MarkFill**: PaperFill takes the place of MarkFill on the same Google Workspace Marketplace
  listing. The first time PaperFill opens for your account, everything MarkFill kept in your account's
  storage is deleted: its word lists, its options, its free-run count and record of your latest run,
  its count of your runs and its billing cache.
- **A count of your runs**: once PaperFill is on the Marketplace, the same storage counts the
  prints and imports that worked, so that after the third it can ask you, once, whether you would
  review it. It is used for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; PaperFill never sees your card. We can see in Stripe your email, your billing country
  and your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

PaperFill uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your email to
Stripe. PaperFill has no servers of its own. Your forms, their responses, your questions and your
files are never sent to us or to anyone else, and PaperFill uses no analytics.

PaperFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

PaperFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who PaperFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no forms, responses,
  questions or files.
- **People you share the form with** see the questions PaperFill added, as they see the rest of
  the form. What you print goes where you send it.
- Your forms, their responses, your questions and your files never leave Google's services through
  PaperFill.

Nothing else is shared, transferred or disclosed: PaperFill does not sell, rent or trade Google
user data, and does not give it to advertisers, data brokers, analytics providers or any other
third party. We would disclose it only if the law required us to, and only what it required.

## How PaperFill protects that data

- **Encryption in transit.** Everything PaperFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Google's APIs and to Stripe.
- **Encryption at rest.** Your form and its responses, your files, PaperFill's settings and its
  error log are stored by Google, which encrypts the data it stores. Your customer record is
  stored by Stripe, which encrypts it too.
- **Access controls.** PaperFill runs inside Google's Apps Script, as you, with only the scopes
  above, in the form you open it in and the files you choose. We have no access to your forms,
  responses, files or settings. Your customer record sits in our Stripe account, which only we can
  sign in to. PaperFill reaches Stripe with a restricted key that stays on Google's servers and
  never reaches your browser.
- **Never stored**: your form's contents and responses, your questions and file contents outside
  your form, your card details, and your Google password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Forms or Stripe error) goes to
  PaperFill's error log in Google Cloud™, which only we can read.

## Keeping and deleting

- The error log is deleted after 30 days.
- The questions PaperFill added stay in your form until you delete them. Deleting the form deletes
  them.
- Free allowance records have no automatic expiry; the next print or import replaces the latest
  one's record without resetting the count used.
- Your settings and records stay in your Google account's storage for PaperFill and contain no
  form contents, answers or question text. Uninstalling PaperFill stops it; removing it at
  https://myaccount.google.com/connections also ends its access to your account and to the files
  you chose for it, after which nothing reads them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
