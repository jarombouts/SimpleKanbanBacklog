---
title: Add vim-style 0/G/$ for first/last card
column: done
position: q
created: 2026-01-07T00:45:00Z
modified: 2026-01-07T00:50:00Z
labels: [feature]
---

## Description

Add vim-style 0/G/$ keys for jumping to first/last card in column.
Completes the vim navigation suite started in iteration 21.

## Key Mappings

- `0` = first card in column (like Home key)
- `G` = last card in column (like End key)
- `$` = last card (vim alternative to G)

## Implementation Notes

Completed in iteration/022-vim-0-G-navigation branch:
- Extended vim key handling in Views.swift translateKeyPress
- Only active when no modifiers pressed
- Reuses existing handleHome/handleEnd methods
- No new tests needed - uses already-tested handlers
- Updated README keyboard shortcuts section
