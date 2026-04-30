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
| [otel-propagators](./skills/otel-propagators/) | Configure OpenTelemetry context propagation (OTEL_PROPAGATORS) for services |

## Usage

Skills are automatically available once installed. The agent will use them when relevant tasks are detected.

**Examples:**
- "Set OTEL_PROPAGATORS for my service"
- "How do I configure W3C tracecontext and B3 propagation together?"
- "Make sure downstream services see the right trace context"

## Skill Structure

Each skill contains:
- `SKILL.md` - Instructions for the agent
- `scripts/` - Helper scripts for automation (optional)
- `references/` - Supporting documentation (optional)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
