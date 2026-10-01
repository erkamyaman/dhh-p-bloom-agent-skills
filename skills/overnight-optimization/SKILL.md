---
name: overnight-optimization
description: Use when you want an AI agent to improve performance, size or startup time of a project over a long unattended run, with tests as a safety gate.
---

# Overnight optimization

> Inspired by DHH's Rails World 2026 keynote: https://www.youtube.com/watch?v=vDjW_dRyKXY

## From the talk

DHH says every optimization is now within reach: models can run overnight and deliver improvements of roughly 10x to 30x (per the auto-generated subtitles). He points to his half-megabyte Hype presentation app and the large CPU and memory savings estimated for Hey's Rust backend. The guardrails, log and steps below are our additions, not from the talk.

The talk's point: optimizations that no human had time for are now within reach if you let an agent work through them unattended. The risk is breaking behaviour, so the run needs a measurable target and a hard safety gate.

## When to use

- A project has a clear metric (bundle size, startup time, request latency, memory).
- You have tests that give you real confidence.

## Steps

1. Measure the baseline and save the numbers to a file.
2. Define the target ("cut bundle size by 20%") and the guardrails ("all tests pass, no visible behaviour change").
3. Tell the agent to work in small steps: one change, run tests, run the benchmark, keep or revert.
4. Have it log every attempt (what changed, before and after numbers, kept or reverted).
5. Run it in its own branch.

## Verification

In the morning, re-run the tests and the benchmark yourself and compare to the baseline. Read the log and review every kept change before merging.

See `references/run-log.md`.
