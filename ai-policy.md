# AI Policy Notes

This file is not meant to be machine-read. It is a human note for deciding how to configure `robots.txt` and `llms.txt`.

## Where to start

- Use `public/robots.txt` if you want the repo's balanced default.
- Use `presets/conservative/public/robots.txt` if you want to block AI-specific bots where possible.
- Use `presets/open/public/robots.txt` if you want broad AI access.
- Use `crawler-matrix.md` when you want to understand why the preset files treat agents differently.

## Practical defaults

### `robots.txt`
Use this to allow or block known crawlers.

### `llms.txt`
Use this to point language models toward your best public pages.

## How this repo groups crawlers

These categories are a repo convention inferred from vendor docs, not a formal standard:

- Search and discovery bots help a site appear in AI search results.
- Training bots collect content that may contribute to model improvement or training.
- User-directed fetch agents visit pages because a user asked an assistant to retrieve them.

## Common policy positions

### Conservative
- Allow normal web search indexing
- Block AI search, training, and user-directed fetch agents where possible
- Keep `llms.txt` small and canonical

### Balanced
- Allow search indexing
- Allow AI discovery and user-directed fetch where helpful
- Block training-oriented crawlers you do not want
- Publish a curated `llms.txt`

### Open
- Allow search and AI crawlers broadly
- Allow training-oriented crawlers if that matches your policy
- Use `llms.txt` to emphasize authoritative content

## Good candidates for `llms.txt`

- Home
- About
- Product overview
- Pricing
- Docs
- FAQ
- API docs
- Privacy policy
- Terms

## Avoid listing

- Admin pages
- Account areas
- Checkout flows
- Staging URLs
- Preview deployments
- Temporary campaign pages unless intentionally canonical

## Reminder

`llms.txt` is an explanation layer, not an enforcement layer. If you need to allow or block access, do it in `robots.txt` first.
