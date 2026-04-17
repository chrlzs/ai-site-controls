# AI Policy Notes

This file is not meant to be machine-read. It is a human note for deciding how to configure `robots.txt` and `llms.txt`.

## Practical defaults

### `robots.txt`
Use this to allow or block known crawlers.

### `llms.txt`
Use this to point language models toward your best public pages.

## Common policy positions

### Conservative
- Allow normal web search indexing
- Block model-oriented AI crawlers where possible
- Keep `llms.txt` small and canonical

### Balanced
- Allow search indexing
- Allow some AI discovery/search crawlers
- Block training-oriented crawlers you do not want
- Publish a curated `llms.txt`

### Open
- Allow search and AI crawlers broadly
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
