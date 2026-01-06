---
title: Add Home/End navigation shortcuts
column: done
position: n
created: 2026-01-06T23:00:00Z
modified: 2026-01-06T23:05:00Z
labels: [feature]
---

## Description

Add Home and End keyboard shortcuts to quickly jump to the first or last card
in the current column.

## Requirements

- Home: Select first card in current column
- End: Select last card in current column
- If no card selected, use first non-empty column
- Consistent with arrow key navigation behavior

## Implementation Notes

Completed in iteration/015-home-end-navigation branch:
- Added handleHome/handleEnd methods to KeyboardNavigationController
- Wired up .home and .end keys in Views.swift
- Returns none if already at first/last card (no-op)
- 11 new tests for edge cases
- All tests passing (64 XCTest + 115 Swift Testing)
