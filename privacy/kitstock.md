---
layout: page
title: "Kitstock: Bundle Inventory — Privacy Policy"
permalink: /privacy/kitstock/
---

# Kitstock: Bundle Inventory — Privacy Policy

Last updated: 29 September 2026

Kitstock is a Shopify app, made by Spyridon Pikoulas, that keeps a store's bundle stock at what
their parts make. This policy says what it does with the store's data. Kitstock reads nothing
about the store's customers or orders.

## What Kitstock accesses and why

- **The store's name and locations** (`read_locations`): to show each bundle's stock per location.
- **The store's products and stock** (`read_products`, `read_inventory`, `write_inventory`): the
  title, SKU and stock at each location of the bundles and parts the merchant picks, and whether
  they track stock. Kitstock changes the stock of those products only, to keep the bundles and
  their parts in step.
- **The changes it made**: the product's title, the location, the figures before and after, what
  caused them, and when.
- **The store's plan**: the access token Shopify issues at install, and whether the store is on
  Pro.

## Where it is kept, and sharing

Data is stored with Cloudflare (Workers and D1), which encrypts it at rest and in transit. A
store's data is used only for that store. Kitstock does not sell or share data, uses no analytics
or advertising, and does not use data to train AI models. Payments for Kitstock are handled by
Shopify, which tells Kitstock the store's plan, never its payment details.

## How long it is kept

The log of changes keeps 30 days. When a store uninstalls Kitstock, it stops at once, and all of
the store's data is deleted 48 hours later, on Shopify's request. Cloudflare's own recovery copies
are gone within 30 days after that.

## Contact

Questions about this policy or your data:
[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
