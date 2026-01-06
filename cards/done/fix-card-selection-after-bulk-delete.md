---
title: Fix card selection after bulk delete
column: done
position: zyys
created: 2026-01-05T18:30:00Z
modified: 2026-01-06T17:20:00Z
labels: [improvement]
---

## Description

After bulk deleting cards, selection should move to a nearby card instead of clearing completely.

## Current behavior

Selection is cleared after delete.

## Expected behavior

Select the next card in the same column, or the previous card if at end of column.

## Implementation

Added `findNextSelection(afterDeleting:)` helper function that:
1. Finds the first non-deleted card after the lowest deleted card position
2. Falls back to card before if none after
3. Returns nil (clear selection) if column becomes empty

Updated all delete/archive handlers to use this function.
