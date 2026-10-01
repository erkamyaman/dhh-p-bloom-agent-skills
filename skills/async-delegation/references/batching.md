# Batching tasks

## Sizing a task

- Small enough to review in one sitting (roughly one reviewable pull request).
- Large enough to have a clear outcome. "Rename a variable" is too small to delegate; "make the settings page work offline" is a fair size.

## Sizing a batch

- Start with 3 to 5 parallel tasks. More than you can review carefully just moves the bottleneck to you.
- If tasks touch the same files, run them one after another instead.

## Review order

1. Failing checks first.
2. Riskiest change next (data, auth, payments).
3. Cosmetic changes last.

## Signals a task was delegated badly

- The agent asks the same clarifying question twice (the brief was vague).
- The result passes tests but misses the point (the acceptance checks were weak).
- Two results edit the same file (the split was wrong).
