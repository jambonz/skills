# jambonz Agent Skills

[Agent Skills](https://agentskills.io) for building voice applications on [jambonz](https://jambonz.org).

## Available Skills

| Skill | Description |
|-------|-------------|
| [`jambonz`](jambonz/) | Build voice applications on jambonz — verb model, transport selection, IVR, AI voice agents, call routing, recording, and more |

## Installation

### Using the skills CLI (recommended)

Works with Claude Code, Cursor, VS Code Copilot, and other [compatible agents](https://agentskills.io):

```bash
npx skills add jambonz/skills
```

Add `--global` to install for all projects:

```bash
npx skills add jambonz/skills --global
```

### Manual installation

Copy the `jambonz/` folder to your agent's skills directory:

| Agent | Path |
|-------|------|
| Claude Code | `.claude/skills/jambonz/` |
| Cursor | `.cursor/skills/jambonz/` |
| VS Code Copilot | `.vscode/skills/jambonz/` |
| Cross-client | `.agents/skills/jambonz/` |

## Using with the MCP Server

For the best experience, pair this skill with the [jambonz MCP server](https://www.npmjs.com/package/@jambonz/mcp-schema-server). The skill provides **decision-making guidance** (which verbs to use, which transport, common patterns), while the MCP server provides **schema lookups and SDK reference**.

Add to your project's `.mcp.json`:

```json
{
  "mcpServers": {
    "jambonz": {
      "command": "npx",
      "args": ["-y", "@jambonz/mcp-schema-server"]
    }
  }
}
```

## Language Support

The skill is language-neutral. It works with:

- **TypeScript** via `@jambonz/sdk` (recommended)
- **Python, Go, or any language** via raw JSON verb arrays over HTTP webhooks or WebSocket

## Source

This skill is maintained in the [jambonz/agent-toolkit](https://github.com/jambonz/agent-toolkit) monorepo alongside the SDK and MCP server.

## License

MIT
