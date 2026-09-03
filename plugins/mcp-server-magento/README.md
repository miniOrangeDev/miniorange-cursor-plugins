# miniOrange Magento MCP

Cursor plugin that connects the IDE to [miniOrange Magento MCP](https://plugins.miniorange.com/magento-mcp-server).

This repo is the Cursor-side wrapper only. It does not include Magento or server source. After install, Cursor connects to the hosted MCP at `https://magento.miniorange.com/mcp` over OAuth.

## What you can do

Ask Cursor about live Magento 2 / Adobe Commerce store data, for example:

- Product catalog and inventory
- Orders, invoices, and shipments
- Customers and store operations

What the agent can do is scoped by the Magento permissions granted during OAuth.

## Requirements

- Cursor with plugin support
- Access to miniOrange Magento MCP (hosted sandbox or a store with the [Magento MCP Server](https://plugins.miniorange.com/magento-mcp-server) extension)

## What's inside

| Path | Role |
|---|---|
| `.cursor-plugin/plugin.json` | Cursor Plugin manifest |
| `mcp.json` | Remote MCP: `https://magento.miniorange.com/mcp` |
| `assets/logo.svg` | Marketplace logo |

## Install

**Marketplace (after listing):** Customize → Plugins → install **miniOrange Magento MCP**. Complete OAuth when Cursor prompts.

**Local test (before submit):**

1. Copy this folder to `~/.cursor/plugins/local/miniorange-magento`  
   On Windows: `%USERPROFILE%\.cursor\plugins\local\miniorange-magento`
2. Confirm `.cursor-plugin/plugin.json` is at that folder root
3. Reload Cursor (**Developer: Reload Window**)
4. Open Customize and confirm the MCP server is listed
5. Sign in when Cursor starts OAuth

## How it works

```text
Cursor → mcp.json → https://magento.miniorange.com/mcp → Magento MCP tools
```

OAuth is handled by Cursor against the hosted server. Desktop uses `http://localhost:8787/callback`. Cursor Agents use `https://www.cursor.com/agents/mcp/oauth/callback`.

## Marketplace

This is a **Cursor Plugin** (manifest at `.cursor-plugin/plugin.json`), not an Agent Plugin. For Cursor Marketplace the GitHub repository must be **public** and open source (MIT). Submit the repo URL at [cursor.com/marketplace/publish](https://cursor.com/marketplace/publish).

## License

MIT. Hosted Magento MCP remains a miniOrange product.

## Links

- Product: https://plugins.miniorange.com/magento-mcp-server
- Cursor plugins: https://cursor.com/docs/plugins
- Cursor plugin format: https://cursor.com/docs/reference/plugins
