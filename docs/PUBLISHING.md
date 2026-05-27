# Publishing

For **Greenspark maintainers** registering the MCP listing. Integrators: use [README.md](../README.md).

## What you publish

| Item | Where |
|------|--------|
| MCP server | `https://docs.getgreenspark.com/mcp` (hosted by ReadMe) |
| Registry entry | [server.json](../server.json) — name `com.getgreenspark/greenspark-api` |
| GitHub repo | Examples and Agent Skills (directory discovery link) |

This repo is **not** MCP server source code.

## Official MCP Registry

1. `brew install mcp-publisher`
2. Authenticate with **DNS** on `getgreenspark.com` for the `com.getgreenspark/*` namespace — follow the [MCP registry publishing guide](https://modelcontextprotocol.info/tools/registry/publishing/)
3. From this repo root: `mcp-publisher publish`
4. Verify: `curl "https://registry.modelcontextprotocol.io/v0/servers?search=com.getgreenspark"`

When [server.json](../server.json) changes, bump its `version`, tag a release, and publish again. Do not commit DNS private keys (`key.pem` is gitignored).

If validation fails on transport, confirm ReadMe uses `streamable-http` or `sse` for the MCP URL and update `server.json` accordingly.

## Other directories

Forms differ; usually submit:

- MCP URL: `https://docs.getgreenspark.com/mcp`
- Repository: `https://github.com/getgreenspark/mcp`
- Documentation: `https://docs.getgreenspark.com`
- Type: Remote / hosted

## After publishing

Record the result in [CHANGELOG.md](../CHANGELOG.md). Optionally link this repo from the ReadMe MCP or Agent Skills guide.
