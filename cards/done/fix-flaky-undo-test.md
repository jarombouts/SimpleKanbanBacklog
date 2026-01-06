---
title: Fix flaky multipleUndoOperations test
column: done
position: t
created: 2026-01-07T01:00:00Z
modified: 2026-01-07T01:05:00Z
labels: [bug]
---

## Description

Fixed the intermittently failing `BoardStoreUndoTests.multipleUndoOperations()`
test that was causing test suite failures.

## Root Cause

UndoManager's `groupsByEvent` property (default: true) relies on run loop
events to determine undo group boundaries. Swift Testing doesn't provide
consistent run loop behavior like AppKit does, causing operations to
sometimes be grouped incorrectly.

## Fix

- Set `undoManager.groupsByEvent = false` to disable automatic grouping
- Use explicit `beginUndoGrouping()` / `endUndoGrouping()` calls for each
  operation to ensure proper isolation
- This makes the test deterministic regardless of run loop state

## Verification

Test passed 3/3 consecutive runs after the fix (previously ~50% failure rate).
