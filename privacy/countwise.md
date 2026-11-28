---
layout: page
title: "Countwise: Inventory Count — Privacy Policy"
permalink: /privacy/countwise/
---

# Countwise: Inventory Count — Privacy Policy

Last updated: 28 September 2026

Countwise is a Shopify app, made by Spyridon Pikoulas, for counting a store's stock and correcting
its inventory. This policy says what it does with the store's data. Countwise reads nothing about
the store's customers or orders.

## What Countwise accesses and why

- **The store's products and stock** (scopes `read_products`, `read_inventory`,
  `write_inventory`): each variant's name, SKU, barcode and unit cost, and its stock at the
  location being counted. Countwise lists them in a count, compares them with what is scanned and,
  when the store applies the count, adjusts the stock.
- **The store's locations** (`read_locations`): their names, to choose the location to count.
- **Each count**: its name, location and products, every scan (the product, the quantity and the
  time) and what applying it changed. Countwise doesn't record who scanned.
- **The store's plan**: the access token Shopify issues at install, and whether the store is on
  Pro.

## Where it is kept, and sharing

Data is stored with Cloudflare (Workers and D1), which encrypts it at rest and in transit. A
store's data is used only for that store. Countwise does not sell or share data, uses no analytics
or advertising, and does not use data to train AI models. Payments for Countwise are handled by
Shopify, which tells Countwise the store's plan, never its payment details.

## How long it is kept

A count and its scans are kept until the store deletes it in the app. When a store uninstalls
Countwise, all of its data is deleted 48 hours later, on Shopify's request. Cloudflare's own
recovery copies are gone within 30 days after that.

## Contact

Questions about this policy or your data:
[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
