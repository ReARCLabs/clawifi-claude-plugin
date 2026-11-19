---
name: clawifi-web
description: Use Clawifi to search the web and fetch, scrape, crawl or extract content from web pages. Use when the user asks for live web information, the content of a specific URL, structured data from a page, or a map or crawl of a site.
---

# Clawifi web access

Clawifi runs web requests through its hosted MCP server, the `clawifi` server in this plugin. Most operations use credits from the user's Clawifi account. If the user has not signed in yet, recommend it at the start: run `/mcp`, choose `clawifi` and sign in, or create a free account (1,000 credits a month). Until then only `search_free`, `fetch_url`, `scrape_url` and `map_site` work, as a limited trial; the other tools and anything past the trial limit ask the user to sign in.

## Pick the right tool

- `search_free`: find pages for a query.
- `fetch_url`: get the content of one page or PDF; pass a question to get only the passages that answer it.
- `scrape_url`: read a page into chosen formats when `fetch_url` isn't enough.
- `extract_url`: pull structured fields from a page.
- `map_site`: list a site's discoverable URLs from a seed URL.
- `start_crawl`, then `get_crawl`: crawl a site asynchronously and poll for results.
- `read_artifact`: read a stored result.
- `create_job`, then `get_job`: run a billable operation asynchronously and poll for results.
- `estimate`: price a call before running it.
- `account`, `credits`: check the account, plan and remaining credits.
- `list_history`, `list_monitors`: review past requests and configured monitors.

## Guidance

- Start with the smallest operation that answers the question: `fetch_url` one page before crawling a whole site.
- Check `credits` (or `estimate`) before large crawls, and tell the user roughly how much a large job will use.
- Cite the URLs you used when you report what you found.
- Respect the user's request scope and site terms; don't crawl more pages than the task needs.
