# Embeddable MCP server

Build website widgets and landing pages from any MCP client. [Embeddable](https://embeddable.co) has an AI builder that makes booking and contact forms, quizzes, price calculators, pricing tables, popups, review walls and more, hosts them, and gives you an embed code for any site.

This repository holds the public listing for the hosted server. There is nothing to install or run.

- **Endpoint:** `https://mcp.embeddable.co/mcp` (remote, streamable HTTP)
- **Auth:** OAuth 2.1 (dynamic client registration and client ID metadata documents are supported). Sign in with your Embeddable account and pick a workspace.
- **Registry name:** `co.embeddable/embeddable`
- **Docs:** https://embeddable.co/mcp

## Connect

**Claude Code**

```bash
claude mcp add --transport http embeddable https://mcp.embeddable.co/mcp
```

**Any client that takes a JSON config (Cursor, Windsurf, VS Code, Cline and others)**

```json
{
  "mcpServers": {
    "embeddable": { "url": "https://mcp.embeddable.co/mcp" }
  }
}
```

The first call opens the Embeddable sign-in page in your browser.

## Tools

| Tool | What it does |
|---|---|
| `whoami` | Shows which Embeddable user and workspace the connection acts as |
| `list_widgets` | Lists the workspace's widgets, with publish status |
| `get_widget` | Gets one widget's details |
| `create_widget` | Creates a new widget or landing page from a description with the AI builder |
| `edit_widget` | Changes a widget in plain words with the AI builder; the result is a draft |
| `get_job` | Gets the status of a running build |
| `get_draft_preview` | Takes a screenshot of the current draft |
| `get_preview` | Gets the preview and editor links, and the published version's screenshot |
| `publish_widget` | Publishes the current draft |
| `get_embed_code` | Gives the embed snippet and the steps for WordPress, Wix, Squarespace, Shopify, Webflow or plain HTML |
| `list_widget_files` | Lists the widget's source files |
| `read_widget_file` | Reads one source file |
| `list_widget_versions` | Lists saved versions |
| `restore_widget_version` | Puts an earlier version back as the draft (never publishes) |
| `get_usage` | Shows the plan and the AI builder messages left this month |

Each `create_widget` or `edit_widget` call uses 1 message from your Embeddable plan, the same as typing in the editor. Edits stay drafts until you publish, and the connection cannot delete anything.

## Support

contact@embeddable.co · [Privacy policy](https://embeddable.co/legal/privacy-policy) · [Terms](https://embeddable.co/legal/terms)

Made by [Common Ninja](https://www.commoninja.com).
