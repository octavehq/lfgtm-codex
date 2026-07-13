# Octave Codex Plugin

> Generated from [octavehq/lfgtm](https://github.com/octavehq/lfgtm). Do not edit directly — changes will be overwritten. File issues and PRs on the upstream repo.

GTM knowledge base integration for OpenAI Codex CLI.

## Install

Install the skills from this repository using your Codex CLI version's skills/plugin mechanism, for example:

```bash
codex plugin marketplace add https://github.com/octavehq/lfgtm-codex
```

If your Codex version does not support plugin marketplaces, clone this repository and copy the `skills/` directories into your Codex skills location (see `codex --help` or the Codex documentation for the path your version uses).

## Configure your Octave MCP server

Add your workspace's MCP server (one per workspace):

```bash
codex mcp add octave-acme --url https://mcp.octavehq.com/mcp?ctx=<context>
```

Use any name starting with `octave-`. Skills detect the Octave server from available tools.

## Skills

All upstream skills are available, renamed with the `octave-` prefix to avoid collisions in the Codex skill namespace:

- `/octave-research` (was `/octave:research` in Claude Code)
- `/octave-library`, `/octave-generate`, `/octave-battlecard`, …

See the [upstream README](https://github.com/octavehq/lfgtm#skills) for full descriptions.

## Not included

The upstream plugin ships five subagent personas (`octave-assistant`, `pmm-strategist`, `sdr-coach`, `revenue-strategist`, `asset-manager`). Codex has no subagent concept, so these are not available in this build. Use the corresponding skills directly.
