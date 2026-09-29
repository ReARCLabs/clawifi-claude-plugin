# Clawifi plugin for Claude

Connects Claude to [Clawifi](https://clawifi.qzz.io), an agent-native internet gateway. Claude can search the web and fetch, scrape, extract, map and crawl pages through the hosted Clawifi API.

## Requirements

- A Clawifi account and API key (`clawifi_live_...`), created at https://clawifi.qzz.io/signup. New accounts get 1,000 free credits.
- [uv](https://docs.astral.sh/uv/) installed (the plugin starts the MCP server with `uvx`)
- Python 3.11 or later

## What it adds

- The `clawifi` MCP server, which runs `clawifi-mcp` from the `clawifi` PyPI package and calls the Clawifi API with your key
- The `clawifi-web` skill, which tells Claude which tool fits which request

## Tools

| Tool | What it does |
| --- | --- |
| `fetch` | Fetch a single URL and return its extracted content |
| `scrape` | Scrape a URL with source-aware routing and return structured content |
| `search_free` | Run a free-tier web search |
| `extract` | Extract structured data from a URL |
| `map_site` | Map a site's discoverable URLs from a seed URL |
| `crawl` / `get_crawl` | Start an asynchronous crawl and poll its results |
| `create_job` / `get_job` | Run a billable operation asynchronously and poll its results |
| `account` / `credits` | Show the account, plan and remaining credits |
| `list_history` / `list_monitors` | List past requests and configured monitors |

## Setup

Install the plugin, then enter your Clawifi API key when Claude prompts for it. The key is stored in your system's secure credential store.

## Support

Docs: https://clawifi.qzz.io/docs
Issues: https://github.com/atakanelik34/clawifi-mcp/issues

## License

MIT
