---
layout: page
title: "EventFill: Create & Import Calendar Events — Privacy Policy"
permalink: /privacy/eventfill/
---

# EventFill: Create & Import Calendar Events — Privacy Policy

Last updated: 23 October 2026

EventFill is an add-on for Google Sheets™ that makes Google Calendar™ events from the rows of a
sheet and imports a calendar's events into a sheet. This policy says what it does with data,
including the Google user data it receives.

## What Google user data EventFill accesses

- **The spreadsheet you use it in** (scope `spreadsheets.currentonly`). EventFill reads the
  columns you pick, writes each row's event link and sync result next to them, and creates the
  sheet an import goes into. When you explicitly choose Create sample tab, it also creates a new
  tab with fictional practice rows in that spreadsheet. It has no access to your other spreadsheets or files.
- **The events of your calendars** (scope `calendar.events`). EventFill creates the events of
  the rows you send, updates the events it made or imported when their rows change, and reads the
  events of the calendar and days you choose to import. It deletes no event and touches no other
  event.
- **The list of your calendars** (scope `calendar.calendarlist.readonly`), to let you pick one.
  It cannot change your calendars, their settings or who they are shared with.
- **Your email address** (scope `userinfo.email`). It is how your purchase or existing subscription
  is found: EventFill looks up the Stripe customer with this email and, when you start a checkout,
  creates one. It is also shown in EventFill so you can check which Google account is used for
  this spreadsheet, calendars, free allowance and billing. EventFill checks that displayed account
  before reading or changing sheet/calendar data or starting checkout.
  Google's installation screen may also say the add-on can 'associate you with your personal info on
  Google'. That is Google's standard sign-in association; EventFill does not request, read or store
  your profile information.
- **Sidebars and menus** (scope `script.container.ui`), to show EventFill inside Sheets™.
- **Connections to outside services** (scope `script.external_request`), to exactly one: Stripe
  (`api.stripe.com`), to check purchases and existing subscriptions, sell one-time unlocks, and
  open the billing portal for existing subscriptions.

## How EventFill uses that data

- **Your cells and events** move between your spreadsheet and your Google Calendar™ inside
  Google's Apps Script. When you choose to email guests, Google Calendar™ sends them the
  invitation. Nothing is sent anywhere else or stored by EventFill outside your spreadsheet.
- **Your settings** (your last calendars and options, your plan status, your free allowance and usage,
  and your Stripe customer number) are kept in your own Google account's storage for the add-on.
  A spreadsheet keeps a short fingerprint of each event it synced, so unchanged rows are not sent
  again.
- **Free allowance records** in your Google account's add-on storage keep which allowance applies,
  why, and its usage. The latest request adds a random identifier, a one-way fingerprint of its
  source and options, reserved and confirmed counts, status and a small response to avoid counting
  a retry twice. The response can include the output tab's identifier/name, an opaque Calendar
  continuation token and a generic refusal message; it contains no source rows or event contents.
- **An explicitly saved column setup** keeps a hashed file/tab identifier, a fingerprint of its
  original headings, column numbers and a save time in your own Google account's add-on storage.
  It contains no raw headings, source rows, guest-column choices or event contents. Up to 20
  setups fit within an 8,000-byte limit; saving another can replace the oldest. Forget removes
  the current tab's setup. We cannot read this storage.
- **A count of your runs**: once EventFill is on the Marketplace, the same storage counts the runs that
  did their job, so that after the third it can ask you, once, whether you would review it. It
  is used for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; EventFill never sees your card. We can see in Stripe your email, your billing country
  and your purchase or existing subscription, which we need to provide the service and to account
  for tax. Stripe's [Privacy Policy](https://stripe.com/privacy) applies.

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
- Free allowance records have no automatic expiry. A completed request record can be replaced by
  the next request without resetting the total used. An uncertain request keeps its reservation;
  it is not automatically retried or refunded. Forgetting a column setup does not erase these records.
- Your settings stay in your Google account's storage for EventFill; they contain no source rows
  or event contents. Saved column setups remain until you forget or replace them, or they are evicted
  to stay within the storage limit.
  Uninstalling EventFill (Extensions > Add-ons > Manage add-ons) stops it; removing it at
  https://myaccount.google.com/connections also ends its access to your account, after which nothing
  reads them. The event fingerprints kept in a spreadsheet stay in it and are deleted with it,
  and the events EventFill made stay in your calendar until you delete them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
