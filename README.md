# AI crawlers: the roster we detect, and the ones that reached our site

Two separate things, kept in two separate columns. The **roster** is the list of crawler User-Agents our detection recognises, each traced to the vendor page it was read from and the day somebody read it. The **observation** is whether that crawler actually requested a page on our own site.

🔴 A crawler with no observation is written **not observed**, never `0`. A zero would say we measured it and it did not come. Our site is one site: a crawler absent here can be busy everywhere else, and that absence is a fact about our traffic rather than about the crawler.

## What is in the roster, and what is deliberately not

This table holds the **21 tokens that send a User-Agent**, which is what makes a request countable. Two further tokens we honour in robots.txt are not here and cannot be: `google-extended` and `applebot-extended` are robots.txt control tokens only — the fetch itself is done by Googlebot and Applebot — so no request ever carries them. Listing them would add two rows to the "not observed" column that are not capable of being observed.

Plain search crawlers (Googlebot, Applebot) are also out, by the same rule read the other way: a vendor's search crawler stays out and its AI / non-search crawler comes in. That is why GoogleOther is listed and Googlebot is not.

## The roster

The request counts are totals over the 74 days from 2026-06-26 to 2026-09-07. They are not rates, and they are not per-day.

| Crawler | UA token | Source, and the day it was read | Reached our site |
| --- | --- | --- | --- |
| GPTBot | `gptbot` | [vendor page](https://developers.openai.com/api/docs/bots), read 2026-09-06 | **871 requests** in the 74 days from 2026-06-26 to 2026-09-07 (on 27 of those days; first 2026-06-28, last 2026-09-05) |
| OAI-SearchBot | `oai-searchbot` | [vendor page](https://developers.openai.com/api/docs/bots), read 2026-09-06 | **362 requests** in the 74 days from 2026-06-26 to 2026-09-07 (on 39 of those days; first 2026-07-09, last 2026-09-07) |
| ChatGPT-User | `chatgpt-user` | [vendor page](https://developers.openai.com/api/docs/bots), read 2026-09-06 | **266 requests** in the 74 days from 2026-06-26 to 2026-09-07 (on 44 of those days; first 2026-07-02, last 2026-09-07) |
| ClaudeBot | `claudebot` | [vendor page](https://support.claude.com/en/articles/8896518), read 2026-09-06 | **591 requests** in the 74 days from 2026-06-26 to 2026-09-07 (on 15 of those days; first 2026-07-09, last 2026-09-04) |
| Claude-User | `claude-user` | [vendor page](https://support.claude.com/en/articles/8896518), read 2026-09-06 | **27 requests** in the 74 days from 2026-06-26 to 2026-09-07 (on 14 of those days; first 2026-06-27, last 2026-09-05) |
| Claude-SearchBot | `claude-searchbot` | [vendor page](https://support.claude.com/en/articles/8896518), read 2026-09-06 | **3 requests** in the 74 days from 2026-06-26 to 2026-09-07 (on 1 of those days; first 2026-09-04, last 2026-09-04) |
| PerplexityBot | `perplexitybot` | [vendor page](https://docs.perplexity.ai/guides/bots), read 2026-09-06 | **610 requests** in the 74 days from 2026-06-26 to 2026-09-07 (on 56 of those days; first 2026-06-30, last 2026-09-07) |
| Perplexity-User | `perplexity-user` | [vendor page](https://docs.perplexity.ai/guides/bots), read 2026-09-06 | **25 requests** in the 74 days from 2026-06-26 to 2026-09-07 (on 9 of those days; first 2026-07-19, last 2026-09-04) |
| GoogleOther | `googleother` | [vendor page](https://developers.google.com/crawling/docs/crawlers-fetchers/google-common-crawlers), read 2026-09-06 | **873 requests** in the 74 days from 2026-06-26 to 2026-09-07 (on 55 of those days; first 2026-06-26, last 2026-09-07) |
| Bytespider | `bytespider` | no vendor page — see the note below, read 2026-09-06 | **7 requests** in the 74 days from 2026-06-26 to 2026-09-07 (on 5 of those days; first 2026-07-16, last 2026-09-04) |
| Amazonbot | `amazonbot` | [vendor page](https://developer.amazon.com/amazonbot), read 2026-09-06 | **2,188 requests** in the 74 days from 2026-06-26 to 2026-09-07 (on 59 of those days; first 2026-07-02, last 2026-09-07) |
| Amzn-SearchBot | `amzn-searchbot` | [vendor page](https://developer.amazon.com/amazonbot), read 2026-09-06 | not observed in the 74 days from 2026-06-26 to 2026-09-07 |
| Amzn-User | `amzn-user` | [vendor page](https://developer.amazon.com/amazonbot), read 2026-09-06 | not observed in the 74 days from 2026-06-26 to 2026-09-07 |
| cohere-ai | `cohere-ai` | no vendor page — see the note below, read 2026-09-06 | **1 request** in the 74 days from 2026-06-26 to 2026-09-07 (on 1 of those days; first 2026-07-19, last 2026-07-19) |
| Meta-ExternalAgent | `meta-externalagent` | [vendor page](https://developers.facebook.com/docs/sharing/webmasters/web-crawlers/), read 2026-09-06 | **8,216 requests** in the 74 days from 2026-06-26 to 2026-09-07 (on 38 of those days; first 2026-07-06, last 2026-09-04) |
| meta-webindexer | `meta-webindexer` | [vendor page](https://developers.facebook.com/docs/sharing/webmasters/web-crawlers/), read 2026-09-06 | not observed in the 74 days from 2026-06-26 to 2026-09-07 |
| meta-externalfetcher | `meta-externalfetcher` | [vendor page](https://developers.facebook.com/docs/sharing/webmasters/web-crawlers/), read 2026-09-06 | not observed in the 74 days from 2026-06-26 to 2026-09-07 |
| MistralAI-User | `mistralai-user` | [vendor page](https://docs.mistral.ai/robots), read 2026-09-06 | not observed in the 74 days from 2026-06-26 to 2026-09-07 |
| MistralAI-Index | `mistralai-index` | [vendor page](https://docs.mistral.ai/robots), read 2026-09-06 | not observed in the 74 days from 2026-06-26 to 2026-09-07 |
| MistralAI-Training | `mistralai-training` | [vendor page](https://docs.mistral.ai/robots), read 2026-09-06 | not observed in the 74 days from 2026-06-26 to 2026-09-07 |
| DuckAssistBot | `duckassistbot` | [vendor page](https://duckduckgo.com/duckduckgo-help-pages/results/duckassistbot/), read 2026-09-06 | **1 request** in the 74 days from 2026-06-26 to 2026-09-07 (on 1 of those days; first 2026-09-07, last 2026-09-07) |

### The tokens with no vendor page

Two entries cite no vendor documentation. The choice was between dropping crawlers we can see in our logs, inventing a citation, or saying plainly what the basis is.

- **Bytespider** (`bytespider`), read 2026-09-06 — ByteDance publishes no reachable crawler page: the reference URL inside Bytespider's own User-Agent (zhanzhang.toutiao.com) does not resolve from outside China, so there is nothing to cite that a reader here could open. The token is the literal substring of the UA string as it arrives in our own logs.
- **cohere-ai** (`cohere-ai`), read 2026-09-06 — Cohere publishes no crawler documentation page; the UA is community-confirmed only, and Cohere has separately stated it does not currently crawl for foundation-model training. Kept because the token still appears in logs, and removing an observed crawler to tidy a citation would under-count what actually visits.

## What was observed, and what was not

Over the 74 days from 2026-06-26 to 2026-09-07, **14 of the 21** crawlers in this roster requested a page on our site, and **7** did not. The 14 together account for 14,041 requests in that window.

The 7 not observed: Amzn-SearchBot (`amzn-searchbot`), Amzn-User (`amzn-user`), meta-webindexer (`meta-webindexer`), meta-externalfetcher (`meta-externalfetcher`), MistralAI-User (`mistralai-user`), MistralAI-Index (`mistralai-index`), MistralAI-Training (`mistralai-training`).

Each of those is a crawler we recognise and did not see in that window. We are not saying it does not crawl; we are saying it did not reach this one site while we were counting.

## Where these numbers come from

- **The roster** is our own detection list: one lowercased substring per vendor-published crawler User-Agent, matched case-insensitively against the request header. Every entry carries the vendor page it was read from and the UTC day it was read, because a vendor page changes and "we checked" with no date cannot go stale and so cannot be trusted.
- **The observations** are our own site's access counters for trirankai.com: one row per crawler per UTC day, summed over the 74 days from 2026-06-26 to 2026-09-07, counting HTML page requests only — API, build assets and dotted files are not in these totals.
- This is one site's traffic, not a survey. It says what reached us; it says nothing about how much any of these crawlers fetches elsewhere, and it should not be read as a ranking of the crawlers themselves.
- The measurement was last rebuilt on 2026-09-07. The live version of these counts is published at [/data/ai-crawler-stats](https://trirankai.com/data/ai-crawler-stats).

Both halves are first-party: our own detection list and our own access logs. Neither is an authority on what any vendor does — it is a statement of what we recognise and what we recorded.

Generated by `scripts/build-crawler-roster-doc.ts` from `src/lib/ai-crawlers.ts` and `src/data/ai-crawler-stats.json`. Edit those, not this file.
