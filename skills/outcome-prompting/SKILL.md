---
name: outcome-prompting
description: Use when giving an AI coding agent a job. Turns a task into a problem-and-outcome brief with acceptance checks, instead of step-by-step instructions.
---

# Outcome prompting

> Inspired by DHH's Rails World 2026 keynote: https://www.youtube.com/watch?v=vDjW_dRyKXY

## From the talk

DHH says agents can now be given problems or outcomes instead of tasks. He warns against being overly prescriptive: a beginner's mindset and higher-level prompts work better. The brief format, acceptance checks and template below are our additions, not from the talk.

Describe the problem and the result you want. Let the agent choose the implementation. Over-specifying steps caps the agent at your own knowledge.

## When to use

- Starting any feature, fix or refactor with an agent.
- A previous prompt was a long list of steps and the result was mediocre.

## Steps

1. Write the **problem** in one or two sentences (who is affected, what hurts).
2. Write the **outcome** as observable behaviour ("a user can ... and sees ...").
3. List **constraints** only where they really exist (platform, API limits, style rules, files not to touch).
4. Add **acceptance checks** the agent can run itself (tests, a command, a screenshot comparison).
5. Leave the implementation open. Do not name functions, files or libraries unless required.

## Verification

Run the acceptance checks. If they pass but the behaviour is wrong, the checks were too weak: tighten them and re-run instead of adding more steps to the prompt.

See `references/brief-template.md` for a fill-in template.
