# Installing Proofsource (for AI agents)

Proofsource is a remote MCP server. Nothing to clone, build or run locally.

- URL: `https://mcp.proofsource.co/mcp`
- Transport: Streamable HTTP
- Auth: OAuth 2.1 (discovery at `https://mcp.proofsource.co/.well-known/oauth-protected-resource/mcp`). The user signs in with their Proofsource email and a one-time code. No API key is needed.

## Config

Add this to the client's MCP settings (Cline: `cline_mcp_settings.json`; Cursor: `~/.cursor/mcp.json`; VS Code: `.vscode/mcp.json` under `servers`):

```json
{
  "mcpServers": {
    "proofsource": {
      "type": "streamableHttp",
      "url": "https://mcp.proofsource.co/mcp"
    }
  }
}
```

Then connect and let the user complete the browser sign-in.

## Check it works

Call `see_example` (works before sign-in), then `list_brands` after sign-in. A user without an account can create one at https://proofsource.co during sign-in.
