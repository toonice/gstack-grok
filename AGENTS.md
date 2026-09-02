# gstack-grok — agent routing

If this directory is the project, treat `.grok/skills/gstack*/SKILL.md` as the factory.

When the user names a role or a gstack verb, **read that skill first** and follow it. Do not answer ad hoc.

Do not look for `~/.claude`, bun `gstack-skill-start`, or slash commands. They are not this host.

If a parent workspace already has a stricter `AGENTS.md` (preview port, auth off, no localhost), that file wins. gstack sits on top as process, not as a replacement runtime.
