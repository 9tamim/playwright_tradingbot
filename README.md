README.md:

Full documentation. Let me structure:

    Title + badges-ish summary

    Overview

    File structure

    Quick start / deployment

    Configuration (PW_CONFIG, PW_AUTOMATION)

    SEO / GEO / AEO setup

    Analytics (GA4, Meta, TikTok, etc.)

    UTM tracking rules

    AI discovery (llms.txt, robots.txt, sitemap)

    IndexNow (fast indexing without Google)

    Event tracking reference

    Consent flow

    Testing / validation

    Changelog

    Support

Let me write this thoroughly but organized.

I should also include a Bengali quick-note section since user speaks Bengali, or keep it English for professionalism. I'll do English with a small Bangla summary at the top or notes in key sections.

Actually let me put a brief Bangla "শুরুর নির্দেশিকা" at the end or top.

Let me draft:
markdown

# Pipwright AI Forex Bots

Landing page for Pipwright — a cloud platform that runs six AI forex trading bots on MetaTrader 5, cTrader and TradingView.

**Live URL:** https://yourdomain.com/
**Status:** Production-ready (replace placeholders before deploy)
**Last updated:** 2026-11-12

---

## 1. Overview

Pipwright is an automated forex trading platform. The site is a single-page landing site with:

- **Six bots:** Trendline, Open Range Scalper, Rangekeeper, Newsdesk, Carry Compass, Hedge Guard
- **Market sessions:** live 24-hour UTC band showing Sydney, Tokyo, London, New York and the overlap
- **Live-style chart:** client-side simulated candlestick chart with EMA overlays
- **Risk calculator:** the exact position sizing formula used by the bots
- **Pricing:** Starter ($0), Pro ($49/mo), Desk ($199/mo)
- **Waitlist / order forms** with Make.com + Stripe automation
- **AI chatbot** ("Pip") that answers product questions
- **Marketing tooling:** UTM builder, share grid, campaign tracking

Design system: engineered chart paper. Bricolage Grotesque + Instrument Sans + IBM Plex Mono. Light and dark themes with system preference detection.

---

## 2. File structure

| File | Purpose |
|---|---|
| `index.html` | The full landing page (HTML, CSS, JS inline) |
| `llms.txt` | Markdown index for LLM and AI agents |
| `sitemap.xml` | XML sitemap for search engines |
| `robots.txt` | Crawl policy, including AI user agents |
| `_headers` | Security and cache headers (Netlify / Cloudflare Pages) |
| `_redirects` | Optional redirects (Netlify only) |
| `indexnow-ping.sh` | IndexNow submission for Bing, Yandex, Naver |
| `README.md` | This file |

---

... etc

Let me write this out fully.

For deployment quick start, include Netlify, Cloudflare Pages, Vercel commands.

For configuration, show PW_CONFIG and PW_AUTOMATION with example values.

For SEO/GEO/AEO, list what's implemented and what to do on the marketing side.

For analytics, list event names and how to verify in GA4 DebugView, Meta Pixel Helper, etc.

For UTM rules, the controlled vocabulary table.

For AI discovery, explain llms.txt format, robots.txt AI bots, sitemap, and the fast non-Google indexing path (IndexNow).

For testing, validation links (Schema validator, PageSpeed, etc.).

For changelog, mention the head fix.

Let me also add a "Pre-launch checklist" section which is very useful.

Then Bengali short guide at the end.

Let me write it all now.

I'll keep it comprehensive but scannable with clear headers and tables.

Let me make sure the URLs are consistent placeholder https://yourdomain.com/.

Also add "Last reviewed" section date to match the page.

Let me finalize the four files now. I'll present them in clearly labeled code blocks.
Pipwright — চারটা ফাইল (llms.txt, sitemap.xml, robots.txt, README.md)

নিচের চারটা ফাইল কপি করে আপনার সাইটের রুট ডিরেক্টরিতে রাখুন। শুধু yourdomain.com আর your-indexnow-key বদলাবে।
1. llms.txt
text

# Pipwright

> Pipwright is a cloud platform that runs six AI-driven forex trading bots on MetaTrader 5, cTrader and TradingView accounts. Each bot targets one trading style (trend, scalping, range, news, carry, or hedge overlay) and applies fixed risk rules, spread filters and a news blackout before every order. It connects with trade-only permissions, so it cannot withdraw funds.

Pipwright is trading software, not a broker and not investment advice. Forex on margin carries a high risk of loss. Backtested and paper results do not predict future returns.

