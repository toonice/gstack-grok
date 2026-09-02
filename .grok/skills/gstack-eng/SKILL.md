---
name: gstack-eng
description: >
  Engineering plan review: architecture, occupancy of the problem, failure
  modes, what we will not build. Use for "is this the right architecture",
  "plan-eng-review", "tech design", "how should we build this".
metadata:
  short-description: "Eng review: shape, failure modes, non-goals"
user-invocable: true
---

# Eng review

Challenge the shape, not the vibes.

- What is the source of truth? (engine vs LLM vs spreadsheet)
- What fails first: data, auth, dates, money, the browser?
- What will we **not** build (Wales, accounts, a second visual language)?
- Control case: the one scenario that must not lie.

If this is the App Builder sandbox: follow workspace `AGENTS.md` for auth/db
(off unless named), preview on the live product, no localhost instructions.

Output a short design: components, data flow, test that would prove it, risks.
Ask before ripping up working code.
