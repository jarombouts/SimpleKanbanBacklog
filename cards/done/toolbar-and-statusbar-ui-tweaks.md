---
title: Toolbar and statusbar UI tweaks
column: done
position: ts
created: 2026-01-06T12:30:00Z
modified: 2026-01-06T10:24:06Z
labels: [feature, important]
---

## Description

Small UI improvements to the toolbar and selection status display.

## Changes

1. **Default toolbar mode**: Set "Icon and Text" as default (currently defaults to "Icon Only")

2. **Rename "Push" to "Sync"**: The push button should say "Sync" instead of "Push"

3. **Move selection status to bottom statusbar**:
   - Remove "Selected: ..." text from toolbar
   - Add a status bar at bottom right of window
   - Show selection info there instead (e.g., "Selected: Add commit and p...")

## Why

- Icon and Text is more discoverable for new users
- "Sync" is more user-friendly than git terminology "Push"
- Selection status clutters the toolbar; bottom statusbar is more standard macOS pattern