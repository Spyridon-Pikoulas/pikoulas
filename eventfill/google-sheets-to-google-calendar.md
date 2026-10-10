---
layout: page
title: "Google Sheets™ to Google Calendar™: create events without duplicates"
permalink: /eventfill/google-sheets-to-google-calendar/
---

# Create Google Calendar™ events from a Google Sheet, without duplicates

People keep all kinds of schedules in spreadsheets (shifts, class timetables, content calendars,
bookings) and want them on Google Calendar™. There are three ways to get them there. Watch out for
one thing: a sheet-to-calendar script that doesn't remember which events it made creates every
event again each time it runs.

## 1. Import a CSV file (no setup, one time)

Put the events in a sheet under these headers, in English: `Subject`, `Start Date`, `Start Time`,
`End Date`, `End Time`, `All Day Event`, `Description`, `Location`. Only the first two are
required. Dates must read like 05/30/2026 and times like 10:00 AM. Then:

1. In Sheets™: File > Download > Comma Separated Values (.csv). This saves the sheet you're on.
2. In Google Calendar™: the gear icon > Settings > Import & export. Choose the file and a calendar,
   then click Import.

This works once. The file has no event IDs, so importing it again adds every event a second time,
and later edits to the sheet never reach the calendar.

## 2. An Apps Script that remembers its events (free, a few minutes)

This script makes one event per row and writes the event's ID into the row. On the next run, a row
that has an ID updates its event instead of creating another one.

Lay out the sheet with a header row and:

- **A**: the title
- **B**: the start, as a date and time, or just a date for an all-day event
- **C**: the end, as a date and time. Leave it empty for an all-day event.
- **D**: leave it empty. The script writes each event's ID here.

B and C have to be real dates (Format > Number > Date time), not text that only looks like one.
The script skips a row whose start is text, and it treats a text end as no end.

Go to Extensions > Apps Script, replace everything in `Code.gs` with the code below, and save:

```js
function onOpen() {
  SpreadsheetApp.getUi().createMenu('Calendar')
    .addItem('Sync events', 'syncEvents')
    .addToUi();
}

/** Title in A, start in B, end in C (empty for an all-day event), D left to the script. */
function syncEvents() {
  var sheet = SpreadsheetApp.getActiveSheet();
  var zone = SpreadsheetApp.getActive().getSpreadsheetTimeZone();
  var cal = CalendarApp.getDefaultCalendar();
  var rows = sheet.getDataRange().getValues();
  for (var i = 1; i < rows.length; i++) {
    var title = rows[i][0], start = rows[i][1], end = rows[i][2], id = rows[i][3];
    if (!title || !(start instanceof Date)) continue;
    var timed = end instanceof Date;
    // Calendar reads an all-day date in the script's time zone: use the date the sheet shows.
    var ymd = Utilities.formatDate(start, zone, 'yyyy-M-d').split('-');
    var day = new Date(ymd[0], ymd[1] - 1, ymd[2]);
    var event = id && cal.getEventById(id);
    if (event) {
      event.setTitle(title);
      if (timed) event.setTime(start, end);
      else event.setAllDayDate(day);
    } else {
      event = timed ? cal.createEvent(title, start, end) : cal.createAllDayEvent(title, day);
      sheet.getRange(i + 1, 4).setValue(event.getId());
    }
  }
}
```

Reload the spreadsheet and a Calendar menu appears; choose Calendar > Sync events. The first run
asks you to authorize the script. It's your own script, so if Google warns that it hasn't verified
the app, click Advanced > Go to (your project name) (unsafe).

What to know:

- Events go to your main calendar. To use another one, replace `CalendarApp.getDefaultCalendar()`
  with `CalendarApp.getCalendarById('...')`. The ID is in Google Calendar™ under the calendar's
  Settings and sharing > Integrate calendar.
- Run it as often as you like. Rows with an ID update their event's title and times, and new rows
  get an event.
- Times are read in the spreadsheet's time zone (File > Settings). 9:00 in the sheet is 9:00 on a
  calendar in the same zone and the converted time on a calendar in another zone, across
  daylight-saving changes too. A shift that ends after midnight just needs the next day's date in
  its end.
- The script doesn't handle all-day dates the obvious way, which is why it has the lines with
  `ymd`. Calendar reads an all-day event's date in the script's own time zone, which isn't
  always the spreadsheet's. Without those lines, a date-only row can land the day before.
- If you delete an event in Calendar, clear its ID in column D as well. Otherwise the row keeps
  pointing at the deleted event and nothing is recreated. Once the ID is cleared, the next run
  makes a new event. Deleting a row leaves its event on the calendar.
- To sort, sort the whole table, never column D on its own.

## 3. EventFill (free for 50 events a day)

[EventFill](/eventfill/) is the add-on I make for this, if you'd rather not keep a script. Open it
from Extensions > EventFill > Open EventFill. Pick the title and date columns (and times, end
dates, description, location, guests and color if you have them), pick a calendar, and click Add
to Calendar:

- A date alone makes an all-day event (with an end date, a multi-day one). A date and a time make
  a timed event. Shifts past midnight work.
- Each row gets a linked "Calendar event" cell. When you run it again, changed rows update their
  events and unchanged ones are skipped, so nothing is duplicated.
- A "Calendar sync" column shows what happened to each row, or what to fix when a row can't be
  sent.
- Times are read in the spreadsheet's time zone, daylight saving included.
- It also works the other way: its Calendar to Sheet tab puts a calendar's events for any range
  of days into a new sheet, for timesheets and reports. Edit them there and send the changes back.

It reaches only the spreadsheet you open it in and your calendars' events, never your calendars'
settings or your other files. 50 events a day are free, every day. Past that, EventFill Pro is
$4.99 a month.

## Which one

For a one-off list that won't change, use the CSV import. For a sheet you keep editing, use the
script or EventFill, since both update events instead of doubling them.
