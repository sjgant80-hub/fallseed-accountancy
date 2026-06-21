# FallSeed Accountancy Firm

> **A Progressive Web App (PWA) seed for UK Accountancy firms.**
> One HTML file. Four base tools + LLM-agnostic build engine + Fork Seed packager. MIT. Sovereign.

**Live:** https://sjgant80-hub.github.io/fallseed-accountancy/

## What this is

`fallseed-accountancy` is a single HTML file you can save to your desktop or install as a PWA. It bundles:

- The four base tools of the Accountancy wedge (anchor / onboard / paper / practice)
- A build engine that generates new tools on demand using any LLM (WebLLM in-browser, ollama / LM Studio local, Groq / OpenRouter free cloud, or BYOK paid)
- A Fork Seed packager that lets you mutate the seed for a different vertical or client

## Vertical context

Accountancy · tax · bookkeeping (UK).

## Base tools

| Role | Tool | Purpose |
|---|---|---|
| anchor | [`fallbooks`](https://sjgant80-hub.github.io/fallbooks/) | Client register · services · fee schedules · deadlines (SA / CT / VAT / PAYE / CS01 / PSC) · engagement records · 12-pt compliance |
| onboard | [`fallbooksonboard`](https://sjgant80-hub.github.io/fallbooksonboard/) | Client onboarding · CDD / AML risk assessment · PEP screen · engagement letter · AAS · 64-8 authorisations · MTD signup |
| paper | [`fallbookspaper`](https://sjgant80-hub.github.io/fallbookspaper/) | Engagement letters · 64-8 · AAS · disengagement · fee proposals · Senior Accounting Officer · LOR · Management letter templates |
| practice | [`fallbookspractice`](https://sjgant80-hub.github.io/fallbookspractice/) | Workflow · job tracker · review sign-offs · CPD log · AML reviews · file reviews · PII renewal · ethical conflicts log |

## Architecture

- **One HTML file** — no build step, no server, no install
- **IDB primary** — every record lives in `IndexedDB` (`fallseed-accountancy-v2`) on your device
- **BroadcastChannel mesh** — `fall-accountancy` for cross-tool sync; `fall-signal` for global hello
- **Mansoor P3 audit chain** — `prevHash` + SHA-256 chained entries on every mutation
- **8-provider LLM cascade** — WebLLM (T1) → ollama / LM Studio (T2) → Groq / OpenRouter free / Google / Cerebras (T3-free) → Anthropic (T3-paid)
- **Streaming** — SSE token-by-token output
- **Fork Seed packager** — serialises a mutated SEED back into a new self-contained HTML

## Sovereignty

- MIT-licensed
- No telemetry, no analytics, no tracking
- All data stays on your device (IDB) — nothing posted unless you wire an external LLM
- Works offline once installed as PWA
- One-time payment; upgrades optional

## Cosmology

Prime **1051**, spine-clean mod 127. Mesh channel **`fall-accountancy`**. Bundle roles **anchor / onboard / paper / practice**. Seal **◊·κ=1**.

Part of the FallSeed family — see [www.ai-nativesolutions.com](https://www.ai-nativesolutions.com).

## Licence

MIT © Simon Gant.
