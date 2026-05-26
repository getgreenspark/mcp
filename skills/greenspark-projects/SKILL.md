---
name: greenspark-projects
description: >-
  Guides Greenspark impact project catalog browsing: categories, project lists,
  and project detail with plan requirements. Use when the user mentions Greenspark
  projects, getProjects, getProject, project categories, or impact project catalog.
---

# Greenspark Projects API

## Related skills

Apply **greenspark-mcp** and **greenspark-auth-environments** before live calls.

## Operations

| operationId | Purpose | MCP notes |
|-------------|---------|-----------|
| `getProjectCategories` | List impact project categories | GET; MCP when toggled |
| `getProjects` | List impact projects for account | GET; MCP when toggled |
| `getProject` | Project detail | GET; **premium plan** may be required |
| `getProjectPage` | Project page content | GET; supplementary |
| `getProjectMetadata` | Project metadata | GET; supplementary |
| `getProjectStories` | Project stories | GET; supplementary |

## Plan requirement

`getProject` (single project detail) may return **403** unless the account has:

- `premiumBusiness`
- `premiumBusinessYearly`
- `enterpriseBusiness`

`getProjectCategories` and `getProjects` do not carry the same premium gate as `getProject` in the public API docs.

If `getProject` fails with 403, explain plan upgrade — do not retry with a different key on the same account.

## MCP rules (v1)

- Projects spec is **MCP-enabled** for GET routes when toggled in ReadMe.
- Read-only via MCP in v1.
- Typical flow: `getProjectCategories` → `getProjects` → optional `getProject` for detail.

## Agent guidance

- For "browse available projects": start with categories and list endpoints.
- For "project detail": use `getProject`; warn about premium requirement if 403.
- Use sandbox key for catalog exploration.
