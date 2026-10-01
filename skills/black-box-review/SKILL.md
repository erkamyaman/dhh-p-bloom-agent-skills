---
name: black-box-review
description: Use when reviewing code an AI agent wrote, especially in a language or area you don't know well. Judges the result through tests and behaviour instead of reading every line.
---

# Black-box review

> Inspired by DHH's Rails World 2026 keynote: https://www.youtube.com/watch?v=vDjW_dRyKXY

## From the talk

DHH says he doesn't know Rust and evaluates what the agents produce as a black box from the outside, the way a business owner judges work from commissioned programmers. The testing steps, red flags and security caveat below are our additions, not from the talk.

Judge agent output from the outside, the way a business owner judges work from a dev team: does it do what was asked, reliably, and fast enough?

## When to use

- Code in a language or framework you don't read fluently.
- Large agent-generated changes where line-by-line review isn't practical.

## Steps

1. Run the existing tests. Add tests for the new behaviour before trusting it.
2. Exercise the real behaviour: run the app, call the endpoint, use the CLI.
3. Measure what matters: speed, memory, bundle size, startup time.
4. Check the edges: empty input, large input, failures, offline.
5. Scan the diff for red flags only (see `references/red-flags.md`), not for style.

## Verification

Black-box review is weaker than reading the code. For anything touching security, money or user data, also have a person who knows the language review those parts.
