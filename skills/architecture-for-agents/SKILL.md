---
name: architecture-for-agents
description: Use when structuring a codebase that AI agents will edit heavily. Weighs duplication against abstraction now that repeating code and keeping copies in sync is cheap.
---

# Architecture for agents

> Inspired by DHH's Rails World 2026 keynote: https://www.youtube.com/watch?v=vDjW_dRyKXY

## From the talk

DHH says abstractions make less sense when hundreds or thousands of agents may be changing an app, because the choke points they create get in the way. He also says the cost of repetition and of keeping copies in sync has dropped to near zero, and that no one has the blueprint yet. The decision table and steps below are our additions, not from the talk.

The talk argues that part of the reason for abstractions (not repeating yourself) weakens when agents can change many places quickly, and that shared choke points can slow down many agents working at once. Treat this as a hypothesis to test, not a rule.

## When to use

- Deciding whether to extract a shared helper, base class or service.
- A codebase is hard for agents to change because everything depends on one module.

## Steps

1. Find the choke points: modules that many features depend on and that change often.
2. For each, ask: does sharing this code save real effort, or does it only avoid repetition?
3. Prefer small, clear, self-contained modules with explicit boundaries and good tests.
4. Allow duplication when copies are small, stable and covered by tests. Keep abstraction where the logic is subtle or must stay consistent (security, money, data rules).
5. Name things clearly and keep a short architecture note in the repo so agents and people share the same map.

## Verification

Pick a typical change and let an agent make it. Count the files it had to touch and the tests that broke. If one shared module caused most of the pain, reconsider it.

See `references/duplicate-or-abstract.md`.
