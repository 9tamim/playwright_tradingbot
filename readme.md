# Pipwright AI Forex Bots — Landing Page

Single-page landing site for **Pipwright**, a cloud platform that runs six AI-driven forex trading bots on MetaTrader 5, cTrader and TradingView.

**Live URL:** `https://yourdomain.com/`
**Status:** Production-ready. Replace placeholders before deploy.
**Last updated:** 2026-11-12

---

## 1. What this site is

A marketing + conversion landing page for a SaaS trading product. It combines:

- **Product story** — six bots, market sessions, engine architecture, risk model
- **Interactive tools** — live simulated candle chart, 24-hour session band, position size calculator
- **Commercial flow** — pricing, order form, waitlist, Stripe checkout redirect
- **AI assistant** — "Pip" chatbot that answers product questions
- **Marketing tooling** — UTM link builder, share grid, campaign attribution
- **Analytics + consent** — GA4, Meta Pixel, TikTok, LinkedIn, Clarity, Hotjar, Plausible, behind a cookie gate

Design system: engineered chart paper. Fonts are Bricolage Grotesque (display), Instrument Sans (body), IBM Plex Mono (data). Light and dark themes follow system preference with a manual override.

---

## 2. File structure

| File | Purpose |
|---|---|
| `index.html` | Full landing page. HTML, CSS, JS all inline. |
| `llms.txt` | Markdown index for LLM and AI agents. |
| `sitemap.xml` | XML sitemap. Single URL for the landing page. |
| `robots.txt` | Crawl policy including AI user agents. |
| `_headers` | Security, MIME and cache headers (Netlify / Cloudflare Pages). |
| `_redirects` | Optional redirects (Netlify only). |
| `indexnow-ping.sh` | IndexNow submission script. |
| `README.md` | This file. |

---

## 3. Quick deploy

### Netlify

```bash
# drag-and-drop the folder at app.netlify.com, or:
netlify deploy --prod --dir=.