---
title: Add column collapse/expand
column: done
position: zzc
created: 2026-01-05T18:30:00Z
modified: 2026-01-06T21:10:00Z
labels: [feature]
---

## Description

Allow columns to be collapsed to save horizontal space.

## Requirements

- [x] Collapse button in column header
- [x] Collapsed column shows just header + card count
- [x] Click to expand
- [x] Remember collapsed state per board

## Implementation (Iteration 008)

- Added `collapsed` property to Column struct (defaults to false)
- Updated board.md parsing and serialization to handle collapsed state
- Only serializes `collapsed: true` to minimize git diffs
- Created collapsed column view (narrow strip with vertical name + card count)
- Collapsed columns still accept drag-drop (cards go to end)
- Click anywhere on collapsed column to expand
- Comprehensive tests added

## Branch

`iteration/008-column-collapse-expand`

## Notes

From roadmap Phase 5.4. Previously marked "wontdo" but implemented in iteration 8.
