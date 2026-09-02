# gstack-grok

Garry Tan's [gstack](https://github.com/garrytan/gstack) factory, redesigned so **Grok** can actually run it.

The original installs into `~/.claude/skills` and is invoked as Claude Code slash commands (`/office-hours`, `/ship`, …). Grok does not load those. This port is Grok skills: YAML frontmatter, trigger text, tools Grok has.

Not affiliated with YC. Methodology is gstack's (MIT). The host is new.

## What you get

A virtual team, without Claude:

| Skill | Job |
|---|---|
| `gstack` | Router |
| `gstack-office-hours` | YC office hours (no code) |
| `gstack-ceo` | Scope / ambition |
| `gstack-eng` | Architecture |
| `gstack-spec` | Ticket with acceptance tests |
| `gstack-investigate` | Reproduce, then fix |
| `gstack-review` | Pre-landing review |
| `gstack-design-review` | Taste / anti-slop |
| `gstack-qa` | Hostile user in the live preview |
| `gstack-ship` | Gates, then land |
| `gstack-retro` | What lied |
| `gstack-careful` | Small diffs |

Dropped on purpose: Chrome MCP, bun daemons, `~/.gstack` telemetry, iOS QA, Codex CLI, `./setup` into `~/.claude`.

## Install

Copy `.grok/skills/gstack*` into a Grok coding / App Builder workspace:

```
.grok/skills/gstack/SKILL.md
.grok/skills/gstack-office-hours/SKILL.md
…
```

Keep the workspace `AGENTS.md` if the host already has one (App Builder must). This pack does not replace it.

Say **gstack**, **office hours**, **review this**, **QA**, or **ship it**. The router table in `gstack` is the map.

## Tool map

| gstack (Claude) | Grok |
|---|---|
| `/browse`, Chrome MCP | `browse_page`, `web_search`, `agent-browser` |
| Skill tool + slash commands | Open the matching `SKILL.md` |
| `codex` second opinion | `task` subagent |
| Anthropic API | xAI (`grok-4.5`) via the xai-api skill |

## Ethos

User sovereignty. Search before building. Completeness is cheap. See `ETHOS.md`.
