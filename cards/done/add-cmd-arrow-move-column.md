---
title: Add Cmd+Left/Right to move card to adjacent column
column: done
position: n
created: 2026-01-06T23:10:00Z
modified: 2026-01-06T23:20:00Z
labels: [feature]
---

## Description

Add Cmd+Left and Cmd+Right keyboard shortcuts to quickly move the selected
card to the previous or next column. More intuitive than Cmd+1/2/3 for
specific columns.

## Requirements

- Cmd+Left: Move card to previous column (if not already in first)
- Cmd+Right: Move card to next column (if not already in last)
- Works with single selection only
- Maintains card's relative position in new column
- Supports undo/redo

## Implementation Notes

Completed in iteration/016-cmd-arrow-move-column branch:
- Added NavigationResult.moveCardToPreviousColumn/moveCardToNextColumn cases
- Added handleCmdArrowLeft/Right methods to KeyboardNavigationController
- Wired up in Views.swift command key handling
- Updated keyboard shortcuts documentation to list all shortcuts
- 11 new tests for edge cases
- All tests passing (75 XCTest + 115 Swift Testing)
