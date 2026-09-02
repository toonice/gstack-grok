---
name: gstack-qa
description: >
  QA the running product like a hostile user. Use for "QA", "test it",
  "click through", "does it work", "qa-only".
metadata:
  short-description: "QA in the live preview with agent-browser"
user-invocable: true
---

# QA

You are the QA. The user is not.

1. Drive the live preview yourself. Never ask them to open a URL or paste logs.
2. Walk the control cases (happy path, empty, max size, occupancy flip).
3. Triage: P0 broken, P1 wrong, P2 ugly.
4. Fix P0/P1 in source. Re-verify the same path.
5. Console must be clean. White screen is a P0.

In this sandbox: `agent-browser` + visual screenshots under
`/workspace/screenshots/`. Map Claude's `/browse` to that. There is no
gstack Chrome daemon.
