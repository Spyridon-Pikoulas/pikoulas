---
layout: page
title: "Stockfeed: Supplier Stock Sync — Privacy Policy"
permalink: /privacy/stockfeed/
---

# Stockfeed: Supplier Stock Sync — Privacy Policy

Last updated: 27 September 2026

Stockfeed is a Shopify app, made by Spyridon Pikoulas, that sets a store's stock from its
suppliers' stock files. This policy says what it does with the store's data. Stockfeed reads
nothing about the store's customers or orders.

## What Stockfeed accesses and why

- **The store's products and stock** (scopes `read_products`, `write_products`,
  `read_inventory`, `write_inventory`): each variant's SKU, name, vendor and price, and its stock at
  the location a feed uses. Stockfeed compares them with the supplier's file and sets the stock,
  and the price when the store asks it to.
- **The store's locations** (`read_locations`): their names, to choose where a feed sets stock.
- **The supplier files**: Stockfeed downloads each file from the address the store gives it. While
  a run is under way it keeps the file's SKUs, stock and prices; once the run is done they are
  deleted.
- **What each run did**: when it ran, how many rows it read and matched, and up to 200 changes it
  made or would make (variant name, SKU, before and after), so the store can see them.
- **The store's plan and settings**: the access token Shopify issues at install, and each feed's
  name, file address and settings.

## Where it is kept, and sharing

Data is stored with Cloudflare (Workers and D1), which encrypts it at rest and in transit. A
store's data is used only for that store. Stockfeed does not sell or share data, uses no
analytics or advertising, and does not use data to train AI models. It sends nothing to the
suppliers: it only downloads their files. Payments for Stockfeed are handled by Shopify, which
tells Stockfeed the store's plan, never its payment details.

## How long it is kept

A feed's last 10 runs and their changes are kept; older ones are deleted. A deleted feed's runs go
with it. When a store uninstalls Stockfeed, all of its data is deleted 48 hours later, on
Shopify's request. Cloudflare's own recovery copies are gone within 30 days after that.

## Contact

Questions about this policy or your data:
[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
