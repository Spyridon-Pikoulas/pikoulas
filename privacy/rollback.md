---
layout: page
title: "Rollback: Backup & Undo — Privacy Policy"
permalink: /privacy/rollback/
---

# Rollback: Backup & Undo — Privacy Policy

Last updated: 27 September 2026

Rollback is a Shopify app, made by Spyridon Pikoulas, that backs up a store's products and
collections and restores them. This policy says what it does with data.

## What Rollback accesses and why

- **Products, collections, inventory and locations** (Shopify scopes `read_products`,
  `write_products`, `read_inventory`, `write_inventory`, `read_locations`). Rollback copies each
  product and collection when it changes, with its stock per location and a copy of its images,
  and writes a version back when you restore it.
- **Sales channels** (`read_publications`, `write_publications`). Rollback notes which sales
  channels each product and collection is on, and puts a restored one back on them.
- **Your store's address and plan.** Shopify gives Rollback an access token for your store at
  install, and tells it which plan you are on.

Rollback does not access orders, customers or payment details.

## Where it is kept

Backups are stored with Cloudflare (Workers, D1 and R2), which encrypts them at rest and in transit.
They are used only to show your history and to restore your store. Rollback uses no analytics and
no advertising, and does not sell, share or use your data for anything else, including training AI
models.

Payments are handled by Shopify: Rollback sees which plan you are on, never your payment details.

## How long it is kept

Each change is kept for your plan's history period (14 days on Free, 90 days on Starter, one year
on Growth and Scale) and then deleted; the copies of your product images are kept until you
uninstall, so that any version in the history can be restored with them. When you uninstall Rollback it stops backing up; 48 hours
later Shopify asks it to erase your store's data, and every backup, change record and token is
deleted. Cloudflare's own recovery copies are gone within 30 days after that. To have your data
deleted sooner, write to us.

## Contact

Questions about this policy or your data:
[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).
