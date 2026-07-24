<p align="center">
  <img src="https://mcpshim.dev/icon.svg" alt="MCPShim" width="100" height="100" />
</p>

<h1 align="center">MCPShim</h1>

<p align="center">
  <strong>Use any MCP server as a standard CLI command.</strong>
</p>

<p align="center">
  <a href="https://mcpshim.dev">Website</a> · <a href="https://github.com/mcpshim/mcpshim">Documentation</a> · <a href="https://github.com/mcpshim/skills">Skills</a>
</p>

---

MCPShim is a lightweight daemon + CLI that turns remote MCP tools into native shell commands your agent or script can call directly.

One daemon centralizes server registration, auth flows, discovery, call
execution, and history. Your agent invokes tools as standard CLI commands - no
SDKs, no libraries, just shell.

```bash
# Register a remote MCP server
mcpshim add --name notion --alias notion --transport http --url https://example.com/mcp

# Inspect available tools
mcpshim tools --server notion

# Call a tool
mcpshim call --server notion --tool search --query "roadmap"

# View recent calls
mcpshim history --server notion --limit 20
```

### Repositories

| Repo                                          | Description                                  |
| --------------------------------------------- | -------------------------------------------- |
| [mcpshim](https://github.com/mcpshim/mcpshim) | Daemon, CLI, and documentation               |
| [skills](https://github.com/mcpshim/skills)   | Agent skill definitions for AI coding agents |

### Companion Projects

| Repo                                          | Description                                       |
| --------------------------------------------- | ------------------------------------------------- |
| [pantalk](https://github.com/pantalk/pantalk) | Give your AI agent a voice on every chat platform |
| [crmkit](https://github.com/crmkit/crmkit)    | An agent-first CRM your AI drives directly        |

MCPShim gives your agent tools. [Pantalk](https://pantalk.dev) gives it a voice across Slack, Discord, Telegram, and more.

### Get Started

```bash
# Install from source
go install github.com/mcpshim/mcpshim/cmd/mcpshimd@latest
go install github.com/mcpshim/mcpshim/cmd/mcpshim@latest

# Start daemon and inspect servers/tools
mcpshimd
mcpshim servers
mcpshim tools
```

<p align="center">
  <sub>Built for AI agents that need MCP orchestration. → <a href="https://mcpshim.dev">mcpshim.dev</a></sub>
</p>
