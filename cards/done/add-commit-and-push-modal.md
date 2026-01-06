---
title: Add commit and push modal
column: done
position: m
created: 2026-01-06T12:00:00Z
modified: 2026-01-06T09:56:32Z
labels: [feature, important]
---

## Description

Add a modal dialog that allows users to commit and push board changes without leaving the app.

## UX Flow

1. When status is "Uncommitted", show a "Commit" button in toolbar (next to status)
2. Click opens modal with:
   - List of changed files (staged automatically: board.md, cards/, archive/)
   - Commit message text field
   - "Commit" button (just commit locally)
   - "Commit & Push" button (commit + push to origin)
3. After success, status updates to "Synced" or "X ahead"

## Requirements

- Only stage board-specific paths (board.md, cards/, archive/)
- Show clear error if commit/push fails
- Keyboard shortcut: Cmd+Shift+C for commit modal?

## Notes

Keeps the simple case simple. Users can still use terminal for complex git operations (rebasing, conflict resolution, etc.).