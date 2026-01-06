---
title: Add Option+Up/Down page navigation
column: done
position: n
created: 2026-01-06T23:35:00Z
modified: 2026-01-06T23:45:00Z
labels: [feature]
---

## Description

Add Option+Up and Option+Down keyboard shortcuts to quickly jump multiple
cards at once (page-like navigation). Useful for boards with many cards.

## Requirements

- Option+Up: Jump up 5 cards (or to first card if fewer)
- Option+Down: Jump down 5 cards (or to last card if fewer)
- Stay within current column
- If no card selected, select first card

## Implementation Notes

Completed in iteration/018-option-arrow-page-navigation branch:
- Added handleOptionArrowUp/Down methods to KeyboardNavigationController
- Added pageJumpSize constant (5 cards)
- Wired up Option modifier detection in Views.swift
- Updated README and Views.swift documentation
- 10 new tests for edge cases
- All tests passing (85 XCTest + 115 Swift Testing)
