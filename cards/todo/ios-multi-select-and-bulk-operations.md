---
title: iOS Multi-select and Bulk Operations
column: todo
position: n
created: 2026-01-07T08:52:04Z
modified: 2026-01-07T08:52:04Z
labels: [feature]
---

## Description

Add multi-select capability and bulk operations to the iOS app, matching macOS functionality.

## Requirements

- Edit mode with checkboxes on cards
- Bulk actions toolbar (move to column, archive, delete)
- "Select All" option
- Long-press or edit button to enter selection mode
- Visual feedback for selected cards

## Notes

macOS supports:
- Click to select, Cmd+click to add/remove from selection
- Shift+click for range select
- Bulk archive (Cmd+Backspace), bulk delete, bulk move (Cmd+1/2/3)

iOS should use touch-appropriate patterns:
- Edit mode toggle
- Checkboxes or selection circles
- Bottom toolbar for actions when cards selected
