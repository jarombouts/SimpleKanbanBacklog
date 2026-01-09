---
title: iOS Feature Parity - Remaining Items
column: todo
position: t
created: 2026-01-07T08:52:04Z
modified: 2026-01-09T17:00:00Z
labels: [feature]
---

## Description

Remaining iOS features needed to reach parity with macOS version.

## Completed (2026-01-08)

### Column Management
- [x] Column settings (rename, reorder, delete) - via Board Settings

### Label Management
- [x] Create new labels from iOS - via Board Settings
- [x] Edit label colors - via Board Settings
- [x] Filter by label (popover/sheet) - toolbar button with popover

### Board Settings
- [x] Edit board title
- [x] Manage columns and labels

### UI Parity
- [x] Dynamic column width (fills space with 1-2 columns)
- [x] Drag-and-drop insertion gap visual feedback
- [x] Card layout matches macOS (title → body → labels)
- [x] Toolbar with label filter, archive, delete, settings buttons
- [x] Archive/delete toolbar buttons as drop targets

### Editor Enhancements
- [x] Markdown syntax highlighting (UITextView with attributed text, regex-based)
- [x] Undo/redo support (keyboard toolbar buttons + system UndoManager integration)

### Multi-select
- [x] Multi-select mode with checklist toggle button
- [x] Bulk move to column
- [x] Bulk add/remove labels
- [x] Bulk archive
- [x] Bulk delete

## Completed (2026-01-09)

### Column Management
- [x] Column collapse/expand (tap header chevron to toggle)

### Board Settings
- [x] Card template editing (NavigationLink to template editor)

### iPad-specific
- [x] Hardware keyboard shortcuts (arrows, Enter, Delete, Cmd+N, Cmd+1-9, etc.)

## Still TODO (iPad Polish)

- [ ] Pointer/trackpad hover states
- [ ] Split View multitasking
- [ ] Slide Over support
- [ ] Pull-to-refresh for sync

## Notes

Most high-priority iOS features are now complete. Remaining items are low-priority iPad polish features that primarily affect users with trackpads or multitasking workflows.
