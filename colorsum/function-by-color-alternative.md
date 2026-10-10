---
layout: page
title: "Function by Color and Custom Count and Sum alternatives for Google Sheets™"
permalink: /colorsum/function-by-color-alternative/
description: "Function by Color stopped being free and Custom Count and Sum broke for a while. Free and paid ways to count and sum cells by color in Google Sheets™ today."
---

# Function by Color and Custom Count and Sum alternatives for Google Sheets™

Most people who count or sum cells by color in Google Sheets™ use one of a few add-ons. As of
September 2026, their Google Workspace™ Marketplace listings say:

- **Function by Color** (Ablebits, about 790,000 installs, rated 3.3): a 30-day trial, then
  paid, and it asks for access to all your spreadsheets. Reviewers say the results need a manual
  refresh, that it "asks me to pay every time I open a sheet", and that copied files lose the
  functions. Ablebits' Power Tools has the same functions inside a larger paid suite.
- **Custom Count and Sum** (about 300,000 installs, rated 3.1): it was free. In May and June 2026,
  reviews said its formulas showed "#ERROR" and their writers were "looking for a replacement".
  It was updated in September 2026 and is now freemium. Its ranges are typed in quotes, which one
  reviewer called "a deal breaker".
- **Function by color** (a different add-on, about 160,000 installs): a trial, then paid.
  Reviewers say it "won't automatically update the count".

If one of these stopped working for you or asks for more than you want to pay, these are the
other ways.

## 1. A filter (free, nothing to install)

Data > Create a filter, then the filter icon > Filter by color, and `=SUBTOTAL(109, C2:C200)`
under the table sums only the rows that show. It does one color at a time, but nothing breaks.

## 2. Your own script (free, a few minutes)

A few lines of Apps Script give you `=SUMBYCOLOR` and `=COUNTBYCOLOR`, and a helper column of color
codes lets SUMIF and QUERY total by color. A script you keep yourself has no trial to run out and
no service behind it that can shut down. The code and its limits are in two guides:

- [How to count and sum colored cells in Google Sheets™](/colorsum/count-colored-cells-google-sheets/),
  including a trigger that updates the totals when a color changes
- [How to sum by color, including another column](/colorsum/sum-by-color-google-sheets/), with
  per-color totals

Like Custom Count and Sum, a custom function needs its range in quotes.

## 3. ColorSum (free for 10 counts a day, $3.99 a month for the formulas)

[ColorSum](/colorsum/) is the add-on I make for this. I built it for what the reviews above ask
for:

- **Plain references**: `=SUMBYCOLOR(A2:A200, D1)`, with no quotes. The range adjusts when you
  copy the formula or insert rows. D1 is any cell with the color, or a code like `"#f4cccc"`.
- **Totals that follow your coloring**: tick "Refresh them when a color changes" and recoloring a
  cell updates the formulas, with no refresh to click.
- **Narrow access**: it reaches only the spreadsheet you open it in, never your other files.
- **A free tier that stays**: the sidebar's count is free 10 times a day, every day. Select the
  cells and click "Count the selected cells" for each color's count, sum and average.

The formulas are part of ColorSum Pro: `COUNTBYCOLOR`, `SUMBYCOLOR` (with an optional range to
sum another column), `AVERAGEBYCOLOR`, `MAXBYCOLOR`, `MINBYCOLOR`, their text-color versions
(`COUNTBYFONTCOLOR`…), and `COLOROF` for a cell's color code. Pro is $3.99 a month or $29 a year,
with a 7-day free trial, and you can cancel from the sidebar.

What it doesn't do: anything besides colors. If you use Power Tools for its other tools, ColorSum
doesn't replace those.

## Whichever you choose

No add-on or script can see colors that come from conditional formatting. Sheets™ shows them
only to people. For those cells, count or sum by the rule's own condition with COUNTIF or SUMIF.
