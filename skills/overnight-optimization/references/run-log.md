# Run log format

```markdown
## Baseline
- metric: <name>, value: <number>, measured with: <command>

## Attempts
| # | Change | Tests | Before | After | Decision |
|---|---|---|---|---|---|
| 1 | Lazy-load charts module | pass | 1.8 MB | 1.5 MB | keep |
| 2 | Replace date library | fail | 1.5 MB | 1.3 MB | revert |

## Summary
- final value: <number>
- changes kept: <count>
```

Rules for the agent: never edit or delete tests to make them pass, never skip the benchmark, and stop after a fixed number of attempts or when the target is reached.
