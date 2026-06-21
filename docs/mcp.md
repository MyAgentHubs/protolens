# ProtoLens MCP

ProtoLens exposes a remote MCP endpoint:

https://protolens.myagenthubs.com/mcp

The MCP server lets AI tools work with prototype review data.

## Tools

The current MCP surface is focused on prototype review:

- `listPrototypeFiles`
- `createReviewLink`
- `listReviewComments`
- `exportReviewMarkdown`

## Basic Config

For MCP clients that support remote OAuth discovery, the ideal configuration is:

```json
{
  "mcpServers": {
    "protolens": {
      "url": "https://protolens.myagenthubs.com/mcp"
    }
  }
}
```

## Dashboard Token Fallback

Some MCP clients do not yet complete remote OAuth flows. For those clients, open the ProtoLens dashboard and copy a short-lived MCP config from the MCP card.

The copied config includes an `Authorization` header. Treat that token like a temporary secret.

## Typical AI Workflow

1. Use `listPrototypeFiles` to find reviewable HTML, SVG, or PNG files.
2. Use `createReviewLink` to create or reuse a stable review URL.
3. Share the review URL with teammates.
4. Use `listReviewComments` or `exportReviewMarkdown` to bring human feedback back into the AI workflow.

This keeps AI-generated prototypes, human review, and implementation follow-up in one loop.
