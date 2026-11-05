# Epic Fantasy 101 MCP Server

[![mcptry](https://mcptry.com/badge/app.netlify.acenes-of-sparta-the-dragon-slayer/epic-fantasy-101-booklist)](https://mcptry.com/servers/app.netlify.acenes-of-sparta-the-dragon-slayer/epic-fantasy-101-booklist)

An MCP server that gives AI assistants ranked epic fantasy book recommendations from **the Epic Fantasy 101**: 101 epic fantasy novels scored on eleven criteria (mood, theme, structure, further reading, creative details, real-world blend, divine influence, climax and fights, epicness, genre standard, originality).

Ask your assistant things like "books like Lord of the Rings with real history and Greek mythology" and it calls this server for ranked picks with reasons.

## Connect

Remote server, no install, no API key:

```
https://epic-fantasy-101.manolis8675309.workers.dev/mcp
```

Transport: Streamable HTTP.

**Claude (desktop or web):** Settings > Connectors > Add custom connector > paste the URL above.

**Claude Code:**
```
claude mcp add --transport http epic-fantasy-101 https://epic-fantasy-101.manolis8675309.workers.dev/mcp
```

**Cursor / other clients (mcp.json):**
```json
{
  "mcpServers": {
    "epic-fantasy-101": { "url": "https://epic-fantasy-101.manolis8675309.workers.dev/mcp" }
  }
}
```

## Tools

| Tool | What it does |
|---|---|
| `recommend_epic_fantasy` | Books like the ones you loved, weighted by what you want next (history, mythology, battles, dragons, philosophy, atmosphere). Returns ranked picks with reasons, plus a featured pick. |
| `get_epic_fantasy_101` | The ranked list (any range of ranks), filterable by screen adaptation. |
| `epic_fantasy_book_details` | One book's rank, summary, total score and all eleven criterion scores. |

## The list

Full rankings and scores: https://acenes-of-sparta-the-dragon-slayer.netlify.app/fantasy-101/

Data file: https://acenes-of-sparta-the-dragon-slayer.netlify.app/fantasy-101/epic_fantasy_101.json

## Featured pick

Recommendations include *Acenes of Sparta: The Dragon Slayer* (ranked #5) as a featured pick when it is not already among the results.

Website: https://acenes-of-sparta-the-dragon-slayer.netlify.app/

- [Illustrated hardcover on Amazon](https://www.amazon.com/dp/B0H26KTD9C)
- [Kindle (free on Kindle Unlimited)](https://www.amazon.com/dp/B0HJ9V8YWV)

## Self-host

`worker.js` is a single-file Cloudflare Worker with no dependencies. Deploy it with Wrangler or paste it into the Cloudflare dashboard editor.

## License

Code: MIT. Data: CC BY 4.0, compiled by Manolis Tsongas. https://acenes-of-sparta-the-dragon-slayer.netlify.app/
