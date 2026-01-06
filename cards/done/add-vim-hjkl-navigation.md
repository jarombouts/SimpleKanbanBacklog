---
title: Add vim-style h/j/k/l navigation
column: done
position: p
created: 2026-01-07T00:40:00Z
modified: 2026-01-07T00:45:00Z
labels: [feature]
---

## Description

Add vim-style keyboard navigation using h/j/k/l keys for developers
who prefer this navigation style.

## Key Mappings

- `h` = left (navigate to previous column)
- `j` = down (navigate to next card)
- `k` = up (navigate to previous card)
- `l` = right (navigate to next column)

## Implementation Notes

Completed in iteration/021-vim-jk-navigation branch:
- Added vim key handling in Views.swift translateKeyPress
- Only active when no modifiers pressed (Cmd/Shift/etc)
- Reuses existing handleArrow* methods from KeyboardNavigationController
- No new tests needed - uses already-tested navigation handlers
- Updated README keyboard shortcuts section
