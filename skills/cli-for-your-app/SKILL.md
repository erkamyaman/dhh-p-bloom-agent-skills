---
name: cli-for-your-app
description: Use when making an app or library usable by a person's own AI agent. Designs a command-line interface so agents can drive the app without a built-in chatbot.
---

# CLI for your app

> Inspired by DHH's Rails World 2026 keynote: https://www.youtube.com/watch?v=vDjW_dRyKXY

## From the talk

DHH says he doesn't want in-app chatbots. He wants to bring his own agent and let it use apps through a CLI, and he jokingly demands one from every app "by next Friday". He cites the Hey CLI as an example. The CLI design details below are our additions, not from the talk.

The talk's view: instead of adding a chatbot to every app, let users bring their own agent and give it a command line to your app. A good CLI is also easy for humans and scripts to use.

## When to use

- Your app has actions users repeat or want to automate.
- You're tempted to add an in-app assistant.

## Steps

1. List the app's main read and write actions (list, show, create, update, search).
2. Map each to a command with predictable names: `app <noun> <verb>`.
3. Make output easy to parse: a `--json` flag, stable field names, and clear exit codes.
4. Handle auth without prompts that block an agent (token via environment variable or config file).
5. Add `--help` text with an example for every command.
6. Make destructive commands explicit (`--confirm` or a dry-run flag).

## Verification

Give an agent only the CLI's `--help` output and a task. If it completes the task without extra hints, the CLI is clear enough. Fix whatever it got stuck on.

See `references/cli-checklist.md`.
