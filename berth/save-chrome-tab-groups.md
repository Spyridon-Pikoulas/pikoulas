---
layout: page
title: "How to save Chrome tab groups and get them back"
description: "Chrome already keeps closed tab groups for free. Here is where to find them, where that falls short, the free session managers, and how Berth keeps groups in a backup file."
permalink: /berth/save-chrome-tab-groups/
theme: extensions
---

# How to save Chrome tab groups and get them back

Chrome saves tab groups for you, so start there. A backup outside Chrome is worth having only for
what Chrome's own copy does not cover: a group deleted by mistake, a lost profile, or a move to a
computer that is not signed in to your account.

## 1. Use Chrome's saved groups

From Google's [tab groups help](https://support.google.com/chrome/answer/2391819?co=GENIE.Platform%3DDesktop&hl=en),
for Chrome on a computer:

- To put a group away without losing it, right-click its name or coloured circle and choose
  **Close group**. A closed group is not deleted.
- To open it again, choose **More (⋮) → Tab groups** and the group's name, or the grid icon on the
  bookmarks bar. **Settings → Appearance → Show tab groups in bookmarks bar** puts them there.
- If you sign in with your history and tabs synced, changes to your groups are saved and synced to
  your other devices.

If a group has gone, check **More → Tab groups** first, then **History** (**Ctrl+H**, or
**Command+Y** on a Mac) for a recently closed window. **Ctrl+Shift+T**, or **Command+Shift+T**,
reopens closed tabs and windows.

Where it falls short: **Delete group** removes the group on every device signed in to the same
account, and Google's help describes no way to export groups to a file. Chrome's bookmark export
keeps links, not live groups.

## 2. Check the free session managers

You do not need to buy Berth to save tab groups.

| Option | Useful for | Check before relying on it |
| --- | --- | --- |
| Chrome itself | Closing and reopening groups, synced across your devices | No export file; a deleted group goes everywhere |
| [Tab Session Manager](https://chromewebstore.google.com/detail/tab-session-manager/iaiomicjabeggjcfkbimgmglanimpnae) | Automatic saves, named sessions, import and export, cloud sync; its listing says it supports tab groups | Turn on its **Save tab groups** option; in the version we read (7.4.0) it starts off |
| [Session Buddy](https://chromewebstore.google.com/detail/session-buddy-tab-bookmar/edacconmaakjimmfgnblocblbcdcpbko) | Saving and restoring sessions, automatic tab history, export in many formats | We could not confirm whether it restores Chrome's native groups |
| [Berth](/berth/) | Automatic checkpoints and a JSON backup file that keep each group's name, colour and tabs | Groups must be open in a window to be saved; turn on external backups |

Descriptions come from each publisher's store listing, checked on 8 November 2026. We do not claim
to beat these tools on every feature. This guide is written by Berth's developer.

## 3. Keep your groups in Berth

1. Install Berth from the [Chrome Web Store](https://chromewebstore.google.com/detail/berth-auto-tab-backup-ses/jdnmflebhmniemajlkianhflfnimgcmi).
   It saves checkpoints of your normal windows as they change, including each open group's name,
   colour, collapsed state and tabs in order.
2. To keep a set of groups under a name, choose **Save workspace**.
3. Open **External backups** and choose **Turn on external backups**, so the groups also sit in
   `berth-latest.json` in your downloads, outside Chrome's profile. Choose **Choose a backup to
   check** and select the file to confirm it is readable.
   [Backing up Chrome tabs](/berth/back-up-chrome-tabs/) has more on the file.

Berth sees only groups that are open in a window. A group you have closed into Chrome's saved groups
is not in any window, so open it before you rely on Berth for it. A checkpoint taken before a group
was closed or deleted still holds it, for as long as that checkpoint is kept.

## 4. Bring the groups back

1. Open Berth's **Recovery** and pick a checkpoint from before the group went, or a workspace's
   **Open preview**. After a lost profile or on a new computer, choose **Import backup** and select
   your JSON file first.
2. Tick the windows or tabs you need and choose **Restore selected**.

Berth opens new windows beside your current ones and rebuilds each group with its name and colour.
If a group fails to form, restoring the same selection again repairs it rather than duplicating what
already opened.

Berth restores links, groups, pins and windows, not unsent forms, unsaved edits, cookies or logins.
Free keeps seven days of checkpoints and three named workspaces you create; importing, exporting and
restoring stay free. Berth Pro is **$12.99 once** for longer history and more workspaces.
[Berth's page](/berth/) has the terms, refunds and privacy policy.
