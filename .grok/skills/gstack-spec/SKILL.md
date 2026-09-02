---
name: gstack-spec
description: >
  Turn a decision into a spec / ticket: problem, occupancy of the user,
  acceptance tests, non-goals. Use for "write a spec", "file a ticket",
  "spec this out".
metadata:
  short-description: "Spec: problem, tests, non-goals"
user-invocable: true
---

# Spec

Write `docs/spec.md` (or append). No code.

```
# Title
Problem
User / job
In scope
Out of scope
Acceptance (given / when / then)
Risks
Next skill (eng | qa | build)
```

Acceptance tests must be observable in the running product, not "code exists".
