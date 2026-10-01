# Security checklist

- [ ] Agent runs in a sandbox, not directly on a main machine
- [ ] Only needed folders are mounted
- [ ] No production secrets in the environment
- [ ] Tokens are scoped and short-lived
- [ ] Network access is limited to an allowlist
- [ ] New dependencies are reviewed and versions pinned
- [ ] Destructive actions need human approval
- [ ] Web pages, issues and documents are treated as untrusted input
- [ ] Commands and file changes are logged
- [ ] Changes are reviewed before merging or deploying
