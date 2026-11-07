---
layout: page
title: "ChartFill: Sankey, Pareto, Box Plot & Gantt Charts — Privacy Policy"
permalink: /privacy/chartfill/
---

# ChartFill: Sankey, Pareto, Box Plot & Gantt Charts — Privacy Policy

Last updated: 1 November 2026

ChartFill is an add-on for Google Sheets™ that draws charts Sheets does not have (Sankey, Pareto,
box plot, funnel, Likert, Gantt and calendar heat map) from cells you select, and inserts each one
as a picture in the same spreadsheet. It replaces SplitFill on the same Google Workspace
Marketplace listing. This policy says what it does with data, including the Google user data it
receives.

## What Google user data ChartFill accesses

- **The spreadsheet you use it in** (scope `spreadsheets.currentonly`).
  - **To draw a chart**, it reads the cells you select, or the table around the one cell you
    select: their values and the text they display, the tab's name and identifier, and the
    spreadsheet's time zone, to read dates as you see them.
  - **To insert a chart**, it adds the picture to that tab, two columns right of the cells it was
    drawn from, with alt text that says what the chart is and holds its settings (see below).
  - **To list and redraw your charts**, it reads the alt text of the pictures in the spreadsheet,
    to find the ones it inserted. A redraw reads the chart's cells again, inserts the new picture
    at the old one's place and size, and removes the old picture.

  It does not change your cells, and it cannot open your other spreadsheets or browse Drive.
- **Your email address** (scope `userinfo.email`). It is how your purchase is found: ChartFill
  looks up the Stripe customer with this email and, when you start a checkout, creates one. It is
  also shown in ChartFill so you can check which Google account is used for your free charts and
  your purchase. Google's installation screen may also say the add-on can 'associate you with
  your personal info on Google'. That is Google's standard sign-in association; ChartFill does not
  request, read or store your profile information.
- **Menus and the sidebar** (scope `script.container.ui`), to show ChartFill inside Sheets.
- **Connections to outside services** (scope `script.external_request`), to exactly one:
  Stripe (`api.stripe.com`), to check purchases and sell the one-time unlock.

## How ChartFill uses that data

- **The cells you chart** are read inside Google's Apps Script and passed to ChartFill's sidebar
  in your browser, which draws the chart there and shows it as the preview. When you click Insert,
  the picture goes back through Apps Script into your spreadsheet. The cells and the picture are
  sent to no one else: not to us, not to an AI service, not to the chart library's host.
- **The chart library.** The sidebar draws with Apache ECharts™, which your browser loads from
  jsDelivr (`cdn.jsdelivr.net`), a public content network, each time the sidebar opens. That
  request is like any web page's: jsDelivr receives your IP address and browser details, and none
  of your spreadsheet. The browser checks the file against a fixed fingerprint and refuses one
  that differs. jsDelivr's [Privacy Policy](https://www.jsdelivr.com/terms/privacy-policy-jsdelivr-net)
  applies to it.
- **What a chart keeps in your spreadsheet.** Each inserted chart is a picture of your data, and
  its alt text holds: the chart's type and title, the tab and cell range it was drawn from, which
  columns it uses, whether the first row is a header, its options, and a random identifier. This
  is what lets ChartFill redraw the chart later. It holds no cell values, though the picture shows
  them. The picture and its alt text are part of the spreadsheet: everyone who can open it can see
  them, and they go with copies and downloads of it. They stay until you delete the picture.
- **Your settings** (your purchase status and your Stripe customer number) are kept in your own
  Google account's storage for the add-on.
- **The free-chart record**, in the same storage, keeps how many of your free charts are used.
  The latest insert adds a random identifier, a one-way fingerprint of the chart's settings, the
  chart's type and its status, so that a retry is neither counted nor inserted twice. No cell
  values, titles or tab names are stored in it.
- **What SplitFill stored is deleted.** If you used SplitFill, what it kept in your account's
  storage for the add-on (its free-job count, the record of your latest job, your purchase status
  and your Stripe customer number) is deleted the first time ChartFill opens, before ChartFill
  stores anything. ChartFill then finds any SplitFill purchase again in Stripe by your email, so
  it carries over. The short-lived preview record SplitFill kept in Google's cache expires on its
  own within ten minutes. The tabs SplitFill made stay in your spreadsheets.
- **A count of your charts**: once ChartFill is on the Marketplace, the same storage counts the
  charts inserted, so that after the third it can ask you, once, whether you would review it. It
  is used for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; ChartFill never sees your card. We can see in Stripe your email, your billing country
  and your purchase, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

ChartFill uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your email to
Stripe. ChartFill has no servers of its own. Your spreadsheets are never sent to us or to anyone
else, and ChartFill uses no analytics.

ChartFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

ChartFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who ChartFill shares Google user data with

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your purchase and, when you buy, to create your customer record and take
  the payment. Stripe receives nothing else of your Google user data: no cells, charts or
  spreadsheet names.
- **People you share the spreadsheet with** see the charts ChartFill inserted and their alt text,
  as they see the rest of the spreadsheet.
- Your cells and charts never leave Google's services and your browser through ChartFill.

Nothing else is shared, transferred or disclosed: ChartFill does not sell, rent or trade Google
user data, and does not give it to advertisers, data brokers, analytics providers or any other
third party. We would disclose it only if the law required us to, and only what it required.

## How ChartFill protects that data

- **Encryption in transit.** Everything ChartFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, between your browser and jsDelivr, and from Apps Script to
  Stripe.
- **Encryption at rest.** Your spreadsheet, ChartFill's settings and records and its error log are
  stored by Google, which encrypts the data it stores. Your customer record is stored by Stripe,
  which encrypts it too.
- **Access controls.** ChartFill runs inside Google's Apps Script, as you, with only the scopes
  above, in the spreadsheet you open it in. We have no access to your spreadsheets or settings.
  Your customer record sits in our Stripe account, which only we can sign in to. ChartFill reaches
  Stripe with a restricted key that stays on Google's servers and never reaches your browser.
- **Never stored** outside your spreadsheet: your cells, your charts, your card details, and your
  Google password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Sheets or Stripe error) goes to
  ChartFill's error log in Google Cloud™, which only we can read.

## Keeping and deleting

- The error log is deleted after 30 days.
- Inserted charts stay in your spreadsheet until you delete them; deleting a chart deletes its alt
  text with it.
- The free-chart record has no automatic expiry; the next insert replaces the latest one's record
  without resetting the count used.
- Your settings and records stay in your Google account's storage for ChartFill and contain no
  cell values. Uninstalling ChartFill stops it; removing it at
  https://myaccount.google.com/connections also ends its access to your account, after which
  nothing reads them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
