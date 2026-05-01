# Observability Skills

A collection of skills for AI coding agents covering observability, tracing, and OpenTelemetry workflows. Skills are packaged instructions and scripts that extend agent capabilities.

Skills follow the [Agent Skills format](https://agentskills.io/home).

## Installation

### Using npx (requires Node.js)

```bash
npx skills add metalbear-co/observability-skills
```

### Claude Code plugin

```bash
/plugin marketplace add metalbear-co/observability-skills
```

## Available Skills

| Skill | Description |
|-------|-------------|
| [setup-otel-propagation](./skills/setup-otel-propagation/) | Configure OpenTelemetry context propagation (OTEL_PROPAGATORS) for services |

## Usage

Skills are automatically available once installed. The agent will use them when relevant tasks are detected.

**Examples:**
- "Set OTEL_PROPAGATORS for my service"
- "How do I configure W3C tracecontext and B3 propagation together?"
- "Make sure downstream services see the right trace context"

## Skill Structure

Each skill lives in its own directory under `skills/` and contains:

- `SKILL.md` — frontmatter (`name`, `description`, `metadata`) plus instructions for the agent
- `scripts/` — helper scripts for automation (optional)
- `references/` — supporting documentation the agent can read (optional)

```
skills/
└── setup-otel-propagation/
    ├── SKILL.md
    └── references/
```

## Adding a New Skill

1. **Create the directory** — `mkdir skills/<your-skill-name>`.
2. **Write `SKILL.md`** — start with frontmatter, then the body. The `name` must match the
   directory name; the `description` is what the agent matches on to decide when to fire, so
   make it specific (list trigger phrases, tools, env vars, error messages).
   ```markdown
   ---
   name: your-skill-name
   description: >
     One paragraph telling the agent exactly when to invoke this skill...
   metadata:
     author: MetalBear
     version: "0.1"
   ---

   # Skill Title
   ...
   ```
3. **Register it** in [`.claude-plugin/marketplace.json`](./.claude-plugin/marketplace.json) by
   adding `"./skills/<your-skill-name>"` to the `plugins[0].skills` array.
4. **Document it** by adding a row to the *Available Skills* table above.
5. **Bump the version** in `marketplace.json` and `.claude-plugin/plugin.json` if this is a
   user-visible change.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
