# Swagger plugin for Cursor

Connect Cursor to **Swagger by SmartBear** with OAuth sign-in and ready-made API workflows. No API tokens, no local installation: authentication happens in your browser on first use.

## What's included

### MCP server (hosted, OAuth)

`https://swagger.mcp.smartbear.com/mcp` gives the agent access to:

- **Swagger registry** — search, fetch, create, and update API definitions across your organizations
- **API governance** — scan definitions against your organization's standardization rules
- **AI-assisted design** — generate an API definition from a natural-language description and auto-fix governance violations
- **API portals** — create and publish portal products and documentation pages

### Rules

A context rule that teaches the agent when to reach for Swagger tools during everyday API design, documentation, and testing tasks.

## Installation

1. Install the plugin from the Cursor Marketplace (or add this repository via **Settings → Plugins**).
2. Open any project. On the first Swagger tool call, a browser window opens for SmartBear OAuth login — sign in and approve.
3. Done. Try it: ask *"search Swagger for our payments API"*.

You need a [SmartBear account](https://smartbear.com/) with access to Swagger Studio.

## Advanced: other SmartBear products

SmartBear also hosts MCP servers for **BugSnag** (`https://bugsnag.mcp.smartbear.com/mcp`) and **Zephyr** (`https://zephyr.mcp.smartbear.com/mcp`) — add them to your Cursor MCP settings the same way. The full product suite — including **PactFlow** (contract testing and provider drift), **Reflect**, **QMetry**, and **Collaborator** — is available in the local MCP server with API keys:

```json
{
  "mcpServers": {
    "smartbear": {
      "command": "npx",
      "args": ["-y", "@smartbear/mcp@latest"],
      "env": {
        "SWAGGER_API_KEY": "…"
      }
    }
  }
}
```

See the [full configuration reference](https://developer.smartbear.com/smartbear-mcp/docs/local-server) for all supported products and variables.

## Links

- [SmartBear MCP documentation](https://developer.smartbear.com/smartbear-mcp)
- [Swagger remote server setup guide](https://developer.smartbear.com/smartbear-mcp/docs/remote-swagger)
- [Source repository](https://github.com/SmartBear/smartbear-mcp)

## License

MIT © SmartBear Software
