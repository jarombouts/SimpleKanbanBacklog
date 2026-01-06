---
title: Add new card keyboard shortcut
column: done
position: o
created: 2026-01-06T14:00:00Z
modified: 2026-01-06T14:00:00Z
labels: [feature]
---

## Description

Add a keyboard shortcut for creating new cards (Cmd+Shift+N).

## Implementation

- Added `NavigationResult.newCard(inColumn: String)` case to keyboard navigation
- Cmd+Shift+N opens new card modal in:
  - The selected card's column (if a card is selected)
  - The first column (if no card is selected)
- Updated roadmap with new keyboard shortcut
- Added tests for NavigationResult enum

## Iteration 011 (2026-01-06)

This addresses the improvement noted in iteration 010 QA: "Keyboard shortcut for creating new card could be nice (currently uses button)"
