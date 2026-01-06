---
title: Add card duplication feature
column: done
position: q
created: 2026-01-06T12:00:00Z
modified: 2026-01-06T12:30:00Z
labels: [feature]
---

## Description

Allow users to duplicate existing cards to quickly create similar cards.

## Requirements

- Add `duplicateCard` method to BoardStore
- Create copy with modified title (e.g., "Original Title (Copy)")
- If "(Copy)" already exists, append number: "(Copy 2)", "(Copy 3)", etc.
- Preserve labels and body content from original
- Place duplicate in same column, right after the original card
- Set fresh created/modified timestamps
- Add to context menu (right-click on card)
- Add keyboard shortcut Cmd+D
- Support multi-select: duplicate all selected cards

## Notes

- Common feature in Kanban apps like Trello, Notion
- Speeds up workflow when creating similar cards
