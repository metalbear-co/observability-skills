# Skills

Each subdirectory here is a single Agent Skill — a `SKILL.md` plus optional `references/`
and `scripts/`. Skills are auto-loaded by Claude Code when this repo is installed as a plugin.

## Index

| Skill | Description |
|-------|-------------|
| [setup-otel-propagation](./setup-otel-propagation/) | Configure OpenTelemetry context propagation (`OTEL_PROPAGATORS`) for services, especially when using mirrord. |

## Adding a new skill

See the top-level [README](../README.md#adding-a-new-skill) for the full checklist. Short version:

1. `mkdir skills/<your-skill-name>`
2. Write `SKILL.md` with frontmatter (`name`, `description`, `metadata`).
3. Register the path in [`.claude-plugin/marketplace.json`](../.claude-plugin/marketplace.json).
4. Add a row to the table above and to the top-level README's *Available Skills* table.
