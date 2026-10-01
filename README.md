# dhh-p-bloom-agent-skills

Agent skills for working with AI coding agents, based on the points made in the opening keynote at Rails World 2026.

Each skill is a folder with a `SKILL.md` (orientation) and a `references/` folder (focused topic files), in the same layout as [ionic-capacitor-skills](https://github.com/erkamyaman/ionic-capacitor-skills).

## Install

```bash
npx skills add erkamyaman/dhh-p-bloom-agent-skills
```

## Skills

| Skill | What it teaches the agent |
|---|---|
| `outcome-prompting` | Turn a task into a problem-and-outcome brief instead of step-by-step instructions |
| `async-delegation` | Split work into parallel tasks, hand them off, and review in batches |
| `black-box-review` | Check agent output through tests and behaviour instead of reading every line |
| `native-vs-web` | Decide what should be native and what should stay web (fits Ionic/Capacitor) |
| `cli-for-your-app` | Give an app a CLI so a user's own agent can drive it |
| `agent-evals` | Write a small eval set, run agents on it, and raise the difficulty once they pass |
| `overnight-optimization` | Benchmark-driven optimization runs with a "tests must still pass" gate |
| `architecture-for-agents` | When duplication beats abstraction, and where it breaks |
| `agent-security-basics` | Sandboxing and quarantine basics when agents run code |

## Source

These skills are inspired by the opening keynote at Rails World 2026 by David Heinemeier Hansson (DHH):
https://www.youtube.com/watch?v=vDjW_dRyKXY

They are our own interpretation of the points he made, written in our own words. They are not affiliated with or endorsed by DHH or 37signals.

## About the name

"p-bloom" plays on "p(doom)", the AI-safety shorthand for the probability of catastrophe. In the talk, DHH argues for optimism and contrasts "pee bloom" with "pee doom". The exact spelling comes from auto-generated subtitles, and we don't claim he coined the term.

## A note on the claims

Many of the talk's points are opinions and personal experience, not measured results. Each skill therefore includes a verification step (tests, a benchmark, or a review gate) instead of trusting the claim.

## Contributing

Create a `skills/<skill-name>/` folder with a `SKILL.md` and focused reference files, then add it to `package.json`.

## License

MIT
