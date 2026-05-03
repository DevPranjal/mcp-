# MCP Skills — fork of `modelcontextprotocol/modelcontextprotocol`

This fork adds **SEP-1: MCP Skills — Progressive Disclosure for Servers via Resources** to
the MCP draft schema.

## What was added

- `seps/1-mcp-skills-progressive-disclosure.md` — the SEP itself (rendered at
  `docs/seps/1-mcp-skills-progressive-disclosure.mdx`).
- `schema/draft/schema.ts` — new draft protocol surface:
  - `ServerCapabilities.skills?: { listChanged?: boolean }`
  - `Skill`, `SkillFrontmatter`
  - `skills/list` request / result / response (paginated, frontmatter-only)
  - `notifications/skills/list_changed`
- `schema/draft/examples/{Skill,ListSkillsRequest,ListSkillsResult,ListSkillsResultResponse,SkillListChangedNotification,ServerCapabilities/skills-*}` — JSON examples.
- Regenerated `schema/draft/schema.json` and `docs/specification/draft/schema.mdx`.

## How to use

```bash
npm install
npm run check:schema   # validate types, JSON schema, examples, MDX
npm run check:seps     # validate SEP rendering
npm run serve:docs     # preview the docs site (incl. SEP-1)
```

After editing `schema/draft/schema.ts` or `seps/`, regenerate artifacts:

```bash
npm run generate:schema   # JSON + MDX
npm run generate:seps     # SEP MDX + nav
```

## Upstream

For the full MCP specification, docs, and tooling, see the upstream project at
[modelcontextprotocol.io](https://modelcontextprotocol.io) and
[CONTRIBUTING.md](./CONTRIBUTING.md). This project is licensed under the
[MIT License](LICENSE).
