---
title: Add vim-style x key for delete
column: done
position: r
created: 2026-01-07T00:50:00Z
modified: 2026-01-07T00:55:00Z
labels: [feature]
---

## Description

Add vim-style x key for deleting cards with confirmation.
Completes the vim action suite alongside navigation keys.

## Key Mapping

- `x` = delete selected card(s) with confirmation (like Delete key)

## Implementation Notes

Completed in iteration/023-vim-x-delete branch:
- Added x/X handling in vim key block in Views.swift
- Reuses existing delete logic with confirmation dialog
- Works with multi-selection for bulk delete
- Updated README keyboard shortcuts section
- Part of complete vim suite: h/j/k/l, 0/G/$, x
