---
layout: page
title: "PhotoFill: Insert & Import Photos, Images in Bulk — Privacy Policy"
permalink: /privacy/photofill/
---

# PhotoFill: Insert & Import Photos, Images in Bulk — Privacy Policy

Last updated: 30 September 2026

PhotoFill is an add-on for Google Slides™ that puts photos you pick in Google Photos™ onto slides.
This policy says what it does with data, including the Google user data it receives.

## What Google user data PhotoFill accesses

- **The photos you pick** (scope `photospicker.mediaitems.readonly`). You select photos in
  Google's own Google Photos™ picker; PhotoFill receives those photos only (the image, its file
  name, size and date taken) and puts them on slides. It cannot see the rest of your library,
  your albums or anything shared with you, and it cannot change or delete anything in Google
  Photos.
- **The presentation you use it in** (scope `presentations.currentonly`). PhotoFill adds slides
  after the current one and puts the photos, and a caption if you ask for one, on them. It has no
  access to your other presentations or files.
- **Your email address** (scope `userinfo.email`). It is how your plan is found: PhotoFill looks
  up the Stripe customer with this email and, when you start a checkout, creates one.
- **Sidebars and menus** (scope `script.container.ui`), to show PhotoFill inside Slides™.
- **Connections to outside services** (scope `script.external_request`), to exactly these:
  Google's Photos Picker API and the Google Photos™ image host, to fetch the photos you picked, and
  Stripe (`api.stripe.com`), to check and sell subscriptions and passes.

## How PhotoFill uses that data

- **Your photos** go from Google Photos™ into your presentation inside Google's Apps Script. They
  are not kept by PhotoFill anywhere else, and never sent to Stripe, to us or to anyone else.
  Google ends the pick itself after a while, or when you pick again.
- **Your settings** (your last layout, order, caption and background, your plan status, your free
  photos of the day and your Stripe customer number) are kept in your own Google account's
  storage for the add-on.
- **A count of your runs**: once PhotoFill is on the Marketplace, the same storage counts the runs
  that did their job, so that after the third it can ask you, once, whether you would review it.
  It is used for nothing else.
- **Payments** are made on Stripe's checkout page. Stripe receives your email, card and billing
  address; PhotoFill never sees your card. We can see in Stripe your email, your billing country
  and your subscription or pass, which we need to provide the service and to account for tax.
  Stripe's [Privacy Policy](https://stripe.com/privacy) applies.

PhotoFill uses Google user data only for the features above. It does not sell or rent it, does
not use it for advertising, and passes it to no one except as those features need: your email to
Stripe. PhotoFill has no servers of its own. Your photos and slides are never sent to us, and
PhotoFill uses no analytics.

PhotoFill does not use Google user data, including data received from Google Workspace™ APIs and
Google Photos™, to develop, improve or train AI or machine-learning models, generalized or
personalized.

PhotoFill's use and transfer of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Who PhotoFill shares Google user data with

PhotoFill shares, transfers or discloses Google user data only to these, and only for the purposes given:

- **Stripe** (our payment processor, [Privacy Policy](https://stripe.com/privacy)) receives your
  email address, to find your plan and, when you buy, to create your customer record and take the
  payment. Stripe receives nothing else of your Google user data: no photos, no presentation
  content.
- **Google** already holds your photos and your presentation. PhotoFill fetches the photos you
  pick from Google Photos™ and puts them into your presentation within Google's services; they are
  not passed to anyone outside Google.

Nothing else is shared, transferred or disclosed: PhotoFill does not sell, rent or trade Google user
data, and does not give it to advertisers, data brokers, analytics providers or any other third
party. We would disclose it only if the law required us to, and only what it required.

## How PhotoFill protects that data

- **Encryption in transit.** Everything PhotoFill sends or receives travels over HTTPS (TLS):
  between your browser and Google, and from Apps Script to the Photos Picker API, the Google
  Photos image host and Stripe. Your photos never leave Google.
- **Encryption at rest.** Your photos, your presentation, PhotoFill's settings and its error log
  are stored by Google, which encrypts the data it stores. Your customer record is stored by
  Stripe, which encrypts it too.
- **Access controls.** PhotoFill runs inside Google's Apps Script, as you, with only the scopes
  above, only in the presentation you open it in and only on the photos you pick. We have no
  access to your photos, your presentations or your settings; only PhotoFill, running as you,
  reads them. Your customer record sits in our Stripe account, which only we can sign in to.
  PhotoFill reaches Stripe with a restricted key that stays on Google's servers and never reaches
  your browser.
- **Never stored**: your photos outside your presentation, your card details, and your Google
  password or sign-in tokens.
- **Errors**: when something fails, its error message (such as a Stripe error, or Google Photos™'
  reason for refusing a request) goes to PhotoFill's error log in Google Cloud™, which only we can
  read.

## Keeping and deleting

- The error log is deleted after 30 days.
- Your settings stay in your Google account's storage for PhotoFill; they hold none of your
  photos. Uninstalling PhotoFill (Extensions > Add-ons > Manage add-ons) stops it; removing it at
  https://myaccount.google.com/connections also ends its access to your account, after which
  nothing reads them. The slides it made stay in your presentation until you delete them.
- To have your data at Stripe deleted, write to us and we delete your Stripe customer. The records
  of your payments are kept for five years after the end of the financial year they belong to, as
  Danish bookkeeping law requires, and deleted after that.

## Contact

Questions about this policy or your data: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
