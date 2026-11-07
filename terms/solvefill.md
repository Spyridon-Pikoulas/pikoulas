---
layout: page
title: "SolveFill: What-If Analysis, Goal Seek & Solver — Terms of Service"
permalink: /terms/solvefill/
---

# SolveFill: What-If Analysis, Goal Seek & Solver — Terms of Service

Last updated: 2 November 2026

These terms are between you and Spyridon Pikoulas, who makes SolveFill, an add-on for Google
Sheets™. Installing or using SolveFill means you accept them.

## The service

SolveFill finds values for cells of your spreadsheet and shows what your formulas give for other
inputs. Goal Seek changes one cell until a formula cell shows the value you ask for. The solver
finds the variable cells' values that maximize, minimize or reach a value of an objective cell
within your constraints, for linear and integer models. A data table puts each value you list into
an input cell and writes what your formulas show for it. Scenarios save named sets of values for
cells, put them back in, and summarize them. Its fields are those of the Goal Seek, Data Table,
Scenario Manager and Solver dialogs in Microsoft Excel. Check results that matter before you rely on
them.

SolveFill writes into the cells you name as the ones to change. While it reads a model, fills a data
table or makes a Scenario Summary, it changes them one value at a time and puts them back. A solve
then writes the answer there, and showing a scenario writes its values. You keep these or replace
them with your original values using Restore, as long as the cells still hold what was written.

An answer that fails its check in the sheet is not kept: the original values are put back. A data
table's results are written into the table as values, which Restore also takes back. If the table's
own formulas change once the results are in, the results are not kept. The optional Answer Report,
the Scenario Summary and the sample model are written to new sheets.

Microsoft and Excel are trademarks of Microsoft Corporation. SolveFill is not affiliated with,
sponsored or endorsed by Microsoft.

## If a run is interrupted

Before a Goal Seek, solve, data table, scenario shown or Scenario Summary first changes a cell, SolveFill keeps a copy of the original values in the
spreadsheet's own storage for SolveFill, until you choose Keep or Restore. A solve or data table runs on Google's servers in steps, and each step puts the cells back before it ends, so closing the
sidebar or losing your connection leaves your values as they were, or with the answer written.
If the sidebar closed after an answer was written, the next time you open SolveFill in that
spreadsheet it offers Keep or Restore.

If Google stops a step before it ends (for example, when it runs past Google's time limit), the
cells can be left holding values SolveFill was trying. The next time you open SolveFill in that
spreadsheet, at least six minutes later, it names those cells and offers to restore the copy over
whatever they hold then, or to keep them as they are; it changes no cells until you choose.
This cannot always be done automatically: if the copy could not be kept, SolveFill changes nothing,
and if the copy was lost or you want values from before later edits, use **File > Version
history** in Sheets to see and restore earlier versions.

## Free use and the one-time purchase

Goal Seek and scenarios (saving, showing and deleting them) are free and unlimited. Each Google
account gets **3 runs free in total**, shared by solves, data tables and Scenario Summaries. Free
solves used before version 5 count toward the 3. One run is one of these: a solve's answer written
and checked in the sheet; a data table filled; or a Scenario Summary sheet made.

Creating the sample model, Goal Seek and scenarios use none. Nor do runs that find no answer, that
leave a table as it was, or that SolveFill refuses before writing. A request with an uncertain
outcome keeps its reserved run unavailable; it is not automatically refunded or repeated. If that
happens, write to us and we will restore it.

After that, SolveFill is a $9 one-time unlock per Google account for unlimited runs, paid
through Stripe at the price shown before you pay, plus any tax due. There is no subscription or
automatic renewal. Models of up to 1,000 variable cells and 10,000 cells read, and data tables of up to 1,000 values
to try and 10,000 cells, are supported, and
Google's service limits apply to free and paid use.

Any payment can be refunded within 14 days: write to the address below with the Google account
email used for the purchase. A full refund or dispute removes the unlock when a later billing
check finds it; checks are normally cached for six hours, so this is not instant.

## Your part

Use SolveFill lawfully and within Google's terms. Don't try to get around the free limit or the
purchase check.

## Warranty and liability

SolveFill is provided as it is, without warranty of any kind. To the extent the law allows, we are
not liable for indirect or consequential loss, and our total liability is limited to what you paid
for SolveFill in the 12 months before the claim. Nothing here limits rights you have as a consumer
that cannot be limited.

## Changes

We may change these terms or SolveFill's price. A new price applies to future purchases. The date
at the top shows the latest version. Danish law governs these terms.

## Contact

[spyridwn.pd@gmail.com](mailto:spyridwn.pd@gmail.com)
