# Maintenance

For developers using [Greenspark MCP](https://docs.getgreenspark.com/mcp) with the examples and skills in this repo.

## Source of truth

1. **[Greenspark API docs](https://docs.getgreenspark.com)** and MCP tools (`get-endpoint`, `list-specs`) — live API behavior and schemas
2. **This repo** — client config examples and Agent Skills; updated on release, may lag the API slightly

If a skill conflicts with live docs or MCP output, **trust the docs** and [open an issue](https://github.com/getgreenspark/greenspark-mcp/issues).

## Staying up to date

- Follow [CHANGELOG.md](../CHANGELOG.md) or [GitHub releases](https://github.com/getgreenspark/greenspark-mcp/releases)
- Refresh installed skills: `npx skills update` (or reinstall from this repo)

Setup and the MCP v1 contract are in [README.md](../README.md).

## Support

| Topic | Contact |
|-------|---------|
| Skills, examples, or MCP URL in this repo | [GitHub issues](https://github.com/getgreenspark/greenspark-mcp/issues) |
| API behavior, keys, billing, account access | [Greenspark documentation](https://docs.getgreenspark.com) |

Registry publishing (maintainers): [PUBLISHING.md](./PUBLISHING.md).
