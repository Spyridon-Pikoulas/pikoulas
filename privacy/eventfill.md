---
layout: page
title: "EventFill: Create & Import Calendar Events — Privacy Policy"
permalink: /privacy/eventfill/
---

# EventFill: Create & Import Calendar Events — Privacy Policy

Last updated: 30 September 2026

EventFill is an add-on for Google Sheets™ that makes Google Calendar™ events from the rows of a
sheet and imports a calendar's events into a sheet. This policy says what it does with data,
including the Google user data it receives.

## What Google user data EventFill accesses

- **The spreadsheet you use it in** (scope `spreadsheets.currentonly`). EventFill reads the
  columns you pick, writes each row's event link and sync result next to them, and creates the
  sheet an import goes into. It has no access to your other spreadsheets or files.
- **The events of your calendars** (scope `calendar.events`). EventFill creates the events of
  the rows you send, updates the events it made or imported when their rows change, and reads the
  events of the calendar and days you choose to import. It deletes no event and touches no other
  event.
- **The list of your calendars** (scope `calendar.calendarlist.readonly`), to let you pick one.
  It cannot change your calendars, their settings or who they are shared with.
- **Your email address** (scope `userinfo.email`). It is how your subscription is found:
  EventFill looks up the Stripe customer with this email and, when you start a checkout, creates
  one.
- **Sidebars and menus** (scope `script.container.ui`), to show EventFill inside Sheets™.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check and sell subscriptions.

## How EventFill uses that data

- **Your cells and events** move between your spreadsheet and your Google Calendar™ inside
  Google's Apps Script. When you choose to email guests, Google Calendar™ sends them the
  invitation. Nothing is sent anywhere else or stored by EventFill outside your spreadsheet.
- **Your settings** (your last calendars and options, your plan status, your free uses of the day
  and your Stripe customer number) are kept in your own Google account's storage for the add-on.
  A spreadsheet keeps a short fingerprint of each event it synced, so unchanged rows are not sent
  again.
- **A count of your runs**: once EventFill is on the Marketplace, the same storage counts the runs that
  did their job, so that after the third it can ask you, once, whether you would review it. It
  is used for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; EventFill never sees your card. We can see in Stripe your email, your billing country
  and your subscription, which we need to provide the service and to account for tax. Stripe's
  [Privacy Policy](https://stripe.com/privacy) applies.

EventFill uses Google user data only for the features above. It does not sell or rent it, does not
use it for advertising, and passes it to no one except as those features need: your email to
Stripe, and your invitations to the guests you choose to email. EventFill has no servers of its
own. The contents of your spreadsheets and calendars are never sent to us, and EventFill uses no
analytics.

EventFill does not use Google user data, including data received from Google Workspace™ APIs, to
develop, improve or train AI or machine-learning models, generalized or personalized.

EventFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who EventFill shares Google user data with

EventFill shares, transfers or discloses Google user data only to these, and only for the purposes given:

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your plan and, when you buy, to create your customer record and take the
  payment. Stripe receives nothing else of your Google user data: no spreadsheet or calendar
  content.
- **The guests you list** in a row are added to its event in your Google Calendar™, and Google
  Calendar shows them the event as it does for any guest; when you choose to email guests, Google
  Calendar sends them the invitation. EventFill adds no one you did not list.
- Your events are otherwise created and read within Google's services, in the calendars you
  choose, and not passed to anyone outside Google.

Nothing else is shared, transferred or disclosed: EventFill does not sell, rent or trade Google user
data, and does not give it to advertisers, data brokers, analytics providers or any other third
party. We would disclose it only if the law required us to, and only what it required.

## How EventFill protects that data

- **Encryption in transit.** Everything EventFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to Stripe.
- **Encryption at rest.** Your spreadsheet, your calendars, EventFill's settings and its error
  log are stored by Google, which encrypts the data it stores. Your customer record is stored by
  Stripe, which encrypts it too.
- **Access controls.** EventFill runs inside Google's Apps Script, as you, with only the scopes
  above and only in the spreadsheet you open it in. We have no access to your spreadsheets, your
  calendars or your settings; only EventFill, running as you, reads them. Your customer record
  sits in our Stripe account, which only we can sign in to. EventFill reaches Stripe with a
  restricted key that stays on Google's servers and never reaches your browser.
- **Never stored**: the contents of your spreadsheet or your events outside your spreadsheet and
  your calendar, your card details, and your Google password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error, or Google
  Calendar's reason for refusing an event) goes to EventFill's error log in Google Cloud™, which
  only we can read.

## Keeping and deleting

- The error log is deleted after 30 days.
- Your settings stay in your Google account's storage for EventFill; they hold nothing from your
  spreadsheets or events. Uninstalling EventFill (Extensions > Add-ons > Manage add-ons) stops
  it; removing it at https://myaccount.google.com/connections also ends its access to your
  account, after which nothing reads them. The event fingerprints kept in a spreadsheet stay in it and are deleted with it,
  and the events EventFill made stay in your calendar until you delete them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
