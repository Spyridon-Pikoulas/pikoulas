---
layout: page
title: "OrgFill: Org Chart Maker for Google Sheets™ — Privacy Policy"
permalink: /privacy/orgfill/
---

# OrgFill: Org Chart Maker for Google Sheets™ — Privacy Policy

Last updated: 10 November 2026

OrgFill is an add-on for Google Sheets™ and Google Slides™ that draws an org chart from a list of people
and puts it in your file. This policy says what it does with data, including the Google user data it
receives.

## What Google user data OrgFill accesses

- **The spreadsheet or presentation you use it in** (scopes `spreadsheets.currentonly` and
  `presentations.currentonly`). In a spreadsheet, OrgFill reads the cells of the sheet you are on, or of
  the cells you select, as they are shown, with the sheet's name, to make the chart; when you insert, it
  puts the picture beside those cells and sets its alt text. In a presentation it reads nothing of your
  content: you paste the rows into OrgFill, and when you insert, it reads the current slide and the
  slide's size and puts the chart's boxes and connectors on it. It has no access to your other files,
  and it changes nothing already in this one.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: OrgFill looks up
  the Stripe customer with this email and, when you start a checkout, creates one. It is also shown in
  OrgFill so you can check which Google account is used for your free charts and purchase. Google's
  installation screen may also say the add-on can 'associate you with your personal info on Google'.
  That is Google's standard sign-in association; OrgFill does not request, read or store your profile
  information.
- **Sidebars and menus** (scope `script.container.ui`), to show OrgFill inside Sheets and Slides.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How OrgFill uses that data

- **The people in your list**: their names, job titles and managers' names are personal data of those
  people. OrgFill uses them only to draw the chart: the preview is drawn in your browser, and on Insert
  the rows go to Google's Apps Script, which lays the chart out again and puts it in your file. They are
  not kept anywhere else, and not sent anywhere else.
- **In the file**: on a slide, the names and titles are the boxes' text; in a sheet, they are in the
  picture, and its alt text names the people at the top of the chart, with their titles. Everyone who
  can open the file can see them, as they see the rest of it. OrgFill keeps nothing in the file's own
  add-on storage.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own Google
  account's storage for the add-on.
- **Free allowance records**, in the same account storage, keep how many of your free charts are used.
  The latest insert adds a random identifier, a one-way fingerprint of the file and the request, and its
  status, so that an insert that fails is not counted. No names or file contents are stored in these
  records.
- **A count of your runs**: once OrgFill is on the Marketplace, your account storage counts the charts
  inserted, so that after the third it can ask you, once, whether you would review it. It is used for
  nothing else.
- **AccessFill**: OrgFill takes the place of AccessFill on the same Google Workspace Marketplace
  listing. The first time OrgFill opens for your account, everything AccessFill kept in your account's
  storage is deleted: its count of free fixes and the records behind it, its count of your runs and its
  billing cache, and the same records of DiffFill, which AccessFill replaced, if they are still there.
  AccessFill kept nothing in your files; the fixes it made stay in them like any other edit.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing address;
  OrgFill never sees your card. We can see in Stripe your email, your billing country and your purchase,
  which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

OrgFill uses Google user data only for the features above. It does not sell or rent it, does not use it
for advertising, and passes it to no one except as those features need: your email to Stripe. OrgFill
has no servers of its own. The contents of your files, the names in your list included, are never sent
to us or to anyone else. OrgFill uses no analytics service and no AI; it counts in its own error log how
many accounts reach each usage step described below.

OrgFill does not use Google user data, including data received from Google Workspace™ APIs, to develop,
improve or train AI or machine-learning models, generalized or personalized.

OrgFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who OrgFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your email
  address, to find your purchase and, when you buy, to create your customer record and take the payment.
  Stripe receives nothing else of your Google user data: no file contents and no names from your list.
- **People you share the file with** see the chart and its alt text, as they see the rest of it.
- Your file never leaves Google's services.

Nothing else is shared, transferred or disclosed: OrgFill does not sell, rent or trade Google user data,
and does not give it to advertisers, data brokers, analytics providers or any other third party. We would
disclose it only if the law required us to, and only what it required.

## How OrgFill protects that data

- **Encryption in transit.** Everything OrgFill sends or receives travels over HTTPS (TLS): between your
  browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your file, OrgFill's settings and its error log are stored by Google, which
  encrypts the data it stores. Your customer record is stored by Stripe, which encrypts it too.
- **Access controls.** OrgFill runs inside Google's Apps Script, as you, with only the scopes above and
  only in the file you open it in. We have no access to your files or to your settings. Your customer
  record sits in our Stripe account, which only we can sign in to. OrgFill reaches Stripe with a
  restricted key that stays on Google's servers and never reaches your browser.
- **Never stored**: your list outside your file, your card details, and your Google password or sign-in
  tokens.
- **Errors**: when something fails, its error message (such as a Stripe error, or the editor refusing a
  chart) goes to OrgFill's error log in Google Cloud™, which only we can read.
- **Usage steps**: each of these steps adds one line to the same error log, naming only OrgFill and the
  step: the sidebar opens, it opens on the Pro offer, Unlock Pro is chosen, a chart is inserted, an
  insert stops at the free allowance. The line holds no file content, name from your list, email address
  or file name. Google adds to every line in the log its own key for the account, which does not name
  you, is used only by OrgFill and changes every 30 days. We use it only to count how many accounts reach
  each step, and never link it to payments, email addresses or other records.

## Keeping and deleting

- The error log, usage steps included, is deleted after 30 days.
- The chart and its alt text are part of the file and stay until you delete them. Deleting the file
  deletes them.
- Free allowance records have no automatic expiry; the next insert replaces the latest one's record
  without resetting the count used.
- Your settings and free allowance records stay in your Google account's storage for OrgFill and contain
  no names or file content. Uninstalling OrgFill (Extensions > Add-ons > Manage add-ons) stops it;
  removing it at https://myaccount.google.com/connections also ends its access to your account, after
  which nothing reads them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records of
  your payments are kept for five years after the end of the financial year they belong to, as Danish
  bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
