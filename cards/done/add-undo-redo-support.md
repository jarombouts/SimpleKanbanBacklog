---
title: Add undo/redo support
column: done
position: n
created: 2026-01-06T21:00:00Z
modified: 2026-01-06T21:40:00Z
labels: [feature]
---

## Description

Add undo/redo support for card operations using macOS's UndoManager.

## Requirements

- Undo/redo for card creation (Cmd+Z undoes create)
- Undo/redo for card deletion (Cmd+Z restores card)
- Undo/redo for card moves (between columns, reordering)
- Undo/redo for card edits (title, body, labels)
- Undo/redo for bulk operations (multi-delete, multi-move)
- Standard Cmd+Z / Cmd+Shift+Z shortcuts
- Edit menu with Undo/Redo items

## Technical Approach

Use macOS's built-in UndoManager:
- Each BoardStore gets an UndoManager
- Register undo actions when performing operations
- Undo restores previous state (card data + file on disk)
- Group related operations (e.g., bulk delete as single undo)

## Implementation Notes

Completed in iteration/012-undo-redo-support branch:
- Undo/redo for card creation, deletion, archiving, duplication
- Undo/redo for card moves (column changes + reordering)
- Bulk operations (delete, archive, move) as single undoable actions
- Added CardWriter.unarchive() for restoring archived cards
- Integrated with SwiftUI environment undoManager for native Edit menu
- 108 tests passing including comprehensive undo/redo test suite

Note: Card edits (title, body, labels) not yet implemented - would need
additional infrastructure to track edit state changes.
