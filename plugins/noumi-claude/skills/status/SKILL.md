---
name: status
description: Check the progress or result of an existing Noumi task or song. Use saved task and song IDs to recover the original request without submitting another generation.
user-invocable: true
---

<!-- Generated from agent-kit; content 5.1.1. Edit canonical sources, then run node scripts/build-agent-kit.mjs. -->

# Recover or inspect an existing song

Verify the connected identity with `noumi_whoami` and read the current `noumi_get_guide` before recovery. Use the actual installed plugin tools and supported schemas. Read [execution and recovery](../song/references/execution.md).

With a saved `queueTaskId`, call `noumi_queue_status` using `taskId`. With a known `songId`, call `noumi_song_status` for that song. If no ID survived a lost response, use the supported latest-status query as a reconciliation clue under the same artist; a latest result alone cannot prove the original submission was rejected. Do not recover by registering again or issuing a new paid creation.

Report queued/processing/done/failed honestly. Only claim a refund when `creditsRefunded` is true in the actual result. On completion deliver the returned message and dashboard link; it is a draft pending the human's publication decision. Cover progress does not block ready audio. Preserve the task ID and a resume route when waiting ends. Content version 5.1.1.
