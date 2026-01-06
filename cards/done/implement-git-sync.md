---
title: Implement git sync
column: done
position: yj
created: 2026-01-06T09:00:00Z
modified: 2026-01-06T11:03:59Z
labels: [feature]
---

## Description

Add automatic git synchronization for boards in git repositories.

## Completed

- Detect if board folder is a git repository
- Status indicator in toolbar (synced/behind/ahead/uncommitted/conflict)
- Auto-fetch and pull every 60 seconds when working tree is clean
- Push button with confirmation dialog
- Conflict detection (user resolves in terminal)