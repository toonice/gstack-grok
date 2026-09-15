---
name: skill-bridge
description: Analyse a GitHub repository and turn its reusable capability into a Grok-compatible skill.
when-to-use: GitHub skill, import repo, bridge skill, convert Claude skill, adapt repository
user-invocable: true
metadata:
  author: Grok Skill Bridge
  short-description: Bridge useful GitHub capabilities into Grok
---

# Grok Skill Bridge

When given a GitHub repository, determine what useful capability it provides and how Grok can use it.

## Rules
1. Inspect README, manifests, skills, MCP configuration, agent instructions, examples, scripts and tests.
2. Identify agent-specific components versus reusable implementation.
3. Prefer direct reuse when Grok already supports the same format.
4. Generate or adapt a `SKILL.md` using Grok's skill format when appropriate.
5. If an MCP server already exists, prefer its native MCP interface rather than rewriting it.
6. Never bypass authentication, access controls or repository licence restrictions.
7. Before installing dependencies or executing code from an untrusted repository, explain the risk and request approval.
8. Produce a compatibility summary and a test plan.
