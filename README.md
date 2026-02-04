# Supabase Extension for Gemini CLI

The Supabase extension for [Gemini CLI](https://github.com/google-gemini/gemini-cli) gives Gemini the tools, skills, and context needed to work effectively with Supabase projects.

## Installation

```bash
gemini extensions install https://github.com/supabase-community/gemini-extension
```

## What's Included

- **MCP Server** — Remote connection to the [Supabase MCP server](https://supabase.com/mcp) for project management, SQL execution, migrations, and more
- **Skills** — Agent skills from [supabase/agent-skills](https://github.com/supabase/agent-skills) (e.g. `postgres-best-practices`)
- **Context** — `SUPABASE.md` with CLI usage patterns and best practices

## Development

Install development tools with [mise](https://mise.jdx.dev/):

```
mise install
```

This repo uses a git submodule for shared agent skills.

After cloning, initialize the submodule:

```bash
git submodule update --init --recursive
```

To test locally:

```bash
gemini extensions install .
```

To update the submodule:

```bash
git submodule update --remote submodules/agent-skills
git add submodules/agent-skills
git commit -m "chore: update agent-skills submodule"
```
