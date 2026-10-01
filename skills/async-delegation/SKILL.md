---
name: async-delegation
description: Use when you have several independent jobs for AI agents. Splits work into parallel tasks, hands them off like to coworkers, and reviews results in batches.
---

# Async delegation

> Inspired by DHH's Rails World 2026 keynote: https://www.youtube.com/watch?v=vDjW_dRyKXY

## From the talk

DHH says the best way to work with agents is asynchronously: give a task like you would to a coworker, send the agent off, and review when something is ready, instead of sitting in a chat waiting for output. Splitting into parallel tasks, batch sizes and review order below are our additions, not from the talk.

Treat agents like coworkers: give a clear task, send them off, and review when something is ready. Don't sit watching tokens stream in a chat.

## When to use

- Three or more tasks that don't depend on each other.
- A task that will take longer than a few minutes.

## Steps

1. List the tasks and mark which are independent. Only independent tasks run in parallel.
2. Give each task its own brief (see `outcome-prompting`) and its own branch or workspace so changes don't collide.
3. Start them all, then do something else.
4. Review in one batch: read each result against its acceptance checks before merging anything.
5. Send corrections as a short follow-up to the same task, not a fresh start.

## Verification

Before merging, run the full test suite on the combined result, not only on each branch alone. Parallel changes can pass separately and still conflict.

See `references/batching.md` for how to size tasks and batches.
