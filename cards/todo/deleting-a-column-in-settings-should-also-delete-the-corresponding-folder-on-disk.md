---
title: deleting a column in settings should also delete the corresponding folder on disk
column: todo
position: zyym
created: 2026-01-06T10:59:47Z
modified: 2026-01-06T11:00:05Z
labels: [improvement, important]
---

i just deleted 'in progress' and on disk the cards/in-progress folder remains. code should check if its empty and delete it if there are no files in it anymore. just warn "could not delete {folder}. not empty." on not empty and dont do anything else.