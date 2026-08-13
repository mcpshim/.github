<p align="center">
  <img src="https://mcpshim.dev/icon.svg" alt="MCPShim" width="100" height="100" />
</p>

<h1 align="center">MCPShim</h1>

<p align="center">
  <strong>Use any MCP server or HTTP API as a standard CLI command.</strong>
</p>

<p align="center">
  <a href="https://mcpshim.dev">Website</a> · <a href="https://github.com/mcpshim/mcpshim">Documentation</a> · <a href="https://github.com/mcpshim/skills">Skills</a>
</p>

---

MCPShim is a lightweight daemon + CLI that turns remote MCP tools and
configured HTTP APIs into native shell commands your agent or script can call
directly.

One daemon centralizes service registration, auth flows, discovery, call
execution, and history. Your agent invokes tools as standard CLI commands - no
SDKs, no libraries, just shell.

```bash
# Inspect a server declared in ~/.config/mcpshim/config.yaml
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

### Ecosystem

| Project                                       | Role                                                           |
| --------------------------------------------- | -------------------------------------------------------------- |
| [zot](https://github.com/openzot/openzot)     | Run complete coding tasks autonomously from a single brief     |
| [Pantalk](https://github.com/pantalk/pantalk) | Connect coding agents to the chat platforms people already use |
| [crmkit](https://github.com/crmkit/crmkit)    | Give agents a shared CRM and system of record over HTTP or MCP |

### Get Started

```bash
# Install from source
go install github.com/mcpshim/mcpshim/cmd/mcpshimd@latest
go install github.com/mcpshim/mcpshim/cmd/mcpshim@latest

# Declare a remote MCP server in the source-of-truth config
mkdir -p ~/.config/mcpshim
cat > ~/.config/mcpshim/config.yaml <<'YAML'
servers:
  - name: notion
    alias: notion
    transport: http
    url: https://mcp.notion.com/mcp
YAML

# Start daemon and inspect servers/tools
mcpshimd &
mcpshim servers
mcpshim tools
```

<p align="center">
  <sub>Built for AI agents that need MCP orchestration. → <a href="https://mcpshim.dev">mcpshim.dev</a></sub>
</p>