## Overview

- Category: Automated forex trading software (SaaS)
- Platforms: MetaTrader 5, cTrader, TradingView webhooks
- Instruments: 28 major and minor currency pairs (Pro and Desk plans); 3 pairs on Starter paper mode
- Access model: Trade-only broker permissions. No withdrawal or transfer rights.
- Trading modes: Backtest, paper trading (free), live
- Hosting: Cloud. No VPS or desktop terminal required.
- Pricing: Starter $0/mo, Pro $49/mo, Desk $199/mo
- Availability: Worldwide, subject to local regulation and broker acceptance
- Founded: 2026
- Last reviewed: 2026-11-12

## Main pages

- [Pipwright home](https://yourdomain.com/): Six AI forex bots, market sessions, risk calculator, pricing.
- [Bot lineup](https://yourdomain.com/#bots): Compare all six bots with timeframes, holding times, reads, safeguards and risk profiles.
- [Market sessions](https://yourdomain.com/#sessions): 24-hour UTC session band for Sydney, Tokyo, London, New York and the London–New York overlap.
- [How it works](https://yourdomain.com/#how): Four-step onboarding from broker connection to live trading.
- [Engine architecture](https://yourdomain.com/#engine): Signal, execution, risk and operations layers inside every bot.
- [Risk calculator](https://yourdomain.com/#calculator): Position sizing formula used by every bot.
- [Pricing](https://yourdomain.com/#pricing): Starter, Pro and Desk plan comparison.
- [Availability](https://yourdomain.com/#coverage): Regional notes for Europe, Asia-Pacific, South Asia, Middle East and Africa, North America, Latin America.
- [FAQ](https://yourdomain.com/#faq): Definitions, platform support, risk management, legality, currency pairs.
- [Campaign link builder](https://yourdomain.com/#promote): UTM-tagged share links for marketing.

## The six bots

- **Trendline** — Trend following on H1/H4. Holds 1 to 5 days. London and New York sessions. Rides multi-day moves, cuts losers early, skips ranging markets.
- **Open Range Scalper** — Session scalping on M1/M5. Holds 2 to 30 minutes. London and New York opens. Trades the first breakout after the open; stands down when spreads widen.
- **Rangekeeper** — Range mean reversion on M15/H1. Holds 1 to 12 hours. Sydney and Tokyo sessions. Fades quiet Asian-session ranges, exits the moment a breakout starts.
- **Newsdesk** — Event-driven on M1/M5. Holds minutes. Release windows (13:30 and 15:00 UTC common). Reads central bank statements and data releases for surprise, then trades the first move or stays out.
- **Carry Compass** — Swing carry on D1. Holds 2 to 8 weeks. Checks once per day at New York close. Holds pairs with the widest interest rate gap in the direction of trend; exits when volatility spikes.
- **Hedge Guard** — Risk overlay at account level. Always on. Caps net exposure per currency, trims positions as drawdown rises, can flatten all accounts. Places no trades by itself.

## Risk model

- Fixed fractional position sizing: lot size = (balance × risk %) ÷ (stop pips × pip value per lot)
- Spread and slippage guard blocks orders when the live spread exceeds the bot's ceiling
- News blackout pauses every bot around scheduled economic releases
- Daily, weekly and equity loss caps pause all bots at once
- Kill switch closes all open positions with a single action
- Backtester and paper mode let you forward-test on live prices without risking capital

## Pricing

- **Starter** — $0/month. Paper trading only. One bot at a time. 3 currency pairs. 30-day trade journal.
- **Pro** — $49/month. All six bots. Live trading on one broker account. 28 currency pairs. Full backtester and CSV export.
- **Desk** — $199/month. Up to five broker accounts. Hedge Guard across all accounts. Webhooks and REST API. Priority support.

## What Pipwright is not

- Not investment, tax or legal advice.
- Not a profit guarantee. No bot can guarantee returns.
- Not a broker. Pipwright connects to the broker you already use.
- Not able to withdraw funds. Trade-only permissions keep money at your broker.
- Not a hedge fund or managed account service.

## Key definitions

- **AI forex bot** — Software that analyses currency prices and news, decides when to buy or sell, and sends orders to your broker without manual clicks. Pipwright bots use machine learning to classify market regimes and read headlines, and fixed rules to size trades and cap losses.
- **Paper trading** — Running a bot on live market prices with simulated money. No real capital at risk.
- **Trade-only access** — Broker permissions that allow placing, modifying and closing orders, but not withdrawing or transferring funds.
- **Regime classifier** — A model that labels each pair as trending, ranging or volatile on every new candle, so a bot only trades the conditions it was built for.

## Optional

- [llms-full.txt](https://yourdomain.com/llms-full.txt): Concatenated plain-text version of the landing page for retrieval-augmented generation.
- [Sitemap](https://yourdomain.com/sitemap.xml): XML sitemap for search engines.
- [Robots](https://yourdomain.com/robots.txt): Crawl policy, including AI user agents.

2. sitemap.xml
xml

<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9"
        xmlns:xhtml="http://www.w3.org/1999/xhtml">
  <url>
    <loc>https://yourdomain.com/</loc>
    <lastmod>2026-11-12</lastmod>
    <changefreq>weekly</changefreq>
    <priority>1.0</priority>
  </url>
</urlset>

নোট: sitemap-এ #bots, #pricing-এর মতো anchor URL দেওয়া যায় না — শুধু পূর্ণ পেজ URL চলে। এক পেজের সাইট হওয়ায় একটাই <url> entry থাকবে। পরে আলাদা পেজ (blog, docs) বানালে সেগুলো এখানে যোগ করবেন।
3. robots.txt
text

# Pipwright — https://yourdomain.com/
# Crawl policy for search engines and AI agents.
# Updated: 2026-11-12

# ── Default: allow crawling, block obvious private paths ──
User-agent: *
Allow: /
Disallow: /api/
Disallow: /admin/
Disallow: /private/

# ── AI / LLM crawlers — explicitly allowed ──
User-agent: GPTBot
Allow: /

User-agent: OAI-SearchBot
Allow: /

User-agent: ChatGPT-User
Allow: /

User-agent: ClaudeBot
Allow: /

User-agent: Claude-Web
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: Google-Extended
Allow: /

User-agent: Applebot-Extended
Allow: /

User-agent: CCBot
Allow: /

User-agent: Meta-ExternalAgent
Allow: /

User-agent: Bytespider
Allow: /

User-agent: cohere-ai
Allow: /

# ── Sitemap ──
Sitemap: https://yourdomain.com/sitemap.xml

# ── LLM discovery ──
# The AI-readable index for this site is at:
# https://yourdomain.com/llms.txt

নোট: llms.txt-কে Sitemap: লাইনে দেবেন না — ওটা শুধু XML sitemap-এর জন্য। উপরে কমেন্ট হিসেবে রেখেছি যাতে parser গুলো confuse না হয়।
4. README.md
markdown

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

_headers is picked up automatically.
Cloudflare Pages
bash

wrangler pages deploy . --project-name=pipwright

_headers is picked up automatically.
Vercel
bash

vercel --prod

Vercel ignores _headers. Use vercel.json if you need custom headers.
Any static host (GitHub Pages, S3, nginx)

Upload all files to the web root. _headers will not apply — configure headers at the server level.
4. Configuration

Both config objects live near the bottom of index.html, in two <script> blocks before the main marketing script.
4.1 window.PW_CONFIG — analytics and pixels
js

window.PW_CONFIG = {
  gtm: "",                          // GTM-XXXXXXX  (use this OR ga4, not both)
  ga4: "",                          // G-XXXXXXXXXX
  googleAds: "",                    // AW-1234567890
  googleAdsLeadLabel: "",           // AbC-dEfGhIjK
  googleAdsPurchaseLabel: "",       // LmN-oPqRsTuV
  metaPixel: "",                    // 1234567890
  tiktok: "",                       // XXXXXXXXXXXXXXXX
  linkedin: "",                     // 1234567
  clarity: "",                      // abcdefghij
  hotjar: "",                       // 1234567
  plausibleDomain: ""               // example.com (cookieless)
};

Leave a value empty to keep that platform off. Tags load only after the visitor accepts cookies, except Plausible which is cookieless and loads immediately.
4.2 window.PW_AUTOMATION — Make.com webhook
js

window.PW_AUTOMATION = {
  webhook: "",                      // https://hook.eu2.make.com/xxxxxxxx
  token: "",                        // long random string checked by a Make filter
  botName: "Pip"
};

One webhook handles four payload types: chat, lead, order, order_status. Without a webhook the page runs in demo mode — the chatbot answers locally, the waitlist says "demo mode", and the order form shows a placeholder checkout.
5. SEO, GEO and AEO
5.1 What is already implemented

    <head> is fully valid. <title>, description, robots, author, theme-color, Open Graph, Twitter Card, canonical, and font preconnects all live in <head>.

    Canonical URL to prevent anchor duplicates from splitting ranking signals.

    Sitemap, robots and llms.txt referenced from <head> via <link> tags.

    Seven JSON-LD blocks in <head>:

        Organization

        WebSite

        SoftwareApplication (with offers for the three plans)

        ItemList (the six bots)

        HowTo (four-step onboarding)

        WebPage (with speakable spec and audience)

        BreadcrumbList (absolute URLs)

        FAQPage (ten questions)

    Speakable spec on #h1 and #what p for voice assistants.

    Answer-first content: the "What is Pipwright?" section opens with a bold, self-contained answer.

    Comparison table: regional availability with scope="row" and scope="col" for AEO extraction.

    Stable heading IDs: #bots, #sessions, #calculator, #pricing, #faq, #coverage. Keep these — llms.txt and any AI citations point at them.

5.2 GEO guidelines (content side)

Generative Engine Optimization targets citations in ChatGPT, Perplexity, Gemini and Google AI Overviews. The page already has the structural ingredients. To push it further:

    Every section opens with a 40–60 word answer that can be extracted alone. The existing "Definition" paragraph is the model.

    Cite external sources for factual claims. For example, the claim that London–New York overlap (12:00–16:00 UTC) is the deepest liquidity period should link to a reputable source (BIS, a central bank publication, or a top-tier broker's research page). Statistics and citations boost AI visibility substantially.

    Keep sentences self-contained. Avoid pronouns that only work in context. "It cuts losing trades early" → "The Trendline bot cuts losing trades early."

    Publish an /llms-full.txt with the full text of the page in plain Markdown if you want RAG tools to ingest it cleanly.

5.3 AEO guidelines (schema side)

    Do not add aggregateRating unless you have real, verifiable reviews. Fabricated ratings get penalised.

    Keep FAQPage answers direct in the first sentence, then expand.

    Add softwareVersion and screenshot to SoftwareApplication when available.

6. Analytics
6.1 Platforms supported
Platform	Loaded when	Event transport
GA4	PW_CONFIG.ga4 is set and consent given	gtag('event', …) + dataLayer
Google Ads	PW_CONFIG.googleAds is set and consent given	gtag conversion events
Meta Pixel	PW_CONFIG.metaPixel is set and consent given	fbq('track', …)
TikTok Pixel	PW_CONFIG.tiktok is set and consent given	ttq.track(…)
LinkedIn Insight	PW_CONFIG.linkedin is set and consent given	lintrk
Microsoft Clarity	PW_CONFIG.clarity is set and consent given	Loads tag
Hotjar	PW_CONFIG.hotjar is set and consent given	Loads tag
Plausible	PW_CONFIG.plausibleDomain is set	Cookieless, loads immediately
GTM	PW_CONFIG.gtm is set and consent given	dataLayer
6.2 Event reference

Every event lands in dataLayer and is forwarded to loaded platforms.
Event	Fired when	Key fields
pw_page_context	Page loads	path, referrer, utm
pw_consent_update	Visitor accepts or declines	granted
cta_click	Any .btn or .chip is clicked	label, href
bot_view	A bot tab is opened	bot
calculator_use	Calculator input changes	—
faq_open	FAQ <details> opens	q
section_view	A <section> becomes 50% visible	section
scroll_depth	25/50/75/100% scroll	percent
share	Share chip or copy-link clicked	network
utm_link_created	UTM link copied	link
generate_lead	Waitlist submitted	method
begin_checkout	Order form submitted	value, currency, items
purchase	Stripe success (needs Make handshake)	transaction_id, value
chat_open	Chat panel opened	—
chat_message	User sends a chat message	length
chat_action	Chat quick-chip pressed	action
6.3 Verifying in GA4

    GA4 → Admin → DebugView.

    Open the site with consent accepted.

    Click a CTA, open a bot tab, use the calculator, submit the waitlist.

    Each event should appear within 30 seconds. If not, check the browser console for dataLayer pushes.

6.4 Verifying with Meta Pixel Helper

Install the Pixel Helper extension → open the site → accept consent → click a CTA. You should see PageView, then Lead on waitlist submit, InitiateCheckout on order submit.
7. UTM rules (controlled vocabulary)

Every campaign uses lowercase, one-token values. GA4 is case-sensitive, so Facebook and facebook become two different sources.
Parameter	Rule	Good	Bad
utm_source	lowercase, one token	google, newsletter, linkedin	Google, Newsletter Blast
utm_medium	category, not placement	cpc, email, social, referral	Google Ads, social-media
utm_campaign	{quarter}_{objective}_{audience}	2026q4_paper-trading_retail	launch, promo

The campaign link builder at #promote already normalizes values: it lowercases, replaces whitespace with _, and strips anything outside a–z 0–9 _ -. The same normalizer is applied to the attribution payload that goes to Make.

First-touch attribution is stored in localStorage under pw_first_touch on the visitor's first arrival with a UTM or external referrer. Last-touch is read from the current URL. Both are joined to the waitlist and order payload so downstream CRM joins work.
8. AI discovery (llms.txt, robots.txt, sitemap)
8.1 llms.txt

A Markdown index at https://yourdomain.com/llms.txt. Structure:

    # Product name

    > One-paragraph summary

    ## Overview — key facts as bullets

    ## Main pages — links to canonical URLs and stable anchors

    Domain-specific sections (bots, pricing, risk model, definitions)

    ## Optional — secondary resources like llms-full.txt

Linked from <head> via <link rel="alternate" type="text/markdown" href="/llms.txt">.
8.2 robots.txt

Explicitly allows the major AI crawlers — GPTBot, OAI-SearchBot, ClaudeBot, PerplexityBot, Google-Extended, Applebot-Extended, CCBot, Meta-ExternalAgent, Bytespider, cohere-ai. Allows default crawling for search engines and blocks /api/, /admin/, /private/.
8.3 sitemap.xml

Single-page site → one <url> entry. Anchors are not valid in sitemaps (they share the parent URL), so do not add #bots or #pricing to the sitemap.
9. Fast indexing without Google

Google is not the fastest path. Use IndexNow and the sitemap ping to reach Bing, Yandex, Naver, Seznam and Yep within hours.
9.1 IndexNow setup

    Pick a random hex key (32+ characters). Example: a1b2c3d4e5f60718293a4b5c6d7e8f90.

    Host it at https://yourdomain.com/{key}.txt. The file contains only the key, no newline.

    On every deploy or content update, run:

bash

./indexnow-ping.sh

The script posts the URL list to https://api.indexnow.org/indexnow. All participating engines share the feed.
9.2 Sitemap ping

After every update:
bash

curl "https://www.bing.com/ping?sitemap=https://yourdomain.com/sitemap.xml"
curl "https://webmaster.yandex.com/ping?sitemap=https://yourdomain.com/sitemap.xml"

9.3 Manual submit (one-time)

    Bing Webmaster Tools — add the site, verify via DNS or meta tag, submit the sitemap.

    Yandex Webmaster — same.

    Naver Search Advisor — submit sitemap.

    Seznam — submit sitemap.

These usually index within a day. Google Search Console is optional but recommended for Search performance reporting; it is not required for discovery.
10. Consent flow

    On page load, gtag('consent', 'default', …) is called with all categories denied. This satisfies Google Consent Mode v2.

    If pw-consent is yes in localStorage, consent is immediately updated to granted and platforms load.

    If pw-consent is no, nothing loads except Plausible (cookieless) if configured.

    If no choice exists, the consent banner appears and Plausible (if configured) still loads.

    Accepting sets pw-consent = yes and calls initPlatforms(). Declining sets pw-consent = no. The "Cookie settings" link in the footer resets the choice.

To comply with GDPR, the banner must be visible before any cookie-based tag fires. This is already handled — do not move the consent check earlier.
11. Pre-launch checklist

    □

    Replace every https://yourdomain.com/ with the production domain (index.html canonical, breadcrumb JSON-LD, UTM builder, llms.txt, sitemap.xml, robots.txt).
    □

    Fill window.PW_CONFIG with real GA4 / Meta / TikTok IDs.
    □

    Fill window.PW_AUTOMATION.webhook and token with the Make webhook and its filter token.
    □

    Generate an IndexNow key, place it at /{key}.txt, update indexnow-ping.sh.
    □

    Deploy to Netlify or Cloudflare Pages so _headers applies.
    □

    Run ./indexnow-ping.sh after the first deploy.
    □

    Submit sitemap.xml to Bing Webmaster Tools and Yandex Webmaster.
    □

    Validate schema with https://validator.schema.org/ and https://search.google.com/test/rich-results.
    □

    Run Lighthouse (mobile and desktop) and confirm accessibility, best practices and SEO pass.
    □

    Test consent flow: deny → no tags fire; accept → tags fire.
    □

    Test waitlist and order forms in demo mode, then with the live webhook.
    □

    Confirm the Make webhook returns Access-Control-Allow-Origin: * (or the exact origin) or forms will fail silently in production.
    □

    Replace the two owner-only <details> blocks in the footer or remove them.
    □

    Update the risk warning and legal footer with your registered entity name and contact address.

12. Validation and testing
Tool	URL	What it checks
Schema validator	https://validator.schema.org/	JSON-LD syntax and required fields
Rich Results Test	https://search.google.com/test/rich-results	FAQ, HowTo, SoftwareApplication eligibility
PageSpeed Insights	https://pagespeed.web.dev/	Core Web Vitals
W3C HTML validator	https://validator.w3.org/	HTML structure
Meta Pixel Helper	Chrome extension	PageView, Lead, InitiateCheckout, Purchase
GA4 DebugView	GA4 → Admin → DebugView	Event fire order and parameters
Bing URL Inspection	Bing Webmaster Tools	IndexNow acknowledgement
IndexNow test	https://www.indexnow.org/	Feed acceptance
13. Changelog
2026-11-12 — head fix and marketing script completion

    Moved <title>, all <meta> tags, font links and every JSON-LD block from <body> into <head>.

    Removed duplicate viewport meta (claude:viewport-fit-sides).

    Added <html lang="en">.

    Added canonical, sitemap, and llms.txt alternates.

    Fixed BreadcrumbList to use absolute URLs instead of #top and #bots.

    Completed the marketing script (was truncated mid-object). Added renderStatus, initPlatforms, consent gating, attribution, all event handlers, share grid, UTM builder, waitlist, order form, chat.

    Defaulted window.PW_AUTOMATION so the page does not throw when only PW_CONFIG is set.

14. Support and ownership

For schema questions, run the validator first. For Make.com webhook debugging, check the Make execution log and confirm the response module includes a CORS header. For analytics mismatches, compare the GA4 DebugView timestamp to the browser dataLayer push.

Contact: hello@yourdomain.com (placeholder — replace before launch).
15. সংক্ষিপ্ত বাংলা গাইড (quick Bengali notes)

    ডিপ্লয় করার আগে — index.html, llms.txt, sitemap.xml, robots.txt — চার ফাইলের ভেতরে yourdomain.com খুঁজে নিজের ডোমেইন বসান।

    PW_CONFIG-এ GA4 (G-XXXXXXXX) আর Meta Pixel ID বসালেই ট্র্যাকিং চালু হবে। Cookie accept করার পরেই ট্যাগ লোড হবে।

    Make.com webhook পেলে PW_AUTOMATION.webhook-এ বসান। না বসালে সাইট demo mode-এ চলবে — চ্যাটবট লোকাল উত্তর দেবে, ফর্ম "demo" দেখাবে।

    IndexNow — একটা ৩২+ অক্ষরের hex key বানান, /{key}.txt ফাইলে রাখুন, indexnow-ping.sh-এ key বসিয়ে deploy শেষে ./indexnow-ping.sh চালান। Bing, Yandex, Naver কয়েক ঘণ্টায় ইনডেক্স করবে।

    Google ছাড়া দ্রুত ইনডেক্স — উপরের IndexNow + Bing/Yandex sitemap ping। Google Search Console লাগবে না, শুধু পরে রিপোর্ট দেখতে চাইলে যুক্ত করবেন।

    llms.txt — ChatGPT, Perplexity, Claude-রা এই ফাইল পড়ে সাইটের সারসংক্ষেপ পায়। নতুন পেজ বা ফিচার যোগ করলে এখানেও যোগ করবেন।

    sitemap.xml-এ anchor (#bots ইত্যাদি) দেবেন না — শুধু পুরো পেজ URL চলে।

text


---

## ফাইল রাখার নিয়ম

your-site-root/
├── index.html ← আপনি আগেই ঠিক করেছেন
├── llms.txt ← উপরের ফাইল ১
├── sitemap.xml ← উপরের ফাইল ২
├── robots.txt ← উপরের ফাইল ৩
├── README.md ← উপরের ফাইল ৪
└── {your-indexnow-key}.txt ← পেলেন IndexNow setup-এ
text


`yourdomain.com` আর `your-indexnow-key` বদলানো ভুলবেন না — এই দুটো ছাড়া ফাইলগুলো কাজ করবে না।

