---
layout: page
title: "How to restore tabs after a Chrome crash"
description: "Try Chrome's free tab recovery first. Then compare session managers and learn how to keep and restore a local backup of windows, pinned tabs and tab groups."
permalink: /berth/restore-tabs-after-chrome-crash/
theme: extensions
---

# How to restore tabs after a Chrome crash

If your tabs have already disappeared, try Chrome's own recovery first. A new extension cannot
give Berth a session it never saved. If you want a separate recovery copy for next time, a
session manager can save your windows and tabs before something goes wrong.

## 1. Try Chrome's free recovery

Press **Ctrl+Shift+T** on Windows or Linux, or **Command+Shift+T** on a Mac. Repeat to reopen
earlier closed tabs. These are Chrome's documented
[reopen-closed-tab shortcuts](https://support.google.com/chrome/answer/157179?hl=en).
Also check Chrome's **History** menu for a recently closed window.

For future normal restarts, Chrome's **Settings → On startup → Continue where you left off**
reopens the pages from your previous session. Google explains that setting in its
[startup-page guide](https://support.google.com/chrome/answer/95314?hl=en).
It is not a separate portable backup of your browser profile.

## 2. Choose a session manager only if you need more

There are good free alternatives. You do not need to buy Berth to save and restore tabs.

| Option | Useful for | Check before relying on it |
| --- | --- | --- |
| Chrome itself | Reopening recent tabs and continuing after a normal restart | Whether the old window is still in Chrome's recovery history |
| [Session Buddy](https://chromewebstore.google.com/detail/session-buddy-tab-bookmar/edacconmaakjimmfgnblocblbcdcpbko) | Free saved sessions, automatic tab history, collections and exports | Its local storage and export choices; retain a separate file if profile loss matters |
| [Tab Session Manager](https://chromewebstore.google.com/detail/tab-session-manager/iaiomicjabeggjcfkbimgmglanimpnae) | Free automatic session saves, named sessions and JSON import/export | Its save interval, tab-group settings and external backup settings |
| [Berth](/berth/) | Automatic checkpoints with a selective preview and optional external JSON files | Turn on external backups and check a real saved file before you need it |

Session Buddy's listing says its current local features are free. Tab Session Manager lists
automatic saves, groups and import/export. These are capable alternatives, not tools we claim
to beat on every feature. This guide is written by Berth's developer.

## 3. Keep a recovery copy in Berth

1. Install Berth from the [Chrome Web Store](https://chromewebstore.google.com/detail/berth-session-backup-reco/jdnmflebhmniemajlkianhflfnimgcmi).
   Open the windows and tabs you want to keep. Berth automatically saves checkpoints of normal
   browser windows; **Save workspace** gives a session a name you can recognize later.
2. Open **External backups** and choose **Turn on external backups**. Wait for a completed
   file. The default destination is `Downloads/Berth/berth-latest.json`; Chrome's download
   preferences can prompt for or change the destination.
3. Choose **Choose a backup to check** and select the actual JSON file from disk. Berth reports
   whether it is readable and whether its bytes match the last completed automatic write.
4. Keep your own copy somewhere you trust. A file on the same disk does not protect against
   losing that disk or computer. The JSON contains readable tab URLs and titles.

Automatic backups need Chrome running and the device awake. Writes are coalesced, normally
within about 30 seconds; sleep, disk problems and download prompts can delay them. A completed
download does not prove that another backup or cloud service has copied the file.

## 4. Restore the tabs you need

Open **Recovery**, choose a saved checkpoint and select its tabs or windows. For a named
session, open **Workspaces** and choose **Open preview**. Then choose **Restore selected**.
Berth opens new windows and leaves your current work open.

**Skip links already open** starts enabled. Leave it on to avoid reopening links you already
have, or turn it off if you deliberately want a second copy. Review the restore result; a
partial failure needs attention rather than an assumption that every tab came back.

After profile loss, use **Import backup** with a surviving JSON file, then preview and restore
the imported session. See [recovery from a surviving backup](/berth/recover-from-a-backup/) for
the standalone local reader and full steps.

Berth restores links, tab order, pins and native group structure. It does not recover unsent
forms, unsaved document edits, cookies or login sessions. Protected browser pages and incognito
windows are excluded.

Free includes three new named workspaces and up to seven days of rolling checkpoint history,
including external backups. Existing imports, exports and restores remain available at the
workspace limit. [Berth's page](/berth/) has the current Pro offer, terms and privacy policy.
