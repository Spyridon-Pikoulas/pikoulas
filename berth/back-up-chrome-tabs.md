---
layout: page
title: "How to back up Chrome tabs to a file and restore them"
description: "Chrome can save your open tabs as bookmarks and export them for free. Here is how, the free session managers, and how to keep an automatic backup file with Berth."
permalink: /berth/back-up-chrome-tabs/
theme: extensions
---

# How to back up Chrome tabs to a file and restore them

Chrome keeps your tabs inside its own profile. To have a copy you can move to another computer or
keep after the profile is gone, save the tabs to a file. Chrome can do that for free by hand. A
session manager is worth adding only if you want it done for you, with windows and tab groups kept.

## 1. Use Chrome's bookmarks

1. Press **Ctrl+Shift+D** on Windows or Linux, or **Command+Shift+D** on a Mac. Chrome saves the
   window's open tabs as bookmarks in a new folder; name it with the date. These are Chrome's
   documented [shortcuts](https://support.google.com/chrome/answer/157179?hl=en). Repeat in each
   window you want to keep.
2. Open the Bookmark Manager with **Ctrl+Shift+O**, or **Command+Option+B** on a Mac. From the menu
   at its top, choose **Export bookmarks**. Chrome
   [saves them as an HTML file](https://support.google.com/chrome/answer/96816?hl=en) that any
   browser can import.
3. To restore, import the file in Chrome under **Bookmarks and lists → Import bookmarks and
   settings**, or in another browser. Right-click the folder and choose **Open all**.

This is a snapshot of the moment you pressed the keys, and it keeps links, not your windows, pinned
tabs or tab groups. If you sign in to Chrome with sync on, your bookmarks and tab groups also reach
your other devices, but that copy lives in your Google Account rather than in a file you hold. Chrome's
own copy of your groups is covered in [how to save Chrome tab groups](/berth/save-chrome-tab-groups/).

## 2. Check the free session managers

You do not need to buy Berth to back up your tabs.

| Option | Useful for | Check before relying on it |
| --- | --- | --- |
| Chrome's bookmarks | A free file of links you can open in any browser | By hand each time; no windows, pins or groups |
| [Session Buddy](https://chromewebstore.google.com/detail/session-buddy-tab-bookmar/edacconmaakjimmfgnblocblbcdcpbko) | Saving sessions in one click, automatic tab history, export in formats such as JSON, CSV, HTML and plain text | Its data stays inside the browser until you export it |
| [Tab Session Manager](https://chromewebstore.google.com/detail/tab-session-manager/iaiomicjabeggjcfkbimgmglanimpnae) | Automatic saves at intervals and on window close, named sessions, import and export, cloud sync | Its save interval and its tab group setting |
| [Berth](/berth/) | An automatic JSON backup file in your Downloads folder, restored by preview | Turn on external backups and check a real saved file |

These descriptions come from each publisher's store listing, checked on 8 November 2026. Both are
free and capable; we do not claim to beat them on every feature. This guide is written by Berth's
developer.

## 3. Keep an automatic backup file with Berth

1. Install Berth from the [Chrome Web Store](https://chromewebstore.google.com/detail/berth-auto-tab-backup-ses/jdnmflebhmniemajlkianhflfnimgcmi).
   It saves checkpoints of your normal windows as they change: tabs in order, pinned tabs and tab
   groups with their names and colours.
2. Open **External backups** and choose **Turn on external backups**. Berth writes
   `berth-latest.json` to a `Berth` folder in your downloads, or the **Downloads subfolder** you set,
   and keeps at most one dated copy an hour. Chrome's download settings can ask where to save or move
   the file; Berth shows where it went.
3. Choose **Choose a backup to check** and select the file from disk. Berth reports whether it is
   readable and matches the last completed write.
4. Copy the folder to a drive or backup service you trust. A file on the same disk does not survive
   losing that disk. The JSON holds readable links and page titles.

**Back up now** writes the file at once, and **Download a backup** saves every checkpoint and
workspace as a single file. To share or move just part of a session, open its preview, tick the
tabs and choose **Export**.

Backups are written only while Chrome is running and the device is awake, normally within about 30
seconds of a change. Incognito windows and Chrome's own pages are left out. A download marked
complete has not necessarily been copied by any other backup or sync service.

## 4. Restore on this computer or another

1. Install Berth, open it and choose **Import backup**. Select a Berth file or a Tab Session Manager
   JSON file.
2. Open the imported session's preview and tick the windows or tabs you need.
3. Choose **Restore selected**. Berth opens new windows beside your current ones, with pins and
   groups rebuilt. **Skip links already open** avoids duplicates.

Without Berth, the recovery reader opens the file in any browser and lists its links; save it
beforehand with **Download recovery reader** in **External backups**. [Recovering from a backup](/berth/recover-from-a-backup/)
has the full steps.

Berth restores links, their order, pins, windows and groups. It does not bring back unsent forms,
unsaved document edits, cookies or logins, so you may need to sign in again.

## What is free

Automatic backups, importing, exporting and restoring are free. Free keeps seven days of checkpoint
history, 24 dated backup copies and three named workspaces you create. Berth Pro raises those limits
for **$12.99 once**. [Berth's page](/berth/) has the terms, refunds and privacy policy.
