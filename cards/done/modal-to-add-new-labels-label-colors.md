---
title: Modal to add new labels + label colors
column: done
position: q
created: 2026-01-05T18:42:20Z
modified: 2026-01-06T11:00:16Z
labels: [feature, important]
---

When editing an existing card, or creating a new card, there should be a button to add new label names + set the label color

## Notes

**Dependency:** First implement "Config button to edit board.md" which creates the settings infrastructure. Label management can then be added as a section within that settings panel, and optionally a quick-add button in the card editor that links to it.

Any time the label selector shows up in edit or new card modals, there should be a button that opens up the settings so the user can add a label there.

I guess this can be merged with "new card modal does not have label picker"