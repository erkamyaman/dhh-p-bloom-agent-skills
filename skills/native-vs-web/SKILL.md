---
name: native-vs-web
description: Use when deciding whether an app should be native, web, or hybrid (Ionic/Capacitor) now that agents make native code cheaper to produce.
---

# Native vs web

> Inspired by DHH's Rails World 2026 keynote: https://www.youtube.com/watch?v=vDjW_dRyKXY

## From the talk

DHH says Hey is being rebuilt as native apps because agents have cut the cost of native development, and he cites Shopify's rewrite of its Shop app as native. He says the web remains best when users won't install anything, such as Basecamp's guests, and admits he doesn't have all the answers on where to draw the line. The decision table and steps below are our additions. Ionic and Capacitor are not discussed in the talk.

The talk argues that web apps were often chosen because small teams couldn't afford several native apps, and that agents are shrinking that cost. This skill helps you re-check the decision per app instead of assuming the old answer.

## When to use

- Starting a new app or a major rewrite.
- An existing hybrid app has hit performance, fidelity or platform-feature limits.

## Steps

1. List what the app needs: offline, background work, push, sensors, widgets, system integration, startup speed.
2. Ask who uses it: returning users who will install it, or one-time visitors who won't.
3. Score each option (web, hybrid with Capacitor, fully native) against the list using `references/decision-table.md`.
4. Estimate the maintenance cost honestly: number of platforms, number of people who can review the code.
5. Prototype the riskiest screen in the leading option and measure it before committing.

## Verification

Compare the prototype to the current app on startup time, scrolling smoothness and the platform features that matter. If the gain is small, stay with what you have.

## Caveat

"Native is now nearly free" is a claim from the talk, not a measured fact. Agent-written native code still needs testing, store review and long-term maintenance.
