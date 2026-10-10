---
layout: page
title: "How to track a competitor's Shopify store: best sellers, new products and price changes"
description: "What any Shopify store shows the public about its best sellers, new products, prices and stock, and three ways to see what changed since you last looked."
permalink: /crate/track-competitor-shopify-store/
---

# How to track a competitor's Shopify store: best sellers, new products and price changes

Every Shopify store shows the public more than its pages suggest. Without any tool you can see
which products sell best, which are newest, and every price and whether it's in stock. What it
doesn't keep is history: to know what changed, you need your own copy from last time to compare
against. Here's both.

## Best sellers and newest products, from the address bar

A Shopify store's collections can be sorted by adding `?sort_by=` to the collection's address,
whether or not the store's sort menu offers the option. `/collections/all` is the collection of
every product:

- **Best sellers**: `https://example-store.com/collections/all?sort_by=best-selling`, ranked by
  Shopify from the store's own sales.
- **Newest first**: `https://example-store.com/collections/all?sort_by=created-descending`.
- Also `price-ascending`, `price-descending`, `title-ascending` and `created-ascending`.

The same works on any single collection (`/collections/shoes?sort_by=best-selling`). It shows the
order, not the numbers: no store shows the public how many it sold, so tools that claim a store's
revenue are estimating. It doesn't work on the few big stores with a custom ("headless")
storefront, which don't use Shopify's collection pages.

## What changed: prices, sales, stock and new products

Each standard Shopify store publishes its whole product list at `/products.json`: every variant's
price, compare-at price (the crossed-out one, so a compare-at price above the price means it's on
sale) and whether it's in stock. It doesn't publish stock quantities, only in or out. Saving that
list and comparing it with the next one shows every change in between.

### 1. Crate: open the store, click, and it tells you

[Crate](/crate/) is the Chrome extension I make for this. Install it from the
[Chrome Web Store](https://chromewebstore.google.com/detail/crate-shopify-scraper-pro/oeapbcnbebcpphjjodgdmiicincncfop)
and pin it to the toolbar. On the competitor's store, click the Crate button, keep **Whole store**
and click **Load products**. Crate saves the store's product list on your computer.

Next time you do the same, Crate compares it with the last visit and tells you, for example,
"Since your last visit on Sep 14: 3 new, 12 price changes, 2 restocked, 1 sold out". With Pro,
**Download changes** gives the list product by product: what changed, the product, its link, and the before
and after.

The count of changes is free, and so is exporting up to 100 products to a spreadsheet; Crate Pro
($12.99, paid once) lists every change and exports whole stores. Crate compares when you open it,
against your last visit, so it suits a weekly look at a few competitors. It sends no alerts, and
has no servers: the store's list and your history stay in your browser.

### 2. A Python script you run on a schedule

This does the same comparison from a terminal. Save it as `shopify_watch.py` and run
`python shopify_watch.py https://example-store.com`. The first run saves the store's variants in a
file next to it; every later run prints what changed since the one before:

```python
import json, sys, urllib.request
from pathlib import Path

store = sys.argv[1].rstrip("/")  # e.g. https://example-store.com
now, page = {}, 1
while True:
    url = f"{store}/products.json?limit=250&page={page}"
    req = urllib.request.Request(url, headers={"User-Agent": "Mozilla/5.0"})
    products = json.load(urllib.request.urlopen(req))["products"]
    for p in products:
        for v in p["variants"]:
            name = p["title"] if v["title"] == "Default Title" else f"{p['title']} ({v['title']})"
            now[str(v["id"])] = [name, v["price"], v["available"]]
    if len(products) < 250:
        break
    page += 1

saved = Path(store.split("//")[-1].replace("/", "_") + ".json")
if saved.exists():
    before = json.loads(saved.read_text(encoding="utf-8"))
    for vid, (name, price, available) in now.items():
        if vid not in before:
            print("NEW      ", name, price)
            continue
        _, old_price, was_available = before[vid]
        if price != old_price:
            print("PRICE    ", name, old_price, "->", price)
        if available != was_available:
            print("RESTOCKED" if available else "SOLD OUT ", name)
    for vid, (name, *_) in before.items():
        if vid not in now:
            print("REMOVED  ", name)
saved.write_text(json.dumps(now), encoding="utf-8")
print(f"{len(now)} variants checked, saved in {saved} for next time")
```

A run prints lines like `PRICE     Classic Tee (Large) 25.00 -> 19.00`. To have it check daily,
schedule it with Task Scheduler on Windows or cron on a Mac or Linux, sending the output to a
file. Some stores refuse requests that don't come from a browser ("HTTP Error 403"); Crate still
reads those, from the store's own tab.

### 3. A monitoring service, for alerts

If you want an email the moment a price moves, across many stores, without keeping a computer on,
that's a paid service's job. Page monitors such as [Visualping](https://visualping.io/) or
[PageCrawl](https://pagecrawl.io/) watch any page, Shopify or not. Several scrapers on
[Apify](https://apify.com/store?search=shopify%20price) read `/products.json` on a schedule and
report only the changes, charged per run or per change. Repricing apps in the Shopify App Store
go one step further and change your own prices to follow.
