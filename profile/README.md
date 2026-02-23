<p align="center">
  <img src="https://mcpshim.dev/icon.svg" alt="mcpshim" width="100" height="100" />
</p>

<h1 align="center">mcpshim</h1>

<p align="center">
  <strong>Turn remote MCP servers into local command workflows.</strong>
</p>

<p align="center">
  <a href="https://mcpshim.dev">Website</a> · <a href="https://github.com/mcpshim/mcpshim">Documentation</a> · <a href="https://github.com/mcpshim/skills">Skills</a>
</p>

---

`mcpshim` is a daemon + CLI bridge that centralizes remote MCP server lifecycle in one local process and exposes a consistent Unix socket protocol for scripts and AI agents.

One daemon handles MCP sessions, auth flows, discovery, and reconnects. Your agent can invoke tools through simple CLI commands or over a Unix domain socket with a JSON protocol.

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

| Repo                                          | Description                    |
| --------------------------------------------- | ------------------------------ |
| [mcpshim](https://github.com/mcpshim/mcpshim) | Daemon, CLI, and documentation |

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=mcpshim/mcpshim&type=date&legend=top-left)](https://www.star-history.com/#mcpshim/mcpshim&type=date&legend=top-left)

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
