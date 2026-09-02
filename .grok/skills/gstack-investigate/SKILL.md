---
name: gstack-investigate
description: >
  Debug like a detective: reproduce, isolate, name the failing assumption.
  Use for "why is this broken", "bug", "investigate", error messages, white
  screens, wrong dates, wrong yield.
metadata:
  short-description: "Investigate: reproduce, isolate, fix cause"
user-invocable: true
---

# Investigate

1. Reproduce in the running product (browser), not by guessing.
2. Isolate: one occupancy, one house, one path.
3. Name the assumption that died ("leavers list ignores size").
4. Fix the cause. Re-verify the same path.
5. Add a regression check if it would happen again.

Do not shotgun-refactor. Do not blame the user.
