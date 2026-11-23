# Installing the Embeddable MCP server

Embeddable is a hosted remote server. There is nothing to download, build or run.

1. Add this server to the MCP settings (streamable HTTP):

```json
{
  "mcpServers": {
    "embeddable": {
      "type": "streamableHttp",
      "url": "https://mcp.embeddable.co/mcp"
    }
  }
}
```

2. On the first tool call the client opens the Embeddable sign-in page (OAuth). The user signs in or creates a free account at https://embeddable.co and picks a workspace. No API key is needed.

3. Check the connection by calling `whoami`. It returns the connected user and workspace.
