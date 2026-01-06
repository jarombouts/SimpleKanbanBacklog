---
title: Inconsistent reordering when dragging cards
column: done
position: ym
created: 2026-01-06T10:31:21Z
modified: 2026-01-06T11:01:44Z
labels: [bug]
---

When dragging a card, the existing (non dragged) cards correctly reposition themselves so a "gap" opens up below the mouse cursor, showing where a card would be dropped if the mouse is released. However, sometimes (not always) when releasing the mouse, the card ends up in an incorrect position. Please investigate!

## Resolution

Fixed two related bugs in `CardDropDelegate` (Views.swift):

1. **Crash fix (EXC_BAD_ACCESS)**: Changed `performDrop` from async to synchronous by using the already-tracked `draggingCardTitle` binding instead of loading from `itemProvider.loadObject`. The async loading caused state mutations after SwiftUI thought the drop was complete, leading to AttributeGraph crashes.

2. **Position fix**: Added `calculateAdjustedIndex` to correctly handle same-column moves. The visual drop index was based on all cards (including the hidden dragged card), but `moveCard` filters out the dragged card before calculating position. This caused off-by-one errors when dropping after the card's original position.