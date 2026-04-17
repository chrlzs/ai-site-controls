# Pre-Launch Checklist

## Choose your defaults

- [ ] Pick `conservative`, `balanced`, or `open`
- [ ] Copy the matching preset to your deployed `robots.txt`
- [ ] Choose the generic, marketing, or docs `llms.txt` starter

## Replace placeholders

- [ ] Replace `YOURDOMAIN.com`
- [ ] Replace `YOUR SITE NAME`
- [ ] Replace example navigation links
- [ ] Remove sections that do not apply

## Review crawler policy

- [ ] Confirm whether normal search engines should be allowed
- [ ] Review `crawler-matrix.md` if you changed vendor-specific bot rules
- [ ] Confirm whether OpenAI crawlers should be allowed or blocked
- [ ] Confirm whether Anthropic crawlers should be allowed or blocked
- [ ] Confirm whether Perplexity crawlers should be allowed or blocked
- [ ] Confirm whether any private paths need additional blocking

## Verify deployment

- [ ] `robots.txt` is publicly reachable at `/robots.txt`
- [ ] `llms.txt` is publicly reachable at `/llms.txt`
- [ ] `sitemap.xml` path is correct
- [ ] Canonical URLs are used in `llms.txt`

## Final QA

- [ ] No staging URLs remain
- [ ] No admin/private URLs are listed in `llms.txt`
- [ ] File formatting is plain text and web-server friendly
