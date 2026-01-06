---
title: Add undo/redo for card edits
column: done
position: n
created: 2026-01-06T21:45:00Z
modified: 2026-01-06T21:50:00Z
labels: [feature]
---

## Description

Complete the undo/redo implementation by adding support for card edit operations.
Iteration 12 added undo/redo for add/delete/move/archive/duplicate but not for
editing card content (title, body, labels).

## Requirements

- Undo/redo for title changes
- Undo/redo for body content changes
- Undo/redo for label changes
- Action names in Edit menu (e.g., "Undo Edit Card Title")

## Implementation Notes

Completed in iteration/013-undo-redo-card-edits branch:
- Title changes with "Rename Card" action name (handles file rename on disk)
- Body changes with "Edit Card" action name
- Label changes with "Edit Card Labels" action name
- 7 new tests added for card edit undo/redo
- Total: 115 tests passing
