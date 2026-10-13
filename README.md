# Proofsource for Claude

Proofsource measures how AI assistants talk about your brand. It asks ChatGPT, Perplexity, Claude and Google AI Overviews the questions your buyers ask, and shows how often you are mentioned, which competitors are recommended instead, and which sources the answers cite.

This plugin connects Claude to your Proofsource workspace and adds two skills:

- **ai-visibility-audit**: a sourced summary of your AI visibility, competitors, cited sources and recent changes.
- **fix-plan**: a prioritized plan from your open gaps, plus tracking new buyer questions and shipped fixes (always asks first).

## Install

```
/plugin marketplace add lcbasu/proofsource-plugins
/plugin install proofsource@proofsource-plugins
```

Then run `/mcp`, pick `proofsource` and sign in with your Proofsource account. Try: "Is my brand mentioned in ChatGPT answers?"

## Connect without the plugin

The connector URL is `https://app.proofsource.co/v1/mcp` (OAuth 2.1; you sign in with your Proofsource email and a one-time code).

- **Claude (web or Desktop):** Settings → Connectors → Add custom connector → paste the URL → Connect.
- **ChatGPT:** Settings → Apps & Connectors → Advanced → turn on Developer mode → Create → paste the URL, choose OAuth.
- **Claude Code:** `claude mcp add --scope user --transport http proofsource https://app.proofsource.co/v1/mcp`, then `/mcp` to sign in.

- **Cursor, VS Code, Cline, Windsurf and other MCP clients:** add a remote (Streamable HTTP) server with the URL above; see [llms-install.md](llms-install.md).

Also listed in the official MCP Registry as `co.proofsource/proofsource` ([server.json](server.json)).

Full guide: https://proofsource.co/docs/chatgpt-and-claude

## Tools

Read: `list_brands`, `list_topics`, `get_visibility`, `get_competitors`, `get_citations`, `get_changes`, `list_fix_opportunities`, `get_fix_verification`, `get_scan_status`, `get_report_link`, `see_example` (works without signing in).
Write (your workspace only, by your plan and role): `add_brand`, `create_prompt`, `mark_fix_shipped`.

New accounts with a work email get two free scans. Personal email addresses get an account without scans.

Support: https://proofsource.co/contact · Privacy: https://proofsource.co/privacy · Terms: https://proofsource.co/terms
