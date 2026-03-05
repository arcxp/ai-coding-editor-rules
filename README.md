# Arc XP PageBuilder AI Coding Editor Rules

Project instruction files for AI code editors working with Arc XP PageBuilder Engine bundles. Drop these into your Feature Pack repo so your AI assistant understands Arc XP conventions, APIs, and common patterns.

## Quick Start

Download `AGENTS.md` directly into your Feature Pack repo root:

```bash
cd /path/to/your-feature-pack
curl -O https://raw.githubusercontent.com/arcxp/ai-coding-editor-rules/main/AGENTS.md
```

Then customize the **Project Context** section at the top with your org's details.

Most AI editors (Cursor, Windsurf, GitHub Copilot, etc.) will pick up `AGENTS.md` automatically.

### Claude Code Setup

Claude Code reads `CLAUDE.md` by default. You have two options:

**Option A — Download directly as CLAUDE.md:**
```bash
curl -o CLAUDE.md https://raw.githubusercontent.com/arcxp/ai-coding-editor-rules/main/AGENTS.md
```

**Option B — Keep AGENTS.md and create a small CLAUDE.md pointer:**

```bash
echo "Read AGENTS.md in this repo for full Arc XP PageBuilder Engine coding instructions." > CLAUDE.md
```

Claude Code will read `CLAUDE.md` first, then follow the instruction to read `AGENTS.md`. This is useful if you want editor-specific instructions in `CLAUDE.md` while sharing `AGENTS.md` across all editors.

### Cursor Setup

Cursor reads `.cursorrules` files. You can either:
- Download as `.cursorrules`: `curl -o .cursorrules https://raw.githubusercontent.com/arcxp/ai-coding-editor-rules/main/AGENTS.md`
- Or use Cursor's newer project settings which also reads `AGENTS.md`

## What's Inside

`AGENTS.md` includes:

- **Project context template** — tech stack, CLI commands, local dev setup
- **Bundle directory structure** — annotated feature pack layout
- **Platform knowledge map** — Content API, View API, Subscriptions, Themes & Arc Blocks
- **Full PageBuilder Engine doc reference** — every API, concept, how-to, and troubleshooting article with URLs (token-efficient relative-path format)
- **Themes & Arc Blocks docs** — design system, block customization, ejecting, identity/subscription blocks
- **Common patterns** — doc references for content sources, features, custom fields, environment vars, site properties, output types
- **Anti-patterns & gotchas** — common mistakes AI agents make with Arc XP code

---

## V1 (Legacy — Cursor only)

The `cursorrules-V1` file is the original Cursor-specific rules file from the first version of this repo. It is kept for reference but is no longer maintained.

If you were using V1, we recommend migrating to `AGENTS.md` which is more comprehensive, works across all AI editors, and covers the full Arc XP documentation set.

---

## Contributing

PRs welcome! If you spot outdated URLs, missing docs, or have patterns that would help AI editors write better Arc XP code, open a pull request.

Share what's working for you, tips, or questions in [Arc XP GitHub Discussions](https://github.com/orgs/arcxp/discussions).

## License

[MIT](LICENSE)
