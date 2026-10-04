---
layout: page
title: "Twinstock: Multi Store Sync — Privacy Policy"
permalink: /privacy/twinstock/
---

# Twinstock: Multi Store Sync — Privacy Policy

Last updated: 28 September 2026

Twinstock is a Shopify app, made by Spyridon Pikoulas, that keeps the stock of a merchant's own
stores in step. This policy says what it does with the stores' data. Twinstock reads nothing about
the stores' customers or orders.

## What Twinstock accesses and why

- **The store's name and locations** (`read_locations`): the name to show which stores are
  linked, the locations to choose the one whose stock takes part.
- **The store's products and stock** (`read_products`, `read_inventory`, `write_inventory`): each
  variant's title, SKU and stock at that location, and whether it tracks stock. Twinstock compares
  them with the linked stores' and changes the stock to pass on what changed in another store.
- **The changes it passed on**: the SKU, the product's title, the store it came from, the figures
  before and after, and when.
- **The store's plan**: the access token Shopify issues at install, and whether the store is on
  Pro.

The stores in a link see each other's store and location names, and the titles, SKUs and stock of
the products they share, in the app. A store joins a link only with a code made in a store
already in it.

## Where it is kept, and sharing

Data is stored with Cloudflare (Workers and D1), which encrypts it at rest and in transit. A
store's data is used only for that store and the stores it is linked with. Twinstock does not sell
or share data, uses no analytics or advertising, and does not use data to train AI models.
Payments for Twinstock are handled by Shopify, which tells Twinstock the store's plan, never its
payment details.

## How long it is kept

The log of changes keeps 30 days. A store's products and stock are deleted from Twinstock when it
leaves its link. When a store uninstalls Twinstock, it leaves its link at once, and all of its data
is deleted 48 hours later, on Shopify's request. Cloudflare's own recovery copies are gone within
30 days after that.

## Contact

Questions about this policy or your data:
[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
