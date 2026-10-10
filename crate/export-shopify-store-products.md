---
layout: page
title: "How to export products from any Shopify store to CSV"
description: "Every Shopify store publishes its product list. How to get it into a spreadsheet, or into your own store's import, for a store you own or one you don't."
permalink: /crate/export-shopify-store-products/
---

# How to export products from any Shopify store to CSV

If it's your own store, Shopify exports it for you: in the admin, go to Products, click Export,
choose All products and the CSV for Excel, Numbers or other spreadsheet programs. Up to 50
products download straight away; more arrive by email. That file is the complete one, with cost
per item and, for a store with one location, stock quantities.

For a store you don't run, such as a competitor, a supplier or a store you're researching, there's
no admin to ask. There is something almost as good: every standard Shopify store publishes its
product list at `/products.json`, for anyone. Here are three ways to turn it into a file.

## What the product list has, and what it doesn't

Each product comes with its title, description, vendor, type, tags, the dates it was created and
published, its options (size, colour and so on), and every variant with its price, compare-at
price (the crossed-out price, when it's on sale), SKU, weight, whether it's in stock, and every
image.

It has no stock quantities, barcodes, costs or sales figures, and only products the store has
published. A few stores don't serve it: a password-protected store, and big brands on a custom
("headless") storefront, which answer with an error page.

## 1. Crate, in the store's own tab

[Crate](/crate/) is the Chrome extension I make for this. Install it from the
[Chrome Web Store](https://chromewebstore.google.com/detail/crate-shopify-scraper-pro/oeapbcnbebcpphjjodgdmiicincncfop)
and pin it (the puzzle-piece icon, then the pin next to Crate). Then:

1. Open the store, or one of its collections, and click the Crate button in the toolbar.
2. Choose **Whole store** or **This collection**, and click **Load products**.
3. Pick a format and click **Download**:
   - **Spreadsheet CSV**: one row per variant, with price, compare-at price, in stock, SKU,
     vendor, type, tags, weight, image, a link to the variant and the dates. Opens in Excel and
     Google Sheets.
   - **Shopify import CSV**: every product with its variants, options and images, in the columns
     of Shopify's own product import (Products > Import in your admin).
   - **JSON**: the store's product data as it publishes it.
   - **Product links**: one URL per line.

Up to 100 products from any store or collection is free; Crate Pro ($12.99, paid once) exports
whole stores of any size. Crate only runs on the tab you click it on, and only reads the list the
store publishes. It also remembers the store, and next time tells you what changed: new
products, price changes, restocks. That part is in
[How to track a competitor's Shopify store](/crate/track-competitor-shopify-store/).

## 2. By hand, for a small store

Add `/products.json?limit=250` to the store's address, for example
`https://example-store.com/products.json?limit=250`, and your browser shows the first 250 products
as JSON. For the next 250, add `&page=2`, and so on until a page comes back with fewer. Paste the
JSON into any "JSON to CSV" converter, and flatten the variants yourself: each product holds its
variants as a list, which converters handle in different ways. This works for a quick look at a
small store; for anything bigger, use Crate or the script below.

## 3. A Python script

This saves a spreadsheet with one row per variant. Save it as `shopify_export.py`, then run
`python shopify_export.py https://example-store.com`:

```python
import csv, json, sys, urllib.request

store = sys.argv[1].rstrip("/")  # e.g. https://example-store.com
rows, page = [], 1
while True:
    url = f"{store}/products.json?limit=250&page={page}"
    req = urllib.request.Request(url, headers={"User-Agent": "Mozilla/5.0"})
    products = json.load(urllib.request.urlopen(req))["products"]
    for p in products:
        for v in p["variants"]:
            rows.append({
                "title": p["title"], "variant": v["title"], "sku": v["sku"],
                "price": v["price"], "compare_at_price": v["compare_at_price"],
                "available": v["available"], "vendor": p["vendor"],
                "type": p["product_type"], "published_at": p["published_at"],
                "url": f"{store}/products/{p['handle']}?variant={v['id']}",
            })
    if len(products) < 250:
        break
    page += 1

with open("products.csv", "w", newline="", encoding="utf-8-sig") as f:
    w = csv.DictWriter(f, fieldnames=list(rows[0]))
    w.writeheader()
    w.writerows(rows)
print(f"{len(rows)} variants saved to products.csv")
```

A store with 1,000 products takes a few seconds. Products without options show the variant as
"Default Title", which is Shopify's name for it. Some stores refuse requests that don't come from a
browser (the script then stops with "HTTP Error 403"); for those, use Crate, which runs in the
store's own tab.

## Copying products into your own store

To move products into your own Shopify store, Crate's Shopify import CSV goes straight into
Products > Import in your admin, with every variant, option, price, compare-at price, image, tag,
type and vendor; the images are links, which Shopify downloads during the import. Sold-out
variants come in sold out, and the rest untracked, since a store doesn't publish how many it
has. Descriptions and photos belong to whoever made them, though: copy them from a store only if
it's yours or the owner has said yes, as a supplier or wholesaler often will. Between two stores
you own, Shopify's own export and import is the better route, since it carries stock levels and
SEO fields too.
