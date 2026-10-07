# Enterpret

Cursor plugin that connects agents to [Enterpret](https://www.enterpret.com) through Enterpret’s official remote [Model Context Protocol](https://modelcontextprotocol.io/) server.

Query customer feedback, Spaces, themes, sentiment, and verbatim quotes in the signed-in Enterpret organization.

## Install

1. Open **Cursor Settings → Plugins**.
2. Search for **Enterpret** (or add this repo via `/add-plugin` when listing is available).
3. Click **Install**, then complete the Enterpret sign-in prompt.

Or run `/add-plugin enterpret` in chat (once published to the Cursor Marketplace).

For local development before Marketplace listing, clone this repo and add the plugin from disk, or point Cursor MCP at the server URL below.

## MCP

```json
{
  "mcpServers": {
    "enterpret": {
      "type": "http",
      "url": "https://wisdom-api.enterpret.com/server/mcp"
    }
  }
}
```

Auth is OAuth against Enterpret. Cursor prompts for Enterpret sign-in when the plugin connects — there is no API key or client ID to configure in this plugin.

Enterpret also supports Bearer tokens from **Settings → Enterpret MCP** for clients that need static credentials; this plugin uses the recommended OAuth flow.

## Notes

- Tool calls run as the Enterpret user who authorizes the connection and cannot exceed that user’s permissions.
- Capabilities include querying feedback, discovering schema/taxonomy, and pulling cited answers and verbatim quotes. See Enterpret’s MCP help article for the current tool list.

## Docs

- Enterpret MCP help center: https://helpcenter.enterpret.com/en/articles/12665166-enterpret-mcp-server
- Enterpret MCP product page: https://www.enterpret.com/platform/enterpret-mcp-server
- Server URL: https://wisdom-api.enterpret.com/server/mcp
- Homepage: https://www.enterpret.com

Logo is a simple Enterpret-like mark on a white tile, using brand indigo `#5B4BFF`.

## License

MIT
