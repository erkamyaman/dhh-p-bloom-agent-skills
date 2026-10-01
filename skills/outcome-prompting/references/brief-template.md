# Brief template

```markdown
## Problem
<who is affected and what goes wrong or is missing>

## Outcome
<what is true when this is done, in observable terms>

## Constraints
- <only real ones>

## Acceptance checks
- <command or test that must pass>
- <behaviour to confirm manually or by screenshot>

## Out of scope
- <things the agent should not touch>
```

## Before and after

Step-by-step (avoid): "Create a service, inject it in the component, add a method that calls the endpoint, then add a loading flag..."

Outcome-level (prefer): "Users on the orders page see a loading state while data loads and a retry button if the request fails. Existing tests pass and a new test covers the failure case."
