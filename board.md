---
title: SimpleKanban Backlog
columns:
  - id: todo
    name: To Do
  - id: in-progress
    name: In Progress
  - id: done
    name: Done
labels:
  - id: important
    name: Important
    color: "#40ff20"
  - id: improvement
    name: Improvement
    color: "#557711"
  - id: feature
    name: Feature
    color: "#3498db"
  - id: bug
    name: Bug
    color: "#e74c3c"
  - id: docs
    name: Docs
    color: "#9b59b6"
  - id: refactor
    name: Refactor
    color: "#27ae60"
  - id: wontdo
    name: Won't Do
    color: "#95a5a6"
---

# SimpleKanban Backlog

This is our own backlog for SimpleKanban development — we dogfood our own tool to plan and track features.

**Location:** This board lives in its own repository at `../SimpleKanbanBacklog` (separate from the main SimpleKanban project repo). This demonstrates the recommended setup: one repo per board for clean git sync.

Using SimpleKanban to manage SimpleKanban lets us:
- Experience the tool as real users do
- Discover pain points and missing features firsthand
- Test the git sync feature with a real remote
- Demonstrate the git-based workflow we're building for

## Card Template

New cards should follow this structure:

## Description

What needs to be done and why.

## Requirements

- Specific, testable requirements
- Acceptance criteria

## Notes

Implementation notes, related files, or context.
