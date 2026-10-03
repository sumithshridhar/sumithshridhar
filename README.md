# Sumith Shridhar

**I build AI systems that run unattended in production — and that show their own failure rates.**

Bengaluru, India · self-taught · B.Com (Data Analytics, 2025)

Most AI demos work once, on stage. I'm more interested in the boring part: what happens on day 90, at 3am, when nobody is watching and the input is malformed. Every project below has some version of the same idea baked in — **a system that tells you when it is wrong.**

> **Open to junior AI / automation / forward-deployed engineering roles at Bengaluru startups** (on-site or hybrid) or remote. Immediate joiner. DM me on [LinkedIn](https://www.linkedin.com/in/sumith-shridhar-b9919924a/) or [X](https://x.com/sumithshridhar).

---

## 🆕 Shipped in September 2026

- **[ghost-ops-jev-buildathon](https://github.com/sumithshridhar/ghost-ops-jev-buildathon)**: runtime guard rules for a finance-ops agent (Jev Buildathon, team of 2). Every tool call is checked against the finance policy before it runs: bank-detail changes without a callback, split payments, refunds to new accounts, sanctioned vendors. No harmful action got through in the 13 practice tasks while real invoices still got paid; 59/59 scenario tests on unseen data.
- **[gh01-twin](https://github.com/sumithshridhar/gh01-twin)** ([live demo](https://sumithshridhar.github.io/gh01-twin/)): an interactive 3D twin of a small AI + robotics tomato greenhouse (115 components, design and simulation only). The AI suggests, a safety PLC decides, hard-wired cut-offs protect. Filming its failure tests (pump failure, water shortage) exposed 3 bugs in my own safety logic, all fixed.
- **[shorts-pipeline-hardening](https://github.com/sumithshridhar/shorts-pipeline-hardening)**: 3 production bug postmortems from an unattended Shorts pipeline. A bug that deleted a finished video and logged it as a success, an `open(path, "w")` that could zero the whole script queue, and a copy-pasted codebase that let one channel ship another's content.
- **[n8n-content-automation](https://github.com/sumithshridhar/n8n-content-automation)**: the n8n workflows behind it. A generator → critic LLM loop, a fully-local Ollama + SSH rebuild, and vision-verified, retry-robust phone automation over ADB.
- **[binance-trading-algo](https://github.com/sumithshridhar/binance-trading-algo)**: a Binance backtest + paper-trading engine built to say no. Next-bar fills, real fees, and a split-half bake-off of six classic strategies against buy & hold.

---

## What I build

### 🔎 [glassbox-pro](https://github.com/sumithshridhar/glassbox-pro) — grounded crime intelligence
Built for the **Karnataka State Police Datathon 2026** (Challenge 1), entirely on Zoho Catalyst.

Ask a question in **English or Kannada**, typed or spoken, and get an answer computed **only from case records** — never generated. Every claim cites the FIR numbers it came from, and each citation is re-verified against the datastore before it renders. If the data isn't there, it says "no records found" instead of inventing one.

- 6 police roles with jurisdiction scoping enforced **server-side**, not hidden in the browser
- Explainable 0–100 offender risk scores — every point itemised with its supporting case
- Money-trail engine tracing mule → collector → cash-out using real AML typologies
- **A forecast that grades itself:** hides its own most recent 30 days, re-runs on older data, and publishes precision — hits *and* misses
- Aligned to the official CCTNS FIR schema (18-digit CrimeNo, BNS 2023 sections, chargesheet A/B/C)

`Node.js` `Zoho Catalyst` `Serverless` `RAG` `Kannada NLP`

### 📉 [trading-algoo](https://github.com/sumithshridhar/trading-algoo) — a backtester built to stop me lying to myself
The engine's #1 job is **not** finding winning strategies. It's refusing to show me a fake one.

- **Next-bar execution** — a decision on bar N can only fill at bar N+1's open, which makes lookahead bias *structurally impossible* rather than merely discouraged
- **An integrity pass before any strategy runs** — gaps, duplicate bars, timezone mistakes, impossible candles (high below low), suspected un-adjusted stock splits, missing values. Bad data in, the backtest never starts
- Real Indian costs charged on every trade: brokerage, STT, exchange fees, SEBI fee, stamp duty, GST, slippage
- Walk-forward testing, Monte Carlo resampling, parameter-sensitivity heatmaps
- A **multiple-testing penalty** that rises with every variant tried — and a permanent count of every variant ever tested, because forgetting your failures inflates everything after them
- Scorecards attach warnings when the evidence is too thin to believe: too few trades, suspiciously high Sharpe, a drawdown you'd have panicked out of
- 29 test files, in the repo from commit 1

`Python` `pandas` `NumPy` `pytest` `Angel One SmartAPI`

### 🎬 [bloom-cafe](https://github.com/sumithshridhar/bloom-cafe) — a cinematic site that degrades honestly
A scroll-animated café site: the page opens as a solid paper field with the name cut out of it, and scrolling flies the camera through the letter into the room. Plain HTML/CSS/JS + GSAP, no build step.

- If the animation CDN fails to load, the page renders a clean static version instead of a broken one
- Respects `prefers-reduced-motion` — the whole zoom-through is swapped for the settled layout
- Font-loading gate so text never flashes unstyled
- **[Live demo](https://sumithshridhar.github.io/bloom-cafe)**

`HTML` `CSS` `JavaScript` `GSAP` `ScrollTrigger`

---

## How I work

**Unattended-first.** My content pipelines have run daily on schedulers for 5+ months with no manual intervention. That means atomic writes so a mid-run crash never corrupts output, single-instance locks so runs can't collide, never-reuse ID allocation, and quality gates that demand *positive proof* the output is good rather than just checking the job didn't crash.

**Honest measurement over impressive numbers.** I'd rather ship a system that reports 61% precision than one that claims 95% and can't show its working.

---

## Stack

`Python` · `Node.js` · `n8n` · `MCP servers` · `RAG` · `Ollama / local LLMs` · `FastAPI` · `Next.js` · `Playwright` · `FFmpeg` · `Supabase` · `Zoho Catalyst` · `OpenCV`

## Reach me

Open to junior full-time roles at Bengaluru startups, and to freelance work in AI automation, agent systems, and data pipelines.

[LinkedIn](https://www.linkedin.com/in/sumith-shridhar-b9919924a/) · [X](https://x.com/sumithshridhar)
