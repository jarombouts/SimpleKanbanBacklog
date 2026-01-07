---
title: iOS Hardware Keyboard Shortcuts
column: todo
position: q
created: 2026-01-07T08:52:04Z
modified: 2026-01-07T08:52:04Z
labels: [feature]
---

## Description

Add hardware keyboard support for iPad users with Magic Keyboard or other external keyboards.

## Requirements

### Navigation
- Arrow keys to navigate between cards
- Tab/Shift+Tab between columns
- Vim-style h/j/k/l navigation (optional)

### Card Actions
- Enter to open card for editing
- Delete/Backspace to delete card
- Cmd+Backspace to archive
- Cmd+1/2/3 to move to column

### Other
- Cmd+N to create new card
- Cmd+F for search
- Escape to cancel/close

## Notes

Use SwiftUI's `.keyboardShortcut()` modifier where possible. May need focus management for full navigation support.

See macOS `KeyboardNavigation.swift` for reference implementation.
