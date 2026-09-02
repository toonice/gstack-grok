---
name: gstack-careful
description: >
  High-stakes mode: slow down, smaller diffs, no drive-by refactors, confirm
  before destructive git or data changes. Use for "be careful", "production",
  "don't break it", "guard", "freeze".
metadata:
  short-description: "Careful: small diffs, confirm destructive moves"
user-invocable: true
---

# Careful

- One concern per change.
- No unrelated refactors.
- Confirm before dropping tables, force-push, or rewriting legal copy.
- Prefer a failing test you can see over a theory.

Unfreeze when they say the stakes are normal again.
