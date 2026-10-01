# Red flags to scan for in a diff

- New dependencies you didn't ask for.
- Network calls to unfamiliar hosts.
- Secrets, tokens or keys in code or config.
- Disabled or deleted tests, or tests that assert nothing.
- Broad error swallowing (empty catch blocks, ignored results).
- Changes to files outside the task's scope (CI config, lockfiles, auth).
- Hard-coded values that should be configuration.
- Large copy-pasted blocks that differ in small ways (may hide a subtle bug in one copy).
