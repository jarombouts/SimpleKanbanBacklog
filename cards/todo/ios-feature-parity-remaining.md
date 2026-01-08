---
title: iOS Feature Parity - Remaining Items
column: todo
position: t
created: 2026-01-07T08:52:04Z
modified: 2026-01-08T14:46:00Z
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

## Still TODO

### Column Management
- [ ] Column collapse/expand (tap header or swipe)

### Board Settings
- [ ] Card template editing

### iPad-specific
- [ ] Pointer/trackpad hover states
- [ ] Split View multitasking
- [ ] Slide Over support
- [ ] Pull-to-refresh for sync

## Notes

Most high-priority iOS features are now complete. Remaining items are polish/enhancement features:
1. Column collapse/expand (UX enhancement)
2. Card template editing (less common use case)
3. iPad-specific features (hardware keyboard, pointer, multitasking)
