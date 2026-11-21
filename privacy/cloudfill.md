---
layout: page
title: "CloudFill: Word Cloud for Slides™, Docs™ & Sheets™ — Privacy Policy"
permalink: /privacy/cloudfill/
---

# CloudFill: Word Cloud for Slides™, Docs™ & Sheets™ — Privacy Policy

Last updated: 10 November 2026

CloudFill is an add-on for Google Slides™, Google Docs™ and Google Sheets™ that makes a word cloud
from the text of the presentation, document or spreadsheet you open it in, and inserts it there as
a picture. From 3 November 2026 it replaces RandomFill on the same Google Workspace Marketplace
listing. This policy says what it does with data, including the Google user data it receives.

## What Google user data CloudFill accesses

- **The file you use it in**: the presentation (scope `presentations.currentonly`), the document
  (`documents.currentonly`) or the spreadsheet (`spreadsheets.currentonly`). It cannot open your
  other files or browse Drive.
  - **To count the words**, it reads the text of the whole file, or of what you select:
    - in Slides, the text in the slides' text boxes, shapes, groups and tables, and the speaker
      notes if you tick **Include speaker notes**;
    - in Docs, the text of every tab, or of the selected text;
    - in Sheets, the text the cells display on the open tab, or in the selected cells.
  - **To insert the cloud**, it finds where it goes (the current slide, the cursor or the end of
    the selected text in Docs, the selected cells in Sheets) and adds the picture there: centred on
    the slide, in the text at the cursor or in a new paragraph after the selected text, or over the
    cells to the right of the selection. It
    gives the picture alt text: "Word cloud" and up to 12 of the cloud's biggest words.

  It does not change your text or cells.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: CloudFill looks
  up the Stripe customer with this email and, when you start a checkout, creates one. It is also
  shown in CloudFill so you can check which Google account is used for your free clouds and your
  purchase. Google's installation screen may also say the add-on can 'associate you with your
  personal info on Google'. That is Google's standard sign-in association; CloudFill does not
  request, read or store your profile information.
- **Menus and the sidebar** (scope `script.container.ui`), to show CloudFill inside Slides, Docs
  and Sheets.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How CloudFill uses that data

- **The text you make a cloud of** is read inside Google's Apps Script and passed to CloudFill's
  sidebar in your browser, which counts the words, lays them out and draws the cloud there as the
  preview. It keeps the text only while the sidebar is open. When you click Insert, the picture goes
  back through Apps Script into your file. The text and the picture are sent to no one else: not to
  us, not to an AI service, not to any other site.
- **Nothing is loaded from other sites.** The layout library (d3-cloud) and the stop-word lists
  are part of CloudFill, and the cloud is drawn in fonts already on your computer, so the sidebar
  makes no request outside Google.
- **What a cloud keeps in your file.** Each inserted cloud is a picture of words from your file,
  and its alt text lists up to 12 of them. The picture and its alt text are part of the file:
  everyone who can open it can see them, and they go with copies and downloads of it. They stay
  until you delete the picture.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own
  Google account's storage for the add-on.
- **The free-cloud record**, in the same storage, keeps how many of your free clouds are used. The
  latest insert adds a random identifier, a one-way fingerprint made from the file's identifier
  and a random number, and its status, so that a retry is neither counted nor inserted twice. No
  text, words or file names are stored in it.
- **What RandomFill stored is deleted.** If you used RandomFill, what it kept in your account's
  storage for the add-on (its free-fill count, the record of your latest fill, your purchase status
  and your Stripe customer number) is deleted the first time CloudFill opens, before CloudFill
  stores anything. CloudFill then finds any RandomFill purchase again in Stripe by your email, so it
  carries over. The values, passwords and team tabs RandomFill wrote stay in your spreadsheets.
- **A count of your clouds**: once CloudFill is on the Marketplace, the same storage counts the
  clouds inserted, so that after the third it can ask you, once, whether you would review it. It is
  used for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; CloudFill never sees your card. We can see in Stripe your email, your billing country
  and your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

CloudFill uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your email to
Stripe. CloudFill has no servers of its own. Your files are never sent to us or to anyone else.
CloudFill uses no analytics service; it counts in its own error
log how many accounts reach each usage step described below.

CloudFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

CloudFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who CloudFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no text, clouds or file names.
- **People you share the file with** see the clouds CloudFill inserted and their alt text, as they
  see the rest of the file.
- Your text and clouds never leave Google's services and your browser through CloudFill.

Nothing else is shared, transferred or disclosed: CloudFill does not sell, rent or trade Google user
data, and does not give it to advertisers, data brokers, analytics providers or any other third
party. We would disclose it only if the law required us to, and only what it required.

## How CloudFill protects that data

- **Encryption in transit.** Everything CloudFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your file, CloudFill's settings and records and its error log are stored
  by Google, which encrypts the data it stores. Your customer record is stored by Stripe, which
  encrypts it too.
- **Access controls.** CloudFill runs inside Google's Apps Script, as you, with only the scopes
  above, in the file you open it in. We have no access to your files or settings. Your customer
  record sits in our Stripe account, which only we can sign in to. CloudFill reaches Stripe with a
  restricted key that stays on Google's servers and never reaches your browser.
- **Never stored** outside your file: your text and your clouds. Never stored at all: your card
  details, and your Google password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Slides, Docs, Sheets or Stripe
  error) goes to CloudFill's error log in Google Cloud™, which only we can read.
- **Usage steps**: each of these steps adds one line to the
  same error log, naming only CloudFill and the step: the sidebar opens, it opens on the Pro
  offer, Unlock Pro is chosen, a cloud is inserted, an insert stops at the free clouds. The line
  holds no text, words, cloud, email address or file name. Google adds to every line in the log
  its own key for the account, which does not name you, is used only by CloudFill and changes
  every 30 days. We use it only to count how many accounts reach each step, and never link it to
  payments, email addresses or other records.

## Keeping and deleting

- The error log, usage steps included, is deleted after 30 days.
- Inserted clouds stay in your file until you delete them; deleting a cloud deletes its alt text
  with it. **Edit > Undo** right after inserting takes it out.
- The free-cloud record has no automatic expiry; the next insert replaces the latest one's record
  without resetting the count used.
- Your settings and records stay in your Google account's storage for CloudFill and contain no
  text. Uninstalling CloudFill stops it; removing it at https://myaccount.google.com/connections
  also ends its access to your account, after which nothing reads them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
