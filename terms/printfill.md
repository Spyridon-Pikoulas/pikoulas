---
layout: page
title: "PrintFill: QR & Barcode Labels - Terms of Service"
permalink: /terms/printfill/
---

# PrintFill: QR & Barcode Labels - Terms of Service

Last updated: 19 October 2026

These terms are between you and Spyridon Pikoulas, who makes PrintFill, an add-on for Google
Sheets™. Installing or using PrintFill means you accept them.

## The service

PrintFill turns displayed values from rows in the current spreadsheet into QR or Code 128 labels.
You select the source, map payload, caption and filename columns, choose a supported layout and
check the prepared labels. It leaves source cells unchanged and prepares one ZIP containing a
printable PDF, one captioned PNG per row and a manifest. Processing happens in your browser using
data read from Google's services. The manifest contains payloads, captions, filenames and positions;
you are responsible for handling and sharing these downloaded data.

QR uses UTF-8 and error correction level M. Code 128 accepts printable ASCII only. Displayed
payloads are encoded exactly, without trimming or normalization. Up to 100 rows, ten columns,
1,010 cells including optional headings and 100,000 serialized displayed-text characters are
supported per job, with a 50 MiB cap on both the PDF and ZIP. Payloads must be at most 2,000
characters and fit the selected label at the supported readable size. One-line captions must fit the bundled font at
8 pt. Unsafe or duplicate filename IDs, unsupported text or overflow refuse the whole batch.
Google's service limits and the same technical limits apply to free and paid use.

Supported label layouts are OnlineLabels OL875 Letter and Flexi Labels FS21 A4, based on OL875
supplier PDF outlines and FS21 supplier dimensions. Supplier codes are descriptive; PrintFill is
independent and not endorsed by these suppliers. No other stock, printer, scanner, physical
alignment, GS1 compliance or retail certification is guaranteed. Print at Actual size / 100%,
test on plain paper, and check printed alignment and decoded values before a full run. Previews
and digital decoding cannot replace a test with your actual paper, printer and scanner.

Generated codes are static. PrintFill does not host destinations, shorten links, redirect or track
scans, or verify that a destination or encoded information is correct, safe or available.

## Free plan and the one-time unlock

The free plan allows **12 generated row-codes in total per Google account**, rather than per
spreadsheet, page, day or download format. Each generated row counts once, including its PDF
label and PNG. Preview is free. A batch larger than the remaining allowance requires selecting
fewer rows or unlocking; PrintFill does not silently omit rows to fit the allowance.

Usage is recorded after the browser prepares all outputs and records the job's completion,
rather than when your operating system confirms a saved file or a printer prints it. A recognized
retry or repeated download does not consume the allowance again. The same unchanged latest job
can regenerate after reopening by reselecting its source and options. Keep downloaded files if
you need them again. Scanning a generated code does not consume the generation allowance.

Your Google account's add-on storage holds total free usage and one latest generation record:
a random job identifier, a source/settings fingerprint, row-code count, timestamps and completion
flag. It contains no raw cells, payloads, captions, mappings, filenames, source range or email.
The record has no automatic expiry. Starting a different batch that passes the source and
allowance checks replaces the record before completion; no usage is taken until completion is
recorded. **Forget latest retry receipt** removes it without restoring free usage or removing your
purchase. A forgotten/replaced free job loses retry recognition and cannot be regenerated for
free once the allowance is exhausted.

The **$9 one-time unlock** covers generation within PrintFill's supported workflows and technical
limits for the Google account shown in the sidebar, plus any tax shown at checkout. It has no
scheduled expiry, subscription or automatic renewal. Payment is through Stripe. The unlock
belongs to the account used to buy it, rather than every collaborator on the spreadsheet.
A full refund or disputed payment removes the paid unlock.

Any payment can be refunded within 14 days: write to the address below with the email you paid with.

## Your part

Use PrintFill lawfully, within Google's terms, and only with data you have the right to use.
Check the source, decoded payloads, captions, filenames and printed labels before using them.
Do not try to bypass the free limit or plan check. You are responsible for downloaded files,
encoded destinations and their use.

## Warranty and liability

PrintFill is provided as it is, without warranty of any kind. To the extent the law allows, we
are not liable for indirect or consequential loss, and our total liability is limited to what
you paid for PrintFill in the 12 months before the claim. Nothing here limits rights you have
as a consumer that cannot be limited.

## Changes

We may change these terms or prices. A later price change does not charge an existing one-time
buyer again for the unlock they bought. The date above shows the latest version. Danish law
governs these terms.

## Contact

[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com)
