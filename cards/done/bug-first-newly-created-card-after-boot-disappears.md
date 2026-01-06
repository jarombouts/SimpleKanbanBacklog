---
title: "Bug: first newly created card after boot disappears!"
column: done
position: zyx
created: 2026-01-06T10:33:59Z
modified: 2026-01-06T11:45:00Z
labels: [bug, important]
---

When creating a new card after the board is opened for the first time, this new card entirely disappears. No data is written to disk. Please investigate.

## Resolution

**Root cause:** SwiftUI state race condition. The `sheet(isPresented:)` pattern captured the OLD empty value of `newCardColumnID` before the state update propagated.

**Fix:** Changed to `sheet(item:)` pattern which passes the column ID directly when the sheet opens, avoiding the race condition.

Also added:
- Proper error handling (removed `try?` that swallowed errors)
- Defensive FileWatcher improvements (process creates before deletes)