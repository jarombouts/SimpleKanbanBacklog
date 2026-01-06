---
title: Add vim-style o/e keys for edit card
column: done
position: s
created: 2026-01-07T00:55:00Z
modified: 2026-01-07T01:00:00Z
labels: [feature]
---

## Description

Add vim-style o and e keys for opening card editor.
Completes the vim action suite.

## Key Mappings

- `o` = open card for editing (like Enter key)
- `e` = edit card (alias for o, like Enter key)

## Implementation Notes

Completed in iteration/024-vim-o-open-card branch:
- Added o/O/e/E handling in vim key block in Views.swift
- Reuses existing handleEnter method
- Updated README keyboard shortcuts section
- Complete vim suite: h/j/k/l (nav), 0/G/$ (jump), x (delete), o/e (edit)
