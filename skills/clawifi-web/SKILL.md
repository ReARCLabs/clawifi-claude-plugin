---
name: clawifi-web
description: Use Clawifi to search the web and fetch, scrape, crawl or extract content from web pages. Use when the user asks for live web information, the content of a specific URL, structured data from a page, or a map or crawl of a site.
---

# Clawifi web access

Clawifi runs web requests on the hosted Clawifi API through the `clawifi` MCP server. Most operations use credits from the user's Clawifi account.

## Pick the right tool

- `search_free`: find pages for a query.
- `fetch`: get the extracted content of one URL.
- `scrape`: get structured content from a URL when `fetch` isn't enough.
- `extract`: pull structured data from a URL.
- `map_site`: list a site's discoverable URLs from a seed URL.
- `crawl`, then `get_crawl`: crawl a site asynchronously and poll for results.
- `create_job`, then `get_job`: run a billable operation asynchronously and poll for results.
- `account`, `credits`: check the account, plan and remaining credits.
- `list_history`, `list_monitors`: review past requests and configured monitors.

## Guidance

- Start with the smallest operation that answers the question: `fetch` one page before crawling a whole site.
- Check `credits` before large crawls, and tell the user roughly how much a large job will use.
- Cite the URLs you used when you report what you found.
- Respect the user's request scope and site terms; don't crawl more pages than the task needs.
