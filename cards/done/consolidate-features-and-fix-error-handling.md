---
title: Consolidate features and fix error handling
column: done
position: zzb
created: 2026-01-06T20:00:00Z
modified: 2026-01-06T20:15:00Z
labels: [improvement]
---

## Description

Iteration 7 work: Consolidated features from parallel branches and fixed a UX bug.

## Changes

### Consolidated Features from Previous Iterations
Merged the following features that were developed in parallel branches but not combined:

1. **Fix card selection after bulk delete/archive** (from iteration/001)
   - Selection now moves to a nearby card instead of clearing completely
   - Added `findNextSelection()` helper function

2. **Delete empty column folder** (from iteration/002)
   - When removing a column, its directory is deleted if empty
   - Added tests for column removal

### Bug Fix: Show Error Alert When Card Creation Fails
Previously, card creation errors (like duplicate titles) were only logged to console and the user saw no feedback. Now errors are displayed in an alert dialog so users know why their card wasn't created.

## Branch

`iteration/007-consolidate-features`

## Notes

Code review identified several potential issues. Most critical ones were already handled correctly (delete operations throw before memory is modified). The error handling fix was implemented to improve UX.
