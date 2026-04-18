# AI Site Controls 

A public starter for adding `robots.txt` and `llms.txt` to an existing site repo.

Use this when you want a lightweight, copy-pasteable baseline for:

- choosing an AI crawler policy intentionally
- publishing a curated `llms.txt` at `/llms.txt`
- leaving future maintainers a clear paper trail for why the rules look the way they do

## 60-second adoption

1. Choose a `robots.txt` preset from `presets/`.
2. Copy that file and a starter `llms.txt` into the folder your site publishes at the web root, often `public/` or `static/`.
3. Replace placeholders like `YOURDOMAIN.com` and `YOUR SITE NAME`.
4. Deploy and verify these URLs:
   - `https://YOURDOMAIN.com/robots.txt`
   - `https://YOURDOMAIN.com/llms.txt`

If you just want a sensible default, use the root `public/` files. The root `public/robots.txt` matches the balanced preset.

## What This Repo Includes

- `public/robots.txt` — balanced default for many public sites
- `public/llms.txt` — generic starter `llms.txt`
- `presets/conservative/` — block AI-specific bots where possible
- `presets/balanced/` — allow search and user-directed fetch, block training
- `presets/open/` — allow AI search and training broadly
- `templates/marketing/` — `llms.txt` example for marketing, portfolio, and SaaS sites
- `templates/docs/` — `llms.txt` example for docs-heavy sites
- `crawler-matrix.md` — sourced notes on current crawler roles and how this repo maps them
- `ai-policy.md` — short policy framing
- `checklist.md` — pre-launch verification list

## Pick A Preset

The preset names are a repo convention, not an industry standard. The recommendations are inferred from current vendor docs and kept in [`crawler-matrix.md`](./crawler-matrix.md).

| Preset | Best for | Search bots | Training bots | User-directed fetch agents |
| --- | --- | --- | --- | --- |
| `conservative` | teams who want AI visibility off unless intentionally reopened later | block | block | block where possible |
| `balanced` | teams who want discoverability without allowing training | allow | block | allow |
| `open` | teams comfortable with broad AI access | allow | allow | allow |

## Choose Your `llms.txt` Starter

- `public/llms.txt` — generic site starter
- `templates/marketing/public/llms.txt` — marketing or brochureware sites
- `templates/docs/public/llms.txt` — documentation portals and developer docs

## Before You Deploy

Search and replace:

- `YOURDOMAIN.com`
- `YOUR SITE NAME`
- example URLs that do not belong to your site
- any crawler rules that do not match your actual policy

Then run through [`checklist.md`](./checklist.md).

## Notes

- `robots.txt` is the real control surface for crawler access.
- `llms.txt` is optional and advisory. It helps models find canonical public pages, but it does not enforce access.
- `ai.txt` is not included because it is not yet a broadly established standard.
- Bot behavior changes over time. Review [`crawler-matrix.md`](./crawler-matrix.md) before changing vendor-specific rules.
