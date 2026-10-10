---
layout: page
title: "How to export Google Calendar™ events to Google Sheets™"
permalink: /eventfill/export-google-calendar-to-google-sheets/
description: "Export a Google Calendar™ to a spreadsheet for timesheets and reports: one row per event, for any range of dates, with a short Apps Script or an add-on."
---

# How to export Google Calendar™ events to Google Sheets™

People export a calendar to a spreadsheet for timesheets, invoices and reports: one row per
meeting with its date, times and hours. Google Calendar™ has no direct way to do this. Here is
what it does have, and two ways that work.

## 1. Calendar's own export (not a spreadsheet)

In Google Calendar™, Settings > Import & export > Export downloads a ZIP file of your calendars as
`.ics` files. That's a calendar format, meant for another calendar app. Google Sheets™ can't open
it as a table, and it holds each calendar's whole history, with no date range. It works as a
backup, not as an export to a sheet.

## 2. A short Apps Script (free)

Apps Script can read a calendar directly. This script adds a menu that writes a calendar's events
between two dates into a sheet of their own. Open a spreadsheet, go to Extensions > Apps Script,
replace everything in `Code.gs` with the code below, and set the three lines at the top:

```js
var CALENDAR = '';  // a calendar's name, or '' for your main calendar
var FIRST_DAY = '2026-10-01';
var LAST_DAY = '2026-10-31';

function onOpen() {
  SpreadsheetApp.getUi().createMenu('Calendar')
    .addItem('Export events', 'exportEvents')
    .addToUi();
}

/** The calendar's events from FIRST_DAY to LAST_DAY into a sheet of their own. */
function exportEvents() {
  var ss = SpreadsheetApp.getActive();
  var zone = ss.getSpreadsheetTimeZone();
  var cal = CALENDAR ? CalendarApp.getCalendarsByName(CALENDAR)[0] : CalendarApp.getDefaultCalendar();
  if (!cal) throw new Error('No calendar named ' + CALENDAR);
  var from = Utilities.parseDate(FIRST_DAY, zone, 'yyyy-MM-dd');
  var to = Utilities.parseDate(LAST_DAY + ' 23:59:59', zone, 'yyyy-MM-dd HH:mm:ss');
  // All-day dates come in the script's time zone: keep them as the date they are.
  var day = function (d) { return Utilities.formatDate(d, Session.getScriptTimeZone(), 'yyyy-MM-dd'); };
  var rows = cal.getEvents(from, to).map(function (e) {
    var allDay = e.isAllDayEvent();
    return [
      e.getTitle(),
      allDay ? day(e.getAllDayStartDate()) : e.getStartTime(),
      allDay ? day(new Date(e.getAllDayEndDate().getTime() - 1)) : e.getEndTime(),
      allDay ? '' : (e.getEndTime() - e.getStartTime()) / 3600000,
      e.getLocation(),
      e.getDescription(),
      e.getGuestList().map(function (g) { return g.getEmail(); }).join(', '),
    ];
  });
  var name = cal.getName() + ' ' + FIRST_DAY + ' to ' + LAST_DAY;
  var sheet = ss.getSheetByName(name) || ss.insertSheet(name);
  sheet.clear();
  var header = ['Title', 'Start', 'End', 'Hours', 'Location', 'Description', 'Guests'];
  sheet.getRange(1, 1, rows.length + 1, header.length).setValues([header].concat(rows));
  if (rows.length) sheet.getRange(2, 2, rows.length, 2).setNumberFormats(rows.map(function (r) {
    var f = r[3] === '' ? 'yyyy-mm-dd' : 'yyyy-mm-dd hh:mm';  // all-day: no time
    return [f, f];
  }));
  sheet.setFrozenRows(1);
}
```

Save, reload the spreadsheet, and choose Calendar > Export events. The first run asks you to
authorize the script. It's your own script, so if Google warns that it hasn't verified the app,
click Advanced > Go to (your project name) (unsafe).

The sheet it makes is named after the calendar and the dates, with one row per event:

- A repeating event gives one row for each time it happens in the range.
- Timed events have their start and end in the spreadsheet's time zone (File > Settings), and
  their length in Hours, so `=SUM(D2:D200)` is the total time. All-day events have dates only and
  no hours, and a multi-day one ends on its last day.
- Start and End are real dates, so you can sort, filter and pivot on them.
- Run it again and the same sheet is rewritten with the calendar as it is now. Change the dates
  at the top and you get a new sheet beside it.

`CALENDAR` takes the name as it appears in your calendar list, so it works for calendars shared
with you too.

## 3. EventFill (free for 50 events a day)

[EventFill](/eventfill/) is the add-on I make for this, if you'd rather not keep a script. Go to
Extensions > EventFill > Open EventFill and open the Calendar to Sheet tab. Pick a calendar, the
first and last day, and, if you like, words the events must contain. Then click "Import to a new
sheet".

- The new sheet has Title, Start date, Start time, End date, End time, Duration (hours),
  Location, Description, Guests and Color, plus a link to each event in Calendar.
- Repeating events come one row per occurrence. Cancelled ones are left out.
- Times are in the spreadsheet's time zone, daylight saving included.
- It works the other way too: edit the imported rows and send them back, and only the rows you
  changed update their events. Its other tab turns any sheet's rows into events.

It reaches only the spreadsheet you open it in and your calendars' events, never your calendars'
settings or your other files. 50 events a day are free, every day. Past that, EventFill Pro is
$4.99 a month or $39 a year, with a 7-day free trial.

## Which one

For one export now and then, the script does the job. If you'd like the words filter, the
columns ready for a report, or changes sent back to the calendar, try EventFill.
