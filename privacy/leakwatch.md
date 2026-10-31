---
layout: page
title: "LeakWatch: Discount Code Guard — Privacy Policy"
permalink: /privacy/leakwatch/
---

# LeakWatch: Discount Code Guard — Privacy Policy

Last updated: 27 September 2026

LeakWatch is a Shopify app, made by Spyridon Pikoulas, that finds a store's discount codes on
coupon sites. This policy says what it does with the store's data. LeakWatch reads nothing about
the store's customers or orders.

## What LeakWatch accesses and why

- **The store's discount codes** (scopes `read_discounts`, `write_discounts`): each active code,
  its discount's title, how many codes the discount has and how many times each code has been
  used. LeakWatch looks for these codes on coupon sites, and follows their daily use to flag a
  sudden jump. When the store asks, or has automatic shut-off on, LeakWatch adds a new code to a
  discount, deletes a leaked code or ends a discount.
- **The store's primary web address and name**, to find the store's pages on coupon sites.
- **Coupon-site pages**: LeakWatch fetches public pages about the store from coupon sites, and any
  page the store adds, and records which of the store's codes appeared on which page and when.
- **The store's plan and settings**: the access token Shopify issues at install, whether
  automatic shut-off is on, and the codes marked as shared on purpose.

## Where it is kept, and sharing

Data is stored with Cloudflare (Workers and D1), which encrypts it at rest and in transit. A
store's codes are used only for that store; they are never sent to coupon sites or anyone else,
since LeakWatch fetches coupon-site pages and searches them itself. LeakWatch does not sell or
share data, uses no analytics or advertising, and does not use data to train AI models. Payments
for LeakWatch are handled by Shopify, which tells LeakWatch the store's plan, never its payment
details.

## How long it is kept

Codes are refreshed daily; a code deleted from the store is dropped at the next refresh. Daily use
counts and the record of where codes were found stay while the app is installed. When a store
uninstalls LeakWatch, all of its data is deleted 48 hours later, on Shopify's request.
Cloudflare's own recovery copies are gone within 30 days after that.

## Contact

Questions about this policy or your data:
[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
