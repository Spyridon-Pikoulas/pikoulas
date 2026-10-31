---
layout: page
title: "SplitFill: Split Sheet by Column into Tabs - Terms of Service"
permalink: /terms/splitfill/
---

# SplitFill: Split Sheet by Column into Tabs - Terms of Service

Last updated: 26 October 2026

These terms are between you and Spyridon Pikoulas, who makes SplitFill, an add-on for Google
Sheets™. Installing or using SplitFill means you accept them.

## The service

SplitFill groups rows from one explicitly selected rectangular range in the current spreadsheet.
You choose a grouping column, optional heading row and inclusion of all selected hidden/filtered
rows, review the groups/output names, then confirm new tabs. Source rows stay in their original
order within each group; existing source and output tabs are not overwritten.

Grouping uses exact displayed text: case, spaces, displayed dates/numbers and leading zeroes
matter. Blank labels form their own group. Equal displayed labels share a group even if their
underlying value types differ; each output cell keeps its own calculated value type. SplitFill
does not restore leading zeroes already lost to source conversion.

At creation, SplitFill copies calculated values, number/date formats and supported base cell
styles, column widths and an optional frozen header. Formulas, embedded source hyperlink targets,
notes, validation, conditional formatting, filters, hidden states, protection and mixed rich-text
decoration are not copied. Google Sheets may detect and style plain URL text in the output as it
normally does. Selected hidden rows appear visibly in the new tabs. This is a snapshot workflow, not
full-fidelity copying, live refresh, separate-file creation or distribution.
Output tabs contain copied source data under the spreadsheet's existing sharing permissions;
they do not provide private access for different groups.

A job supports **1–1,000 data rows**, up to **10 columns**, **50 groups** and **10,500 output cells
including repeated headers**. An optional source heading row is additional to the data-row limit.
Jobs near these limits can take several minutes; SplitFill works in steps and shows its progress.
These limits apply to free and paid use; text-size and spreadsheet-allocation safeguards also
apply. Merged source cells, unsupported values, formula results beginning with error-like `#` text and
oversized jobs refuse rather than silently dropping rows. Literal error-looking text is permitted;
a formula producing such text is conservatively refused, even if that text was intentional.

Timing varies with content and Google's services; these bounds are not a completion-time
guarantee or proof of every simultaneous text/allocation extreme. Google's service limits apply.

Preview captures typed values, displayed text, formulas, base styles, column widths and settings.
Each generation request checks fresh values, displayed text and formulas. Formatting and widths
may be reused from a short-lived cache, then checked afresh before completion. Style-only source
changes may therefore be detected after some tabs have been written; completion is refused and
those tabs remain. Missing or invalid cached formatting requires a matching full source check
before further writes. Changes solely to omitted source notes, links or rich-text annotations
do not invalidate Preview. The source itself is not modified.

## Free plan and the one-time unlock

From 26 October 2026, accounts with no earlier SplitFill records get **two trial jobs in total**,
each over 50 source rows taken from each group in turn, in tabs titled "Trial split". Accounts that
used SplitFill before then keep **two complete snapshot jobs in total per Google account**, across
spreadsheets. Earlier use, settings or licence records found in your account preserve that
allowance. Unclear or damaged records also keep it; accounts with no earlier records receive the
trial jobs. After the unlock, preview the same selection again to split it whole. Preview is
free. One entire set counts as one job, regardless of its number of tabs. All output tabs must be
written, verified and finalized before one atomic completion record takes one free use. Creating a
tab or pausing between groups does not count as completion. Paid jobs do not consume remaining
free jobs.

An accepted job retains its starting allowance decision while completing its groups. **Stop after
current request** pauses between calls; the current request may still finish. Unfinished output
can contain a mix of final and **INCOMPLETE** names if final renaming was interrupted. Final names
alone do not establish whole-job completion; check the verified completion shown in the sidebar.
An interrupted reply does not by itself mean failure: inspect the tabs and retry the same job.

After reopening, choose the same source/options, Preview, then **Create or reopen these
snapshots** or **Resume these snapshots**. A recognized retry preserves the same tab identifiers
and does not consume another free job, including at the free cap. Changes to checked source or
output data, or missing or ambiguous output tabs, can refuse recovery. SplitFill does not delete or
repair such tabs. Keep your source and completed outputs until you have checked them.

Before each write, SplitFill checks the affected output's typed values, displayed text, absence
of formulas, managed grid dimensions, identity/name and ownership. Previously written outputs'
identities/names/ownership may wait until whole-set completion or reopening a completed job.
Every output must pass the whole-set check before success or a free-use debit. Edits or deletions
of earlier outputs may therefore be detected later, with partial tabs preserved.
Formatting/annotation edits are not independently audited or overwritten and may remain when
the checked data and grid stay exact.

The latest record has no automatic expiry. A different job that passes source and allowance
checks replaces a completed record before beginning. An unfinished job blocks a different one
until it is completed or explicitly forgotten. **Forget latest retry receipt**, after
confirmation, removes recognition without deleting tabs, restoring usage or removing a purchase.
Existing tabs/names stay as they are and lose automatic recovery. Forgotten/replaced jobs cannot
rely on free retry recognition; another job requires remaining allowance or the unlock.
Storage and retention details are in the [privacy policy](/privacy/splitfill/).

The **$9 one-time unlock** covers snapshot jobs within SplitFill's supported workflows and
technical limits for the Google account shown in the sidebar, plus any tax shown at checkout.
It has no scheduled expiry, subscription or automatic renewal. Payment is through Stripe. The
unlock belongs to the account used to buy it, rather than every collaborator on the spreadsheet.
A full refund or disputed payment removes the paid unlock.

Any payment can be refunded within 14 days: write to the address below with the email you paid with.

## Your part

Use SplitFill lawfully, within Google's terms, and only with data you have the right to use.
Check the account, source range, grouping labels, hidden-row inclusion, proposed names and
completed snapshots before relying on them. Consider who can access the copied data under your
spreadsheet's sharing settings. Do not bypass the free limit or plan check.

## Warranty and liability

SplitFill is provided as it is, without warranty of any kind. To the extent the law allows, we
are not liable for indirect or consequential loss, and our total liability is limited to what
you paid for SplitFill in the 12 months before the claim. Nothing here limits rights you have
as a consumer that cannot be limited.

## Changes

We may change these terms or prices. A later price change does not charge an existing one-time
buyer again for the unlock they bought. The date above shows the latest version. Danish law
governs these terms.

## Contact

[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com)
