---
layout: page
title: "Stoplist: Checkout Blocklist — Privacy Policy"
permalink: /privacy/blocklist/
---

# Stoplist: Checkout Blocklist — Privacy Policy

Last updated: 27 September 2026

Stoplist is a Shopify app, made by Spyridon Pikoulas, that lets a store refuse checkout to buyers
it has blocked. This policy says what it does with data: the store's, and that of the buyers a
store blocks. The store decides whom to block; Stoplist processes their details on the store's
behalf and for nothing else.

## What Stoplist accesses and why

- **The details of buyers a store blocks.** When a store blocks the buyer of an order, or an
  order gets a Shopify Payments chargeback while the store has automatic blocking on, Stoplist
  reads that order's email address, phone numbers and shipping address (first line, postcode and
  country) from Shopify (scopes `read_orders`, `read_shopify_payments_disputes`). A store can also
  type an email, phone number or address in by hand. Stoplist never reads names, billing addresses
  or payment details.
- **Chargebacks.** For each chargeback, the dispute's and order's numbers and the reason given.
- **The store's checkout rule** (scope `write_validations`), which Stoplist creates to run its
  check at checkout.
- **The store's address, plan and settings**: the access token Shopify issues at install, the
  message shown to blocked buyers, and whether automatic blocking is on.

## What is kept

Stoplist does not keep the email addresses, phone numbers or addresses it blocks. It turns each
one into a one-way code, made with a secret that is different for every store, and keeps that
code with a masked label for the store to recognise the entry (for example `j•••@gmail.com`), the
order number and the store's note.

## At checkout

Shopify runs Stoplist's check inside its own checkout. The check turns the buyer's email, phone
and delivery address into codes the same way and compares them with the store's list; it also
checks whether the buyer's customer account carries the store's `blocklist` tag. It runs
entirely within Shopify: checkout details are not sent to Stoplist, and no record of checkouts is
kept. A buyer who matches is shown the store's message and cannot complete the order.

## Where it is kept, and sharing

Data is stored with Cloudflare (Workers and D1), which encrypts it at rest and in transit. Each
store's list is used only in that store's checkout; lists are never shared or combined between
stores. Stoplist does not sell or share data, uses no analytics or advertising, and does not use
data to train AI models. Payments for Stoplist are handled by Shopify, which tells Stoplist the
store's plan, never its payment details.

## How long it is kept

An entry stays until the store removes it. When Shopify passes on a buyer's request to erase their
data, Stoplist deletes the entries for that buyer's email and phone and everything taken from the
orders named in the request. When a store uninstalls Stoplist, all of its data is deleted 48 hours
later, on Shopify's request. Cloudflare's own recovery copies are gone within 30 days after that.

## If you were refused at checkout

Stoplist blocks only buyers a store chose to block, or whose order got a chargeback at a store
that turned automatic blocking on. Contact the store: it can see why you are on its list and
remove you in one click. You can also write to us, and we will pass your request on to the store.

## Contact

Questions about this policy or your data:
[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
