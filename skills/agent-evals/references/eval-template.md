# Eval template

```markdown
## Task <id>
Prompt: <exactly what the agent is given>
Starting state: <repo commit or fixture>
Pass check: <command that exits 0 on success>
Difficulty: easy | medium | hard
Notes: <known pitfalls>
```

## Results table

| Task | Run 1 | Run 2 | Notes |
|---|---|---|---|
| 01 | pass | pass | |
| 02 | fail | pass | flaky check? |

## Raising the bar

- Combine two tasks into one.
- Remove hints from the prompt.
- Use a larger or messier codebase.
- Add a performance or size requirement to the pass check.
