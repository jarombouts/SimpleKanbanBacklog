---
title: Add Shift+Arrow keys to extend selection
column: done
position: n
created: 2026-01-06T23:50:00Z
modified: 2026-01-07T00:30:00Z
labels: [feature]
---

## Description

Add Shift+Up and Shift+Down keyboard shortcuts to extend the current selection
by one card. Similar to Shift+Click but keyboard-driven.

## Requirements

- Shift+Up: Extend selection to include card above current
- Shift+Down: Extend selection to include card below current
- Only works within same column (like Shift+Click)
- Uses anchor card concept for consistent range selection
- If no selection, acts like regular arrow key

## Implementation Notes

Completed in iteration/019-shift-arrow-extend-selection branch:
- Added NavigationResult cases: extendSelectionUp, extendSelectionDown
- Added handleShiftArrowUp/Down methods to KeyboardNavigationController
- Wired up Shift modifier detection in Views.swift
- Uses selectRange(to:) which leverages existing anchor-based selection
- Updated README keyboard shortcuts section
- 10 new tests for edge cases
- All Shift+Arrow tests passing (85 XCTest + 115 Swift Testing)
