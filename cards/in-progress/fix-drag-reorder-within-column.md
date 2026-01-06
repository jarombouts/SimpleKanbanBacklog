---
title: Fix drag reorder within column
column: in-progress
position: n
created: 2026-01-06T12:45:00Z
modified: 2026-01-06T09:16:15Z
labels: [bug]
---

## Description

Dragging cards within the same column doesn't work properly for reordering.

## Problems

1. **No visual drop indicator**: When dragging a card, there's no visual feedback showing where it will be inserted (e.g., a line between cards)

2. **Always drops at end**: Dragging a card within the same column always puts it at the bottom of the column, ignoring where you actually dropped it

## Expected Behavior

- Show insertion indicator (horizontal line) between cards while dragging
- Drop card at the indicated position, not always at the end
- Should work for both same-column reorder and cross-column moves

## Notes

This makes it impossible to prioritize cards by dragging them up/down within a column.