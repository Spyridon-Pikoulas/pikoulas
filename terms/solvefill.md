---
layout: page
title: "SolveFill: Goal Seek & Linear Solver — Terms of Service"
permalink: /terms/solvefill/
---

# SolveFill: Goal Seek & Linear Solver — Terms of Service

Last updated: 25 October 2026

These terms are between you and Spyridon Pikoulas, who makes SolveFill, an add-on for Google
Sheets™. Installing or using SolveFill means you accept them.

## The service

SolveFill finds values for cells of your spreadsheet: Goal Seek changes one cell until a formula
cell shows the value you ask for, and the solver finds the variable cells' values that maximize,
minimize or reach a value of an objective cell within your constraints, for linear and integer
models. Its fields are those of the Goal Seek and Solver dialogs in Microsoft Excel. Check results
that matter before you rely on them.

SolveFill writes into the cells you name as the ones to change. While it reads a model it changes
them one at a time and puts them back; it then writes the answer there, which you keep or replace
with your original values using Restore, as long as the cells still hold the answer. An answer that fails its check in the sheet is not kept:
the original values are put back. The optional Answer Report and the sample model are written to
new sheets.

Microsoft and Excel are trademarks of Microsoft Corporation. SolveFill is not affiliated with,
sponsored or endorsed by Microsoft.

## If a solve is interrupted

Before a Goal Seek or solve first changes a cell, SolveFill keeps a copy of the original values in the
spreadsheet's own storage for SolveFill, until you choose Keep or Restore. A solve runs on
Google's servers in steps, and each step puts the cells back before it ends, so closing the
sidebar or losing your connection leaves your values as they were, or with the answer written.
If the sidebar closed after an answer was written, the next time you open SolveFill in that
spreadsheet it offers Keep or Restore.

If Google stops a step before it ends (for example, when it runs past Google's time limit), the
cells can be left holding values SolveFill was trying. The next time you open SolveFill in that
spreadsheet, at least six minutes later, it names those cells and offers to restore the copy over
whatever they hold then, or to keep them as they are; it starts no new solve until you choose.
This cannot always be done automatically: if the copy could not be kept, SolveFill changes nothing,
and if the copy was lost or you want values from before later edits, use **File > Version
history** in Sheets to see and restore earlier versions.

## Free use and the one-time purchase

Goal Seek is free and unlimited. Each Google account gets **3 solves free in total**. One solve is
one answer written and checked in the sheet; creating the sample model, Goal Seek, and solves that
find no answer or that SolveFill refuses before writing use none. A request with an uncertain
outcome keeps its reserved solve unavailable; it is not automatically refunded or repeated. If that
happens, write to us and we will restore it.

After that, SolveFill is a $9 one-time unlock per Google account for unlimited solves, paid
through Stripe at the price shown before you pay, plus any tax due. There is no subscription or
automatic renewal. Models of up to 1,000 variable cells and 10,000 cells read are supported, and
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
