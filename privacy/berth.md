---
layout: page
title: "Berth — Privacy Policy"
permalink: /privacy/berth/
---

# Berth — Privacy Policy

Last updated: 19 October 2026

Berth saves browser work sessions and restores them from local checkpoints and backup files.
It is made by Spyridon Pikoulas. Contact: [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com).

## Your sessions and backup files

Berth reads the URLs and titles of tabs in normal browser windows, their order and pinned state,
and native tab-group names, colors and collapsed state. It keeps these locally so you can recover
your work. It does not capture incognito windows, page bodies, cookies, passwords, unsent forms
or the contents of documents. It does not restore login sessions or unsaved document edits.

Sessions, named workspaces and recovery-job state are stored in this browser's extension storage.
External JSON backups are written to your computer through Chrome's downloads system. They may
contain private URLs and titles. Keep them somewhere you trust; copying them into a synced folder
shares them with the storage service you choose. Berth does not upload these files or your session
contents to our servers. Importing a file reads it locally.

Berth rotates dated backup files it created to keep a bounded set; keep a separate copy if you
want to retain one independently. Removing Berth removes its browser-held data and leaves the
external files that remain on disk. You can remove saved workspaces in Berth,
and delete your external copies yourself. A browser profile failure can destroy its internal
storage, which is why a retained external backup matters.

## Optional usage counts

Usage measurement is off unless you choose to share it. When enabled, Berth sends at most one
small batch a day containing only the UTC day, extension version and counts of actions such as
completed backup writes, completed or failed restores, saved workspaces, free-limit encounters
and checkout starts. A few local markers count first successful actions and a week-four return
once. These markers remain on your device.

We do not send an installation identifier, account identifier, email, URLs, page titles, workspace
or group names, file paths, file contents or browsing text in these batches. Our measurement
database stores totals by day, version and action only. Cloudflare delivers the requests and
processes network metadata such as IP addresses as a hosting provider; our application does not
log requests or store IP addresses in its database.

These counts help evaluate Berth during an eight-week launch run. Collection stops when that run
ends, and the measurement data is deleted 30 days later. You can turn sharing off in Berth at any
time; unsent usage counts are then cleared. Opting out does not affect recovery, backup or Pro.

## Payments

Pro is sold through [ExtensionPay](https://extensionpay.com), with card payments handled by
[Stripe](https://stripe.com/privacy). ExtensionPay receives the buyer's email and purchase
information. Stripe receives payment details; Berth never receives your card number. Berth keeps
its purchase key and status in browser storage and contacts ExtensionPay to unlock or restore Pro.
ExtensionPay's library uses Chrome sync storage for its purchase key, cached purchase information
and installation time when available, so Chrome may synchronize those fields across your signed-in
browsers if sync is enabled.
Browser sessions, backups and optional usage counts do not use sync storage.
Financial records and their retention are separate from the optional launch usage counts.

## Limited use and sharing

We do not sell your data or use it for advertising. Browser-session data is used only to provide
backup and recovery. Optional action totals are used only to evaluate and improve Berth. Data is
not used for creditworthiness or lending. We follow the Chrome Web Store User Data Policy,
including its Limited Use requirements, and use the providers named above for hosting/payment
functions. The public website has a separate site analytics disclosure.

## Questions

Contact [spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com) for support or privacy questions.
Because the optional counts contain no identifier, we cannot link a particular database total
back to you. Your browser sessions and backup files remain under your control.
