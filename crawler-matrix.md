# Crawler Matrix

Last reviewed: 2026-04-17

This file is the maintenance note for the `robots.txt` presets in this repo.

The `Type` and `Suggested treatment in balanced preset` columns are this repo's interpretation of current vendor docs. They are recommendations for this starter, not a formal standard.

| Vendor | User-agent | Type | Vendor-described purpose | Suggested treatment in balanced preset | Source |
| --- | --- | --- | --- | --- | --- |
| OpenAI | `OAI-SearchBot` | Search and discovery | Used to surface websites in ChatGPT search results | Allow | [OpenAI crawler docs](https://developers.openai.com/api/docs/bots) |
| OpenAI | `ChatGPT-User` | User-directed retrieval | Used when a user asks ChatGPT or a Custom GPT to visit a page; OpenAI notes that `robots.txt` rules may not always apply because the request is user initiated | Allow as a public policy signal | [OpenAI crawler docs](https://developers.openai.com/api/docs/bots) |
| OpenAI | `GPTBot` | Training | Crawls content that may be used to improve OpenAI foundation models | Disallow | [OpenAI crawler docs](https://developers.openai.com/api/docs/bots) |
| Anthropic | `Claude-SearchBot` | Search and discovery | Navigates the web to improve search result quality for Claude users | Allow | [Anthropic crawler help](https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler) |
| Anthropic | `Claude-User` | User-directed retrieval | Supports Claude users when Claude accesses websites at a user's direction | Allow | [Anthropic crawler help](https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler) |
| Anthropic | `ClaudeBot` | Training | Collects public web content that could potentially contribute to model training | Disallow | [Anthropic crawler help](https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler) |
| Perplexity | `PerplexityBot` | Search and discovery | Indexes pages for Perplexity search; Perplexity says it is not used for foundation model pre-training | Allow | [Perplexity robots.txt help](https://www.perplexity.ai/help-center/en/articles/10354969-how-does-perplexity-follow-robots-txt) |

## Notes

- `robots.txt` is the real access-control file in this repo. `llms.txt` is advisory.
- User-directed agents sit in a gray area because vendors may treat explicit user actions differently from automated crawling. This repo still includes explicit rules for them because they communicate site intent clearly.
- Re-check vendor docs before changing these presets. Bot names and behavior can change.
