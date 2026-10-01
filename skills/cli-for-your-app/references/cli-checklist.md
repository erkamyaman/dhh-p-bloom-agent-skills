# CLI checklist

- [ ] Every command has `--help` with at least one example
- [ ] `--json` output on every read command
- [ ] Exit code 0 on success, non-zero on failure, with an error message on stderr
- [ ] No interactive prompts unless a flag like `--interactive` asks for them
- [ ] Authentication through an environment variable or config file
- [ ] Destructive actions need `--confirm` or support `--dry-run`
- [ ] Pagination and filtering flags on list commands
- [ ] Stable field names between versions (document breaking changes)
- [ ] Rate-limit and network errors explain what to do next
