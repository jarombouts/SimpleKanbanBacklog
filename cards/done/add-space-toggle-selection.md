---
title: Add Space bar to toggle card selection
column: done
position: o
created: 2026-01-07T00:35:00Z
modified: 2026-01-07T00:40:00Z
labels: [feature]
---

## Description

Add Space bar keyboard shortcut to toggle a card in/out of multi-selection.
More ergonomic than Cmd+Click for keyboard-driven workflows.

## Implementation Notes

Completed in iteration/020-space-toggle-selection branch:
- Added NavigationResult.toggleCardInSelection case
- Added handleSpace method to KeyboardNavigationController
- Wired up .space key in Views.swift
- Uses existing toggleSelection method (same as Cmd+Click)
- Updated README keyboard shortcuts section
- 7 new tests for edge cases (all pass)
- Total: 92 XCTest + 115 Swift Testing = 207 tests
