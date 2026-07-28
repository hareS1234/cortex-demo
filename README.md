# CorteX demo site

Public pages for reviewing the CorteX government-services prototype.

| Page | What it is |
|---|---|
| [`/`](index.html) | Six-slide product walkthrough. The two demo buttons open the live assistants. |
| [`/dashboard.html`](dashboard.html) | CortexAI monitoring dashboard. **Every figure is simulated** for prototype review. |

## Live assistants

These run on the pilot FastGPT instance and open in a new tab:

- Tax deduction wizard (social, property, standard): `http://136.110.71.182:3000/chat/share?shareId=rJaRduIWtzP5vtpWLTXi5uG0`
- Pension assistant: `http://136.110.71.182:3000/chat/share?shareId=mqjpC7dgS5XjFl2Iw0EyMKPA`
- Tax deductions: `http://136.110.71.182:3000/chat/share?shareId=qz4rTiWYmJWhaYkp7Di1M3OA`
- OSAGO: `http://136.110.71.182:3000/chat/share?shareId=ipRUObNLB2SgEKV0xEuOMrHt`

## Why the demos open in a new tab here

This site is served over HTTPS and the pilot instance over plain HTTP, so browsers block
embedding it in a frame (mixed content). The local copy of the deck in `portal/index.html`
embeds the assistants in a popup window instead, and is what to present from.

Put TLS in front of the pilot instance and the embedded version works here too. The nginx
configuration for that is in the main repository under
`cortex-mvp/fastgpt/deploy/`.

## Source

Generated from `portal/` in the CorteX working repository. Do not edit these files directly;
edit the source and regenerate, otherwise the next build overwrites your changes.
