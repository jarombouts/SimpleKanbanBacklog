---
title: Fix duplicate title and empty column bugs
column: done
position: tm
created: 2026-01-06T10:00:00Z
modified: 2026-01-06T11:01:41Z
labels: [bug]
---

## Description

Fixed two bugs in card creation:

## Bug 1: Empty column field
Cards could be created with empty column, saving to `cards/` instead of `cards/{column}/`.

**Fix:** Added validation in CardWriter.save() to reject empty columns.

## Bug 2: Duplicate title detection
Two cards with the same title but different slugs could exist (e.g., if a card was renamed externally but kept its old filename).

**Fix:** Changed duplicate check to compare actual parsed titles instead of slugified filenames. Also added in-memory check in BoardStore for fast-path detection.

## Tests added
- throwsOnEmptyColumn
- detectsDuplicateTitleWithDifferentSlug
- throwsOnDuplicateTitleAcrossColumns