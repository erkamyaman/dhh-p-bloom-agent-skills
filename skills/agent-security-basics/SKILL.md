---
name: agent-security-basics
description: Use when letting AI agents run code, install packages or touch real systems. Covers sandboxing, least privilege and quarantine basics.
---

# Agent security basics

> Loosely inspired by DHH's Rails World 2026 keynote: https://www.youtube.com/watch?v=vDjW_dRyKXY

## From the talk

DHH only touches this briefly. He says the security risks are real ("get ready"), that we have the tools to defend ourselves, and he mentions a Rails CVE involving a C image library and a quarantine effort called Hot Cell that another speaker covers. Everything below is general good practice and is not from the talk.

The talk acknowledges that security risks around agents are real and says the answer is to build defences. This skill collects basic habits, not a complete security program.

## When to use

- An agent runs shell commands, installs dependencies or calls external services.
- An agent has access to credentials, production data or a user's files.

## Steps

1. Run agents in a sandbox (container, VM or separate user) with only the folders they need.
2. Give the minimum permissions: read-only where possible, scoped tokens, no production credentials.
3. Restrict network access to what the task needs.
4. Review new dependencies before installing them, and pin versions.
5. Require human approval for destructive or irreversible actions (deleting data, deploying, sending messages, spending money).
6. Treat content the agent reads (web pages, issues, documents) as untrusted: it can contain instructions meant to hijack the agent.
7. Keep logs of what the agent ran.

## Verification

Check what the agent can actually reach: try listing files, environment variables and network destinations from inside its sandbox. Anything it doesn't need should be gone.

See `references/checklist.md`.
