# Duplicate or abstract?

| Question | If yes | If no |
|---|---|---|
| Must all copies behave identically (security, money, validation)? | Abstract | Duplication is acceptable |
| Is the logic subtle or easy to get wrong? | Abstract | Duplication is acceptable |
| Do many features change this code at the same time? | Consider splitting it up | Keep as is |
| Are the copies small and covered by tests? | Duplication is acceptable | Abstract or add tests |
| Would a change need edits in more than 5 places? | Add a check that finds drift between copies | Fine |

Drift check idea: a test or script that compares the copies and fails if they diverge unexpectedly.
