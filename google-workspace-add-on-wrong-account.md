---
layout: page
title: "Google Workspace add-on using the wrong account?"
permalink: /google-workspace-add-on-wrong-account/
description: "Open a Sheets or Slides add-on with the intended Google account, check file access and resolve common multiple-account problems."
---

# Google Workspace add-on using the wrong account?

If an add-on will not open, reports an authorization or storage error, or uses an unexpected
account, try a window signed into **only the Google account you want to use**. Google says
simultaneous sign-in to multiple accounts is unsupported for Apps Script add-ons and recommends
a single-account session or private window in its
[troubleshooting guidance](https://developers.google.com/apps-script/guides/support/troubleshooting#issues_with_multiple_google_accounts).

## Open it with one account

1. Save your work. Open a Chrome Incognito window, or your browser's equivalent private window.
2. Go to Google Drive and sign into only the account that installed and authorized the add-on.
   If you already paid, use the Google account associated with that purchase.
3. Open the spreadsheet or presentation there. Check the Google account menu in the file before
   reopening the add-on from **Extensions**. Complete Google's authorization if it is requested.
4. Check the selected source and destination before starting. If a previous attempt might have
   written results, inspect those results before repeating it, especially when creating events
   or slides.

For regular use, a separate [Chrome profile](https://support.google.com/chrome/answer/2364824?hl=en)
keeps work and personal sessions apart: choose Chrome's profile menu, then **Add Chrome profile**.
Keep just the intended Google account signed into that profile. Signing into a Google website
is separate from Chrome's optional browser sign-in and sync.

## The file opens, but the add-on still fails

In our two-account tests, opening the file as the second account did not reliably make add-on
calls use that account; Google also sometimes refused access to add-on storage. The account
shown by the file alone is therefore not proof of which account an add-on call uses. Do not
rely on editing `/u/0/` or `/u/1/` in the link to resolve this. Try the single-account route above.

If the file itself says **You need access**, first check which account it is shared with.
Ask the owner for access for that specific email if needed; an add-on installation does not
grant access to someone else's file. Google's
[file-access help](https://support.google.com/drive/answer/16722399?hl=en) explains the checks.
For editing jobs, you also need permission to edit the destination.

If the problem remains in a single-account session, it may have another cause. Work or school
administrators can restrict add-ons and connected services. Send support the add-on name,
exact error and whether the single-account test worked; omit private file contents and passwords.

This guide applies to [GeoFill](/geofill/), [ColorSum](/colorsum/), [EventFill](/eventfill/) and
[PhotoFill](/photofill/).
