# Clawifi plugin for Claude

Connects Claude to [Clawifi](https://clawifi.dev), web access for AI agents. Claude can search the web, read pages and PDFs, extract data, and map and crawl sites through Clawifi's hosted MCP server.

## Requirements

- Nothing to install. The plugin connects to the hosted MCP server at `https://api.clawifi.dev/mcp`.
- A Clawifi account for full use. Sign in from Claude, or create a free account (1,000 credits a month) at https://clawifi.dev/signup. Without an account, `search_free`, `fetch_url`, `scrape_url` and `map_site` work as a trial (12 calls a minute, 50 a day).

## What it adds

- The `clawifi` MCP server: Clawifi's hosted MCP server, reached over HTTPS.
- The `clawifi-web` skill, which tells Claude which tool fits which request.

## Tools

| Tool | What it does |
| --- | --- |
| `search_free` | Search the web across several engines as one |
| `fetch_url` | Read one page or PDF; pass a question to get only the passages that answer it |
| `scrape_url` | Read a page into chosen formats |
| `extract_url` | Extract structured fields from a page |
| `map_site` | List a site's discoverable URLs from a seed URL |
| `start_crawl` / `get_crawl` | Start an asynchronous crawl and poll its results |
| `read_artifact` | Read a stored result |
| `create_job` / `get_job` | Run a billable operation asynchronously and poll its results |
| `estimate` | Price a call before it runs |
| `account` / `credits` | Show the account, plan and remaining credits |
| `list_history` / `list_monitors` | List past requests and configured monitors |

## Setup

In Claude Code, install the plugin from this repository:

```
/plugin install clawifi --marketplace ReARCLabs/clawifi-claude-plugin
```

Then run `/mcp`, choose `clawifi` and sign in with your Clawifi account (or create a free one). The trial tools work before you sign in.

## Data and privacy

- **What it runs:** nothing on your machine. The plugin declares one remote MCP server, and Claude connects to it at `https://api.clawifi.dev/mcp` over HTTPS. It has no hooks and no local code.
- **What it sends:** when Claude calls a Clawifi tool, it sends that tool's arguments (search queries, URLs, crawl and extraction settings, job and crawl IDs) to the Clawifi MCP server. After you sign in, requests are tied to your Clawifi account. Clawifi then fetches the requested public web pages on its own infrastructure. The plugin sends no other files or data from your machine.
- **What is stored:** Clawifi keeps request history and credit usage for your account, which you can view with `list_history` and `credits`.
- Privacy policy: https://clawifi.dev/privacy
- Terms: https://clawifi.dev/terms

## Support

Docs: https://clawifi.dev/docs · Remote MCP: https://clawifi.dev/docs/remote-mcp
Email: support@clawifi.dev
Issues: https://github.com/ReARCLabs/clawifi-mcp/issues
Security: see [SECURITY.md](SECURITY.md)

## License

MIT
