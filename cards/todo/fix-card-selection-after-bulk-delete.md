---
title: Fix card selection after bulk delete
column: todo
position: w
created: 2026-01-05T18:30:00Z
modified: 2026-01-06T09:09:10Z
labels: [improvement]
---

## Description

After bulk deleting cards, selection should move to a nearby card instead of clearing completely.

## Current behavior

Selection is cleared after delete.

## Expected behavior

Select the next card in the same column, or the previous card if at end of column.