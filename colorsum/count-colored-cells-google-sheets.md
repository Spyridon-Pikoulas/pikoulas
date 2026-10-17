---
layout: page
title: "How to count and sum colored cells in Google Sheets™"
permalink: /colorsum/count-colored-cells-google-sheets/
---

# How to count and sum colored cells in Google Sheets™

Google Sheets™ has no COUNTIF for colors. None of its built-in functions can read a cell's fill or
text color. Here are three ways that do work, from no setup to no upkeep.

## 1. Filter by color and SUBTOTAL (no setup, one color at a time)

Click a cell in your table, then Data > Create a filter. Click the filter icon in the colored
column's header, then Filter by color > Fill Color, and pick the color. Under the table, put:

- `=SUBTOTAL(103, B2:B200)`: how many visible cells aren't empty
- `=SUBTOTAL(109, B2:B200)`: the sum of the visible numbers

SUBTOTAL ignores the rows the filter hides, so both follow when you pick another color. Leave an
empty row between the table and these formulas, or the filter takes them in and hides them with
the rest. Filter by color > Text Color works the same way for font colors.

## 2. A custom function (free, a few minutes)

Go to Extensions > Apps Script, replace everything in `Code.gs` with the code below, and save:

```js
/** =SUMBYCOLOR("B2:B50", "#f4cccc"): sum of the cells in the range with that fill. */
function SUMBYCOLOR(a1, color) {
  var range = SpreadsheetApp.getActiveSheet().getRange(a1);
  color = color.toLowerCase();
  var fills = range.getBackgrounds(), values = range.getValues(), sum = 0;
  for (var i = 0; i < values.length; i++)
    for (var j = 0; j < values[i].length; j++)
      if (fills[i][j] === color && typeof values[i][j] === 'number') sum += values[i][j];
  return sum;
}

/** =COUNTBYCOLOR("B2:B200", "#cccccc") */
function COUNTBYCOLOR(a1, color) {
  var fills = SpreadsheetApp.getActiveSheet().getRange(a1).getBackgrounds();
  return fills.flat().filter(function (c) { return c === color.toLowerCase(); }).length;
}

/** =FILLOF("B2"): the fill color code of a cell, to use in the two above. */
function FILLOF(a1) {
  return SpreadsheetApp.getActiveSheet().getRange(a1).getBackground();
}
```

Then, in the sheet:

- `=COUNTBYCOLOR("B2:B200", "#f4cccc")` counts the cells filled with that color, text ones included.
- `=SUMBYCOLOR("B2:B200", "#f4cccc")` adds up the numbers among them.
- `=FILLOF("B2")` shows a cell's color code, so you know what to put in the two above. For
  example, the palette's "light red 3" is `#f4cccc`.

The limits:

- The range has to be in quotes and on the same sheet as the formula. A custom function receives
  the cells' values, not the cells, so it has to look the range up itself. That also means the
  range doesn't adjust when you copy the formula or insert rows.
- Recoloring a cell leaves the total as it was, because Sheets™ doesn't recalculate anything when
  only a color changes. The next section fixes that.

### Update the totals when a color changes

A color change doesn't recalculate formulas, but it does fire a spreadsheet's "On change"
trigger. So let the trigger change a cell that the formulas depend on:

1. Add a sheet named `Settings`. The script writes the time into its cell A1.
2. Add this function to the script and save:

   ```js
   function onFormatChange(e) {
     if (e.changeType === 'FORMAT') SpreadsheetApp.getActive().getRange('Settings!A1').setValue(new Date());
   }
   ```

3. In Apps Script, open Triggers (the clock icon on the left) > Add Trigger. Choose the function
   `onFormatChange`, event source "From spreadsheet", event type "On change", then Save and
   authorize it.
4. Give each formula that cell as an extra argument:
   `=SUMBYCOLOR("B2:B200", "#f4cccc", Settings!A1)`. The function ignores the argument, but when
   the trigger writes into Settings!A1, every formula that mentions it recalculates.

Now a recolored cell changes the totals a few seconds later. The trigger fires on every format
change (fonts and borders too), which does no harm: it only causes a recalculation.

## 3. ColorSum (free for 10 counts a day)

[ColorSum](/colorsum/) is the add-on I make for this, if you'd rather not keep a script. Select
the cells, go to Extensions > ColorSum > Open ColorSum, and click "Count the selected cells". It
lists every fill color (or text color) in the selection with its count, sum and average. That
count is free 10 times a day.

ColorSum Pro ($3.99 a month) adds formulas:

- Click a color, pick an empty cell and choose "Insert in the selected cell" to get
  `=SUMBYCOLOR(C2:C200, D1)`. It uses normal references that you can copy down and that adjust
  like any formula's, and D1 is any cell that has the color. You can also give a code like
  `"#f4cccc"`.
- `COUNTBYCOLOR`, `AVERAGEBYCOLOR`, `MAXBYCOLOR` and `MINBYCOLOR` work the same way, each has a
  text-color version (`COUNTBYFONTCOLOR`…), and `=COLOROF(A2)` gives a cell's color code.
- Tick "Refresh them when a color changes" and the totals follow your coloring, with no trigger
  to set up.

It has access only to the spreadsheet you open it in.

## Whichever you choose

Colors that come from conditional formatting are invisible to every script and add-on, because
they read only the colors you applied yourself. For those cells, count the rule's condition with
COUNTIF or SUMIF instead: it picks out the same cells.
