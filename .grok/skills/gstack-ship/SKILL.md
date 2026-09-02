---
name: gstack-ship
description: >
  Ship gate: typecheck, build, review, QA, then land. Use for "ship it",
  "create a PR", "deploy", "land this", "push to github".
metadata:
  short-description: "Ship: tests, review, QA, then land"
user-invocable: true
---

# Ship

Never skip: typecheck, production build, a real browser pass, review findings
closed or explicitly accepted.

## Gates

1. `gstack-review` on the change
2. `gstack-qa` on the running product
3. Typecheck + build must pass
4. If they asked for GitHub: push only what they named, no CV copy, no secrets
5. Stop on merge conflicts, test fail, or unanswered P0

If this is App Builder: shipping means the preview works, not that you invented
a `gh pr`. Only open/push GitHub when the user asked and the GitHub tool is
connected.

Do not bump random VERSION files that do not exist.
