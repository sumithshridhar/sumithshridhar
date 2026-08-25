# Sumith Shridhar

**I build AI systems that run unattended in production — and that show their own failure rates.**

Bengaluru, India · self-taught · B.Com (Data Analytics, 2025)

Most AI demos work once, on stage. I'm more interested in the boring part: what happens on day 90, at 3am, when nobody is watching and the input is malformed. Every project below has some version of the same idea baked in — **a system that tells you when it is wrong.**

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
- Real Indian costs charged on every trade: brokerage, STT, exchange fees, SEBI fee, stamp duty, GST, slippage
- Walk-forward testing, Monte Carlo resampling, parameter-sensitivity heatmaps
- A **multiple-testing penalty** that rises with every variant tried — and a permanent count of every variant ever tested, because forgetting your failures inflates everything after them
- Scorecards attach warnings when the evidence is too thin to believe: too few trades, suspiciously high Sharpe, a drawdown you'd have panicked out of
- 29 test files, in the repo from commit 1

`Python` `pandas` `NumPy` `pytest` `Angel One SmartAPI`

---

## How I work

**Unattended-first.** My content pipelines have run daily on schedulers for 5+ months with no manual intervention. That means atomic writes so a mid-run crash never corrupts output, single-instance locks so runs can't collide, never-reuse ID allocation, and quality gates that demand *positive proof* the output is good rather than just checking the job didn't crash.

**Honest measurement over impressive numbers.** I'd rather ship a system that reports 61% precision than one that claims 95% and can't show its working.

---

## Stack

`Python` · `Node.js` · `n8n` · `MCP servers` · `RAG` · `Ollama / local LLMs` · `FastAPI` · `Next.js` · `Playwright` · `FFmpeg` · `Supabase` · `Zoho Catalyst` · `OpenCV`

## Reach me

Open to freelance work in AI automation, agent systems, and data pipelines.

[LinkedIn](https://www.linkedin.com/in/sumith-shridhar-b9919924a/)
