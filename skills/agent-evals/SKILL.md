---
name: agent-evals
description: Use when measuring how well an AI agent handles a recurring kind of task. Builds a small eval set, runs it, and raises the difficulty once the agent passes.
---

# Agent evals

> Inspired by DHH's Rails World 2026 keynote: https://www.youtube.com/watch?v=vDjW_dRyKXY

## From the talk

DHH mentions agent evals for Rails run by Evil Martians for the Rails Foundation. Agents saturated the first version (about 95% completion), so a harder one was made. The steps, task counts and thresholds below are our additions, not from the talk.

The talk mentions an agent benchmark for Rails that agents saturated quickly, so it was made harder. The lesson: evals have a shelf life, and you need to keep raising the bar.

## When to use

- You rely on agents for a recurring task (for example, adding features to your app).
- You want to compare models, prompts or skills.

## Steps

1. Pick 10 to 20 realistic tasks from your own work.
2. For each, write a pass/fail check that doesn't depend on a human reading the output (tests, a script, a diff against expected behaviour).
3. Run the agent on every task from a clean state and record pass or fail.
4. Look at failures first: was it the agent, the prompt, or a bad check?
5. When the pass rate is consistently high (say above 90%), add harder tasks.

## Verification

Run the same eval twice. If results differ a lot between runs, the checks or tasks are too noisy to trust.

See `references/eval-template.md`.
