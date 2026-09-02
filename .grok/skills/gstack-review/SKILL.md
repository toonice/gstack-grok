---
name: gstack-review
description: >
  Pre-landing code review: scope drift, safety, slop, completeness. Use for
  "review this", "code review", "pre-landing", "check the diff".
metadata:
  short-description: "Review: scope, safety, slop, completeness"
user-invocable: true
---

# Review

Read the diff (or the files you just touched). Do not praise.

## Passes

1. **Scope** — did we build the ticket, or a neighbouring product?
2. **Safety** — injection, secrets, LLM trusting the model over the engine, auth boundaries, money/dates.
3. **Slop** — emoji chrome, purple gradients, empty catches, comments that narrate, fake CV copy, unused helpers.
4. **Completeness** — occupancy edge cases, empty states, mobile, the control case that must not lie.

## Findings

`[P0|P1|P2] (confidence n/10) path — fact`

- Auto-fix P2 slop.
- Ask on P0/P1 taste or behaviour.
- User sovereignty on product calls.

End with: `Pre-landing: N issues (X P0)`.
