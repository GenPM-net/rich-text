# @core/rich-text

[![genpm](https://api.genpm.net/v1/badge/@core/rich-text.svg)](https://genpm.net/p/@core/rich-text) ![license](https://img.shields.io/badge/license-MIT-blue)

> Rich text: Tiptap editor, allowlisted JSON documents and XSS-safe HTML/React rendering, plain text and TOC

A [GenPM](https://genpm.net) module: **source code + AI rules + MCP config**, injected into your project instead of hidden in `node_modules`. The code lands in `src/lib/rich-text`, pinned to a verified commit, and you own it.

## Install

```bash
genpm add @core/rich-text
```

No genpm yet? `curl -fsSL https://genpm.net/install.sh | sh` (macOS/Linux), `irm https://genpm.net/install.ps1 | iex` (Windows), or one-off with `npx @genpm-net/cli add @core/rich-text`.

Or let your AI agent do it: run `genpm mcp setup` once, then ask *"add @core/rich-text with genpm"* in Claude Code, Cursor, VS Code, Windsurf, Codex or Gemini CLI. It shows you a dry-run plan before writing anything.

## What it does

Rich text stored as JSON (Tiptap/ProseMirror format), never as HTML. `RichTextSchema` allowlists nodes (paragraphs,
headings, lists, quotes, code, images from @core/media, YouTube/Vimeo embeds), marks and links (site paths, `#`,
http(s), mailto, tel). Renders to HTML or React with full escaping, plain text, excerpts, reading time and a table of
contents with stable heading ids. Includes a Tiptap editor component. No tables, no collaboration.

## At a glance

- **npm dependencies** (proposed, never installed without asking): `zod`, `react`, `@tiptap/react`, `@tiptap/pm`, `@tiptap/starter-kit`, `@tiptap/extension-link`, `@tiptap/extension-image`
- **AI rules**: [`AGENTS.md`](AGENTS.md), loaded by your agent only when it works in `src/lib/rich-text`

## Security

GenPM installs a 40-character commit SHA (never a branch), verifies an Ed25519-signed manifest, never runs install scripts and scans AI rules for prompt injection. Details: [genpm.net/docs/security](https://genpm.net/docs/security).

## License

MIT — see [LICENSE](LICENSE). Browse the full catalog at [genpm.net](https://genpm.net).
