# Greenspark MCP

Install kit and Agent Skills for the Greenspark API on [Model Context Protocol](https://modelcontextprotocol.io/).

The MCP **server** is hosted by [ReadMe](https://readme.com) at **`https://docs.getgreenspark.com/mcp`**. This repo ships client examples, [server.json](server.json) registry metadata, and skills — not server source code.

## Quick start

**1. Connect MCP** — merge into your client config (see [examples/](examples/)):

```json
{
  "mcpServers": {
    "greenspark": {
      "url": "https://docs.getgreenspark.com/mcp",
      "headers": { "x-api-key": "YOUR_SANDBOX_API_KEY" }
    }
  }
}
```

Use a **sandbox** key for testing. Setup guide: [docs.getgreenspark.com](https://docs.getgreenspark.com).

**2. Install skills** (optional):

```bash
npx skills add getgreenspark/mcp -a cursor -g -y
```

More agents and single-skill installs: [skills/](skills/) · [skills.sh](https://skills.sh/)

## MCP v1

- **Read-only** — `execute-request` on enabled **GET** routes only
- **Live via MCP:** Impact, Reporting, Account, Projects
- **Auth:** `x-api-key`; match key to host (sandbox vs production)

Details: **greenspark-mcp** and **greenspark-auth-environments** in [skills/](skills/).

## Skills

`greenspark-mcp` · `greenspark-auth-environments` · `greenspark-integration-workflow` · `greenspark-impact` · `greenspark-reporting` · `greenspark-account` · `greenspark-projects`

## Links

| Resource | Link |
|----------|------|
| API docs | [docs.getgreenspark.com](https://docs.getgreenspark.com) |
| Staying up to date | [docs/MAINTENANCE.md](docs/MAINTENANCE.md) |
| Registry publishing | [docs/PUBLISHING.md](docs/PUBLISHING.md) (maintainers) |
| Changelog | [CHANGELOG.md](CHANGELOG.md) |

MIT — [LICENSE](LICENSE)
