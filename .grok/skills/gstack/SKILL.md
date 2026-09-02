---
name: gstack
description: >
  Route product work through a virtual team: office hours, CEO/eng plan review,
  spec, investigate, code review, design review, QA, ship. Use when the user
  says gstack, office hours, review this, QA this, ship it, is this worth
  building, think bigger, write a spec, or wants a pre-landing review.
  Methodology from Garry Tan's gstack, redesigned for Grok (no Claude Code,
  no ~/.claude, no slash commands).
metadata:
  short-description: "Grok port of gstack: office hours, review, QA, ship"
user-invocable: true
---

# gstack (Grok host)

This is **not** Claude Code. There is no `/office-hours` slash command and no
`~/.claude/skills/gstack` binaries. The factory is these skills. **Read the
matching skill and follow it** instead of answering ad hoc.

| User intent | Skill to open |
|---|---|
| New idea, worth building, brainstorm | `gstack-office-hours` |
| Think bigger, scope, ambition | `gstack-ceo` |
| Architecture, is this the right shape | `gstack-eng` |
| Write a spec / ticket | `gstack-spec` |
| Bug, why broken | `gstack-investigate` |
| Code review, diff, pre-landing | `gstack-review` |
| Visual polish, design audit | `gstack-design-review` |
| Test it like a user | `gstack-qa` |
| Ship, PR, deploy, land it | `gstack-ship` |
| Weekly look-back | `gstack-retro` |
| Slow down, high-stakes | `gstack-careful` |

When in doubt, open the skill. False positives beat unstructured answers.

## Tool map (Claude → Grok)

- Web: `web_search`, `browse_page` — never Claude-in-Chrome MCP
- In-app QA: `agent-browser` against the live preview — never ask the user to click around
- Parallel specialists: `task` subagents, then you integrate
- LLM in the *product*: `xai-api` skill + `XAI_API_KEY`, not Anthropic
- Persistence: repo files / localStorage. No `~/.gstack` telemetry daemons.

## Ethos (keep)

- **User sovereignty** — recommend, they decide.
- **Search before building.**
- **Completeness is cheap** — do the whole thing, one lake at a time.
- Direct voice. No filler. End on an action.

## Do not

- Install bun into `~/.claude` or run gstack `./setup`
- Invent slash commands
- Block App Builder preview work: if this workspace is shipping an app, QA and ship mean verify the running product, not open a GitHub PR unless they asked
