# Octave Codex Plugin

> Generated from [octavehq/lfgtm](https://github.com/octavehq/lfgtm). Do not edit directly — changes will be overwritten. File issues and PRs on the upstream repo.

GTM knowledge base integration for OpenAI Codex CLI.

## Install

Install the skills from this repository using your Codex CLI version's skills/plugin mechanism, for example:

```bash
codex plugin marketplace add https://github.com/octavehq/lfgtm-codex
```

If your Codex version does not support plugin marketplaces, clone the complete repository and use your host’s supported skill discovery or symlinks. Keep skills/shared, sibling skills, agents, root scripts and LICENSE together; copying isolated skill folders breaks dependencies.

## Configure your Octave MCP server

Add your workspace's MCP server (one per workspace):

```bash
codex mcp add octave-acme --url https://mcp.octavehq.com/mcp?ctx=<context>
```

Use any name starting with `octave-`. Skills detect the Octave server from available tools.

## Skills

All upstream skills are available, renamed with the `octave-` prefix to avoid collisions in the Codex skill namespace:

- `/octave-research` (was `/octave:research` in Claude Code)
- `/octave-library`, `/octave-generate`, `/octave-battlecard-doc`, …

See the [upstream README](https://github.com/octavehq/lfgtm#skills) for full descriptions.

## Review and runtime resources

All seven upstream agent instruction files and root helper scripts are included.
Use supported host delegation when available; otherwise run the packaged reviewer
instructions sequentially. See skills/shared/host-runtime.md.

