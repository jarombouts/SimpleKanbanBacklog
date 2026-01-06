---
title: Add keyboard card reordering
column: done
position: n
created: 2026-01-06T22:00:00Z
modified: 2026-01-06T22:55:00Z
labels: [feature]
---

## Description

Add keyboard shortcuts to reorder cards within the same column without using
drag and drop.

## Requirements

- Cmd+Up: Move selected card up one position in column
- Cmd+Down: Move selected card down one position in column
- Works with single selection only (not bulk)
- Respects undo/redo

## Implementation Notes

Completed in iteration/014-keyboard-card-reordering branch:
- Added NavigationResult.reorderCardUp/reorderCardDown cases
- Added handleCmdArrowUp/Down to KeyboardNavigationController
- Wired up in Views.swift key handling
- Uses existing moveCard for actual reordering (supports undo)
- 12 new tests for edge cases (top/bottom bounds, single card, etc.)
- All tests passing (53 XCTest + 115 Swift Testing)
