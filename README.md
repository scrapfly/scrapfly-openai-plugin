# Scrapfly plugin for OpenAI Codex

[Codex plugin](https://developers.openai.com/plugins/build/plugins) with the skills of the [Scrapfly](https://scrapfly.io) web data APIs: scraping with JavaScript rendering and proxy pools, screenshots, AI data extraction, crawling, Cloud Browser automation and alerting, through the `scrapfly` CLI and the Python, TypeScript, Go and Rust SDKs.

## Skills

- [`scrapfly-agent-rules`](skills/scrapfly-agent-rules/SKILL.md): Cross-tool golden rules for an autonomous Scrapfly web agent connected to the Scrapfly MCP server (web_scrape, screenshot, the Cloud Browser lifecycle, snapshot/click/fill/type/press/scroll/select/drag, and WebMCP).
- [`scrapfly-alerting`](skills/scrapfly-alerting/SKILL.md): Threshold-based alerting on Scrapfly account metrics.
- [`scrapfly-browser`](skills/scrapfly-browser/SKILL.md): Automate cloud browsers using the Scrapfly Cloud Browser API with Python Playwright.
- [`scrapfly-cli`](skills/scrapfly-cli/SKILL.md): Use the Scrapfly CLI (`scrapfly`) to scrape web pages, capture screenshots, extract structured data with AI, crawl entire sites, and drive a cloud browser over CDP from a shell.
- [`scrapfly-crawler`](skills/scrapfly-crawler/SKILL.md): Crawl entire websites using the Scrapfly Crawler API with the Python SDK
- [`scrapfly-extraction`](skills/scrapfly-extraction/SKILL.md): Extract structured data from web content using the Scrapfly Extraction API with the Python SDK
- [`scrapfly-scraper`](skills/scrapfly-scraper/SKILL.md): Web scraping using the Scrapfly Scraper API with the Python SDK
- [`scrapfly-screenshot`](skills/scrapfly-screenshot/SKILL.md): Capture web page screenshots using the Scrapfly Screenshot API with the Python SDK
- [`scrapfly-sdk-go`](skills/scrapfly-sdk-go/SKILL.md): Web scraping from Go with the Scrapfly SDK (`github.com/scrapfly/go-scrapfly`).
- [`scrapfly-sdk-rust`](skills/scrapfly-sdk-rust/SKILL.md): Web scraping from Rust with the Scrapfly SDK (`scrapfly-sdk` crate).
- [`scrapfly-sdk-typescript`](skills/scrapfly-sdk-typescript/SKILL.md): Web scraping from TypeScript or JavaScript with the Scrapfly SDK (`scrapfly-sdk`).

## Requirements

- A Scrapfly API key, from the [Scrapfly dashboard](https://scrapfly.io/dashboard), in `SCRAPFLY_API_KEY`.
- For the skills that shell out to it, the [Scrapfly CLI](https://github.com/scrapfly/scrapfly-cli) (`scrapfly`).
- For the SDK skills, the SDK of the language: [Python](https://scrapfly.io/docs/sdk/python), [TypeScript](https://scrapfly.io/docs/sdk/typescript), [Go](https://scrapfly.io/docs/sdk/golang), [Rust](https://scrapfly.io/docs/sdk/rust).

## Install in Codex

Until the plugin is listed in the Codex plugin directory, install it from a local marketplace:

1. Clone this repository, for example into `plugins/scrapfly-openai-plugin` at the root of the repository you use Codex in.
2. Add `.agents/plugins/marketplace.json` at that root, shaped like [`examples/marketplace.json`](examples/marketplace.json): `source.path` is the plugin folder, relative to the marketplace file and starting with `./`.
3. Restart Codex, open **Plugins** (or `/plugins` in the Codex CLI), pick the marketplace and install **Scrapfly**.

With the Codex CLI, `codex plugin marketplace add ./path-to-marketplace-root` registers the same marketplace.

## Try it

In a new Codex thread:

1. "Use Scrapfly to scrape https://web-scraping.dev/products and list each product's name and price."
2. "Use Scrapfly to take a full-page screenshot of https://web-scraping.dev."
3. "Use Scrapfly to crawl https://web-scraping.dev, 20 pages at most, and summarize the sections of the site."

## License

MIT, see [LICENSE](LICENSE).
