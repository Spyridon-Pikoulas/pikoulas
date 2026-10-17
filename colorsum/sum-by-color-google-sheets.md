---
layout: page
title: "How to sum by color in Google Sheets™, including another column"
permalink: /colorsum/sum-by-color-google-sheets/
description: "SUMIF by cell color in Google Sheets™: add up a column by the fill color of its cells or of another column, total each color, with a filter, a short script or an add-on."
---

# How to sum by color in Google Sheets™, including another column

Google Sheets™ has no SUMIF for colors, because no built-in function can read a cell's color. The
colored cells are often not even the numbers you want to add. A name or a status is colored, and
the amount sits in another column. The three ways below handle both cases.

## 1. Filter by color and SUBTOTAL (no setup, one color at a time)

Click a cell in your table, then Data > Create a filter. Click the filter icon in the colored
column's header, then Filter by color > Fill Color, and pick the color. Under the table, put:

```
=SUBTOTAL(109, C2:C200)
```

SUBTOTAL adds only the rows the filter shows, so this works whichever column is colored: filter
on the colored names in A and sum the amounts in C. Pick another color and the total follows.
Leave an empty row between the table and the formula, or the filter hides the formula with the
rest of the rows.

## 2. A helper column of color codes, then SUMIF (free, a few minutes)

A short custom function can turn the colors into text, a color code per cell. After that, the
usual SUMIF, QUERY and pivot tables can work with them. Go to Extensions > Apps Script, replace
everything in `Code.gs` with this, and save:

```js
/** =FILLS("A2:A200"): the fill color code of each cell in the range, as a column. */
function FILLS(a1) {
  return SpreadsheetApp.getActiveSheet().getRange(a1).getBackgrounds();
}
```

Then, if the colored cells are in A2:A200 and the amounts in C2:C200:

1. In the first cell of an empty column, say E2, type `=FILLS("A2:A200")`. The column fills with
   each cell's color code: `#f4cccc` for the palette's light red 3, `#ffffff` for no fill.
2. Sum one color: `=SUMIF(E2:E200, "#f4cccc", C2:C200)`.
3. Total every color at once:

   ```
   =QUERY({E2:E200, C2:C200}, "select Col1, sum(Col2) group by Col1 label sum(Col2) ''", 0)
   ```

   It lists each color code once, with its total beside it. A pivot table on columns E and C
   does the same.

The SUMIF and QUERY ranges must be the same height as the FILLS range. To find a color's code,
look in the helper column next to a cell that has it. If the numbers are colored themselves,
use `=FILLS("C2:C200")` and sum the same column.

The limits are those of any custom function:

- The range is in quotes, so it doesn't adjust when you insert rows or copy the formula.
- Sheets™ doesn't recalculate anything when only a color changes, so the codes, and the totals
  with them, keep the old colors until something else recalculates them.
  [How to count and sum colored cells](/colorsum/count-colored-cells-google-sheets/#update-the-totals-when-a-color-changes)
  has a trigger that fixes that. Give FILLS the extra argument it describes:
  `=FILLS("A2:A200", Settings!A1)`.

## 3. ColorSum (free for 10 counts a day)

[ColorSum](/colorsum/) is the add-on I make for this, if you'd rather not keep a script.

- **When the numbers are colored**: select them, go to Extensions > ColorSum > Open ColorSum, and
  click "Count the selected cells". It lists every fill color (or text color) in the selection
  with its count, sum and average. That count is free 10 times a day.
- **When another column is colored** (ColorSum Pro, $3.99 a month or $29 a year, 7 days free):
  `=SUMBYCOLOR(A2:A200, D1, C2:C200)` adds the amounts in C on the rows where A has the color of
  D1. D1 can be any cell with that color, or a code like `"#f4cccc"`. The ranges are plain
  references, so they adjust like any formula's when you copy it or insert rows.
  `AVERAGEBYCOLOR`, `MAXBYCOLOR` and `MINBYCOLOR` take the same third range, and each has a
  text-color version (`SUMBYFONTCOLOR`…).
- Tick "Refresh them when a color changes" in the sidebar, and the totals update when you recolor
  a cell, with no trigger to set up.

It has access only to the spreadsheet you open it in.

## Whichever you choose

Colors from conditional formatting are invisible to every script and add-on. They read only the
colors you applied yourself. If a rule colors the cells, sum by the rule's condition instead,
with SUMIF or SUMIFS on the same column the rule checks.
