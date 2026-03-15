# jambonz Agent Skills

[Agent Skills](https://agentskills.io) for building voice applications on [jambonz](https://jambonz.org).

## Available Skills

| Skill | Description |
|-------|-------------|
| [`jambonz`](jambonz/) | Build voice applications on jambonz — verb model, transport selection, IVR, AI voice agents, call routing, recording, and more |

## Installation

### Claude Code

Copy the skill to your project:

```bash
cp -r jambonz/ .claude/skills/jambonz/
```

Or to your global skills directory for all projects:

```bash
cp -r jambonz/ ~/.claude/skills/jambonz/
```

### Cursor

```bash
cp -r jambonz/ .cursor/skills/jambonz/
```

### VS Code Copilot

```bash
cp -r jambonz/ .vscode/skills/jambonz/
```

### Other Agents

Copy the `jambonz/` folder to the skills directory for your agent. See [agentskills.io](https://agentskills.io) for a list of supported agents.

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
