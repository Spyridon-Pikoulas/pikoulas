---
layout: page
title: "Recover browser work from a Berth backup"
permalink: /berth/recover-from-a-backup/
theme: extensions
---

# Recover browser work from a Berth backup

A surviving backup can bring back your tab links, windows, pinned tabs and named tab groups
after a browser profile is lost. You need the JSON file saved before the loss. Berth cannot
reconstruct a missing backup, unsaved forms, document edits, cookies or login sessions.

Berth is being prepared for Chrome Web Store review. These instructions describe its recovery
workflow; the install link will appear on the [Berth page](/berth/) once it is public.

## Find your file

If you enabled automatic external backups, look in your browser's Downloads folder, under
`Berth` or the subfolder you chose. The latest file is `berth-latest.json`; dated copies have
names beginning with `berth-`. A manually exported file may be called `berth-backup.json` or
`berth-checkpoint.json`. Keep an untouched copy before recovering.

A checkpoint held only inside the old browser profile may have been lost with that profile.
A file on the same disk does not protect against losing the disk or device. Keep a separate
copy in your own trusted backup storage. The files contain readable URLs and page titles.

## Read the links without the extension

Before a failure, Berth's **External backups** screen lets you download a recovery reader.
Keep `berth-recovery-reader.html` beside a backup. Open the reader in a browser, choose your
JSON file and open the links you need. It reads the file locally and does not upload it.

The reader displays windows and group labels. Opening individual links does not rebuild native
Chrome groups or the original window layout; use Berth's import and restore for that.

## Restore windows and groups in Berth

1. Open Berth and choose **Import backup**. Select a Berth or Tab Session Manager JSON file.
2. Confirm the import. Existing sessions remain saved, and unsupported links are excluded.
3. Open the imported workspace's preview. Select the tabs or windows you need.
4. Choose **Restore selected**. Berth creates new windows and leaves current work open.

**Skip links already open** is on by default. Turn it off if you want a separate copy of a link
that is already open. If a tab or group fails, retry the same selection to resume the recovery;
review the reported result before starting a different restore.

Restoring and exporting a surviving backup remain available at the free workspace limit.
Only HTTP and HTTPS links are supported; browser settings pages and extension pages are excluded.

## Check your backup before you need it

Turn on external backups, then wait for a completed file. In **External backups**, choose
**Choose a backup to check** and select the real JSON file from disk. Berth validates it and
reports whether its bytes match the last completed automatic write. A completed download alone
does not establish that a cloud service copied it. Keep the reader and test a backup while your
current browser work is still available.

[Berth](/berth/) · [Privacy policy](/privacy/berth/) ·
[Support](mailto:spyridwn.pd@gmail.com)
