# AI Site Controls Starter

A reusable starter repo for adding `robots.txt` and `llms.txt` to websites of many kinds.

This repo is intentionally generic so it can be copied into personal sites, marketing sites, documentation portals, product sites, or client projects.

## What this includes

- `public/robots.txt` — generic baseline crawler rules
- `public/llms.txt` — generic baseline LLM guidance file
- `templates/marketing/` — a marketing-site flavored example
- `templates/docs/` — a documentation-site flavored example
- `checklist.md` — quick pre-launch checklist
- `ai-policy.md` — notes on how to think about AI crawler policy choices
- `LICENSE` — MIT

## Recommended use

Use the root `public/` files as your default starter.

If a project is strongly documentation-focused or marketing-focused, start from one of the templates instead:

- `templates/marketing/`
- `templates/docs/`

## Deploy targets

These files should end up at the web root:

- `https://YOURDOMAIN.com/robots.txt`
- `https://YOURDOMAIN.com/llms.txt`

## Customize before deploy

Search and replace these placeholders:

- `YOURDOMAIN.com`
- `YOUR SITE NAME`
- example URLs
- allowed or blocked crawler rules

## GitHub quick start

```bash
git init
git add .
git commit -m "Initial commit for robots.txt and llms.txt starter"
git branch -M main
git remote add origin https://github.com/YOUR-USER/YOUR-REPO.git
git push -u origin main
```

## Notes

- `robots.txt` is the real control point.
- `llms.txt` is optional and helpful for discoverability/clarity.
- `ai.txt` is not included because it is not yet a broadly established standard.
