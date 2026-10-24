---
layout: page
title: "DedupeFill: Review Duplicates for Google Sheets™"
permalink: /dedupefill/
theme: addons
---

<div class="product"><p class="crumb"><a href="/addons/">Workspace add-ons</a></p><div class="title"><img class="icon" src="/media/dedupefill-icon.webp" width="128" height="128" alt=""><h1>DedupeFill: Review Duplicates for Google Sheets™</h1></div><p class="line">Deduplicate rows by key; review retained and discarded tabs in Google Sheets™.</p><div class="foot"><span class="price">Pro $9.00 once</span><span class="soon">Coming soon</span></div><p class="links"><a href="/privacy/dedupefill/">Privacy policy</a> &middot; <a href="/terms/dedupefill/">Terms of service</a> &middot; Support: <a href="mailto:spyridwn.pd@gmail.com">spyridwn.pd@gmail.com</a></p></div>

<div class="shots"><img class="shot" src="/media/dedupefill-1.webp" width="720" height="595" alt="DedupeFill: Review Duplicates for Google Sheets™ screenshot" loading="lazy"><img class="shot" src="/media/dedupefill-2.webp" width="720" height="595" alt="DedupeFill: Review Duplicates for Google Sheets™ screenshot" loading="lazy"><img class="shot" src="/media/dedupefill-3.webp" width="720" height="595" alt="DedupeFill: Review Duplicates for Google Sheets™ screenshot" loading="lazy"><img class="shot" src="/media/dedupefill-4.webp" width="720" height="305" alt="DedupeFill: Review Duplicates for Google Sheets™ screenshot" loading="lazy"></div>


Review duplicate rows before creating two new tabs: the rows you keep, and the rows you discard
with references to their retained source rows. Your source stays intact.

**Two complete paired jobs free per Google account; $9 once for more. Refunds within 14 days.**
Preview and recognized retries are free. No subscription or automatic renewal; technical and
Google service limits apply.

**DedupeFill is being prepared for Marketplace release. It is not available to install yet.**

## Choose what counts as a duplicate

- Select a range with headings and the columns that identify matching rows.
- Choose the first or last source row to keep. This means row order, not newest date.
- Review retained and discarded rows, their counts and source-row references before creating
  both output tabs. Optional fictional practice data lets you try the workflow first.

Keys use exact typed values: case and spaces matter, and text `00123` differs from numeric
`123` displayed as `00123`. There is no fuzzy matching or automatic merging. Blank-key rows
need explicit approval to keep each separately. DedupeFill refuses date-valued keys, source errors and ambiguous error-looking text.
Selected hidden and filtered rows participate.

## Keep a snapshot of both decisions

All original columns survive in the appropriate output. The discarded report adds original
and retained source-row numbers, so conflicting non-key values remain available for review.
Calculated values and number formats are copied; formulas become results and literal text
stays text. Fonts/layout and source annotations are not copied; Sheets may detect plain URLs
normally. Later source changes do not update the outputs. Both tabs use the spreadsheet's
existing sharing permissions.

Stop after the current request; a retry of the same unchanged job continues it without using another free job.

## Supported bounds

Select up to 5,000 data rows plus one heading row, up to 20 source columns and up to 10
key columns. The two outputs together must fit 100,000 cells, including both heading rows
and the discarded report's two added source-row reference columns. These limits apply jointly;
not every maximum-width input fits the paired-output cap. Oversized jobs refuse rather than
silently dropping rows. Additional text safeguards and Google service limits apply to free
and paid jobs.

Jobs near these limits can take several minutes; DedupeFill works in steps and shows its progress.

## When a free method is enough

For ordinary cleanup, duplicate your tab and use
[Data cleanup → Remove duplicates](https://support.google.com/docs/answer/6325535?hl=en).
[UNIQUE](https://support.google.com/docs/answer/10522653?hl=en) also returns unique rows.
DedupeFill is for reviewing a paired retained/discarded result inside Sheets; these free
methods may be enough if you do not need that report. Google's matching rules can differ.

## Access and billing

DedupeFill accesses only the spreadsheet where you use it. Google's services do the processing;
no AI or external spreadsheet-processing service receives your rows. Stripe receives billing
email and payment information, not spreadsheet contents. The account shown in the sidebar owns
the free allowance and purchase; operations check that account.

Google Sheets™ is a trademark of Google LLC.

[Privacy policy](/privacy/dedupefill/) · [Terms of service](/terms/dedupefill/) · Support:
[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com)
