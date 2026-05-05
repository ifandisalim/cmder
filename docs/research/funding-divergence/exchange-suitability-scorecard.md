# Exchange suitability scorecard — funding divergence (mid-tier lens)

**Template:** use [`../../templates/exchange-suitability-scorecard.md`](../../templates/exchange-suitability-scorecard.md) for blank rows and spreadsheet column headers.

**Scoring:** each of the **seven** categories below is **0–2** (see template). **Total** = sum of those seven scores (**max 14**). Totals are **tie-breakers only** after knockouts and **hard blockers**.

**Evidence bar:** per project spec, each score should eventually cite official docs, reproducible data pulls, or be marked **unknown** — not guessed. **Access date for URLs cited in repo research:** 2026-05-05 (re-verify before trading).

---

## Knockout rules (any “no” → do not shortlist for trial)

| Knockout | Question |
|----------|----------|
| **K1** | Can you **legally access** perps from your operating jurisdiction (verified, not assumed)? |
| **K2** | Is there a **documented public API** sufficient to fetch funding and trade (even if you start manual)? |
| **K3** | Can you verify **how funding is calculated** in the official docs for the exact contract type? |

If any knockout fails, **stop**—do not proceed to compare headline funding.

---

## Hard blockers (Malaysia lens — from desk research)

These are **flags**, not legal advice. Align with your own compliance review.

| Venue | Hard blocker (Malaysia / ops) |
|-------|-------------------------------|
| **Gate.io** | **Geo:** Malaysia appears on Gate’s **Restricted Locations** — treat as **blocked for MY-resident onboarding** regardless of API quality. |
| **OKX, Bybit, Binance** | **Regulatory / product:** SC enforcement, risk disclosures, or platform announcements cite **Malaysia restrictions** — not usable as MY-accessible legs for this workflow **as described in** [`exchange-research-outputs.md`](exchange-research-outputs.md). |
| **Bitget, MEXC, HTX, BingX, Kraken, KuCoin** | **Alert list / offshore:** Several names appear on the SC **Investor Alert List** while terms may **omit** Malaysia from “prohibited” lists — **two different questions** (onboarding vs regulatory comfort). See longlist table in research outputs. |
| **KuCoin** | **Unknown until verified:** MY **resident** onboarding / KYC outcome was **not** confirmed from a single fetched Terms pass in the starter research — **do not assume** access. |

---

## Longlist score summary (seven categories)

**Legend:** API = API quality · Liq = liquidity · Fund = funding behavior · Cost = costs · Ops = operational reliability · Risk = risk controls · MY = Malaysia accessibility · **T** = total (max 14) · **K** = knockouts all OK? (Y/N/**?** = unknown)

Desk scores below are **starter judgments** from documentation depth, research-output notes, and typical venue profiles — **replace** with your own measured scores before capital deployment.

| Venue | API | Liq | Fund | Cost | Ops | Risk | MY | T | K1 | K2 | K3 | Hard blocker? |
|-------|-----|-----|------|------|-----|------|----|----|----|----|-----|---------------|
| **Bitget** | 2 | 1 | 1 | 1 | 1 | 1 | 1 | 8 | ? | Y | Y | SC alert list; offshore |
| **MEXC** | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 7 | ? | Y | Y | SC alert list; funding/API unknowns |
| **HTX (Huobi)** | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 7 | ? | Y | ? | Domain/branding drift; verify product + docs |
| **BingX** | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 7 | ? | Y | ? | MY = verify Disclaimer country list |
| **Kraken** | 2 | 2 | 2 | 2 | 2 | 2 | 1 | 13 | ? | Y | Y | SC alert list; often “majors” not mid-tier |
| **KuCoin** | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 8 | ? | Y | Y | MY onboarding unknown; SC alert list |
| **Deribit** | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 14 | Y | Y | Y | BTC/ETH-centric; tail alts may be weak |
| **Hyperliquid** | 2 | 1 | 1 | 1 | 1 | 1 | 1 | 8 | ? | Y | Y | Bridge/wallet ops; MY licensing fuzzy |
| **Gate.io** | 2 | 2 | 2 | 2 | 2 | 2 | 0 | 12 | N | Y | Y | **MY geo block** — hard stop for MY residents |
| **dYdX (v4)** | 2 | 1 | 1 | 1 | 1 | 1 | 1 | 8 | ? | Y | Y | Chain-native; hedge vs CEX complexity |

**Why K1 is “?” on many rows:** legal access is **user- and fact-specific**; repo research cites terms and regulator lists but does **not** certify eligibility. Treat **?** as “must verify personally.”

---

## Per-venue notes (required)

### Bitget

| Category | Score | Notes |
|----------|-------|-------|
| API quality | 2 | Public API hub documented ([API intro](https://www.bitget.com/api-doc/common/intro)); typical CEX REST/WS patterns — still dry-run rate limits. |
| Liquidity | 1 | Broad retail perp catalog; **tail symbols** need live depth checks at your size. |
| Funding behavior | 1 | Funding exists on perps; **historical granularity** and **index alignment vs hedge leg** need symbol-level verification. |
| Costs | 1 | Fee tables + campaigns move; lock **your** VIP/tier assumption in writing. |
| Operational reliability | 1 | Global retail exchange ops variance — use status/incident evidence you trust. |
| Risk controls | 1 | Unified-account venues need careful read of margin/liquidation for **exact** mode you use. |
| Malaysia accessibility | 1 | Terms excerpt in research **does not** list Malaysia as prohibited; **Bitget on SC Investor Alert List** — enforcement/regulatory mismatch risk. |

**Hard blockers:** none proven for MY **website access** in the starter desk pass; **regulatory comfort** is a personal/org gate.

---

### MEXC

| Category | Score | Notes |
|----------|-------|-------|
| API quality | 1 | Developer hub cited in research — confirm **current** base URLs and futures endpoints before build. |
| Liquidity | 1 | Very long tail of perps; **depth and churn** vary wildly by symbol. |
| Funding behavior | 1 | Research flags **funding history granularity** and **symbol churn** as unknowns without live pulls. |
| Costs | 1 | Verify maker/taker and any promo distortions; long-tail venues often have **tier opacity**. |
| Operational reliability | 1 | Treat like other high-listing retail books — log downtime and support outcomes. |
| Risk controls | 1 | Confirm isolated/cross, ADL/insurance language for **futures** specifically. |
| Malaysia accessibility | 1 | User Agreement excerpt: Malaysia **not** in prohibited list; **MEXC on SC Investor Alert List**. |

**Hard blockers:** none documented for MY in starter pass beyond alert-list **comfort** flag.

---

### HTX (Huobi)

| Category | Score | Notes |
|----------|-------|-------|
| API quality | 1 | API portal cited in research; **branding/domain changes** increase integration risk — pin official endpoints. |
| Liquidity | 1 | Historically serious derivatives stack; **per-symbol** depth still required. |
| Funding behavior | 1 | Verify **exact** perp product names and funding docs in live UI for your contract type (**?** until pulled). |
| Costs | 1 | Fee and tier docs must be re-fetched for your account type. |
| Operational reliability | 1 | Same as other globals — evidence-based status review. |
| Risk controls | 1 | Read margin/liquidation for the **specific** derivatives product. |
| Malaysia accessibility | 1 | Community restrictions post cited: Malaysia **not** named; **HTX/Huobi on SC Investor Alert List**. |

**Hard blockers:** **operational/documentation drift** — treat “can’t find stable official doc URL” as a **soft** project blocker until verified.

---

### BingX

| Category | Score | Notes |
|----------|-------|-------|
| API quality | 1 | API docs linked in research — validate futures/perp coverage matches your symbols. |
| Liquidity | 1 | Retail/social flow mix; **non-majors** need depth measurement. |
| Funding behavior | 1 | Confirm funding cadence/caps in official futures docs per contract. |
| Costs | 1 | Fee clarity OK at headline level; **all-in** needs your tier. |
| Operational reliability | 1 | Standard CEX operational discipline. |
| Risk controls | 1 | Customer Agreement + margin docs — confirm ADL/liquidation paths. |
| Malaysia accessibility | 1 | Research warns: **exact** restricted country names live on BingX **Disclaimer** page — **verify Malaysia there** before relying on access. |

**Hard blockers:** **if** Disclaimer lists Malaysia → **MY geo / ToS block** (verify; not confirmed in repo text).

---

### Kraken

| Category | Score | Notes |
|----------|-------|-------|
| API quality | 2 | Strong API culture; futures/perps documented ([support/licensing pages](https://support.kraken.com/) — verify live). |
| Liquidity | 2 | Deep on majors; better than most mid-tier for **BTC/ETH**-class books. |
| Funding behavior | 2 | Documentation and market structure generally transparent for listed perps — still **read rulebook per contract**. |
| Costs | 2 | Fee schedules tend to be clearly published; recompute for **your** tier. |
| Operational reliability | 2 | Mature status/comms relative to long-tail venues. |
| Risk controls | 2 | Liquidation and multi-collateral docs cited in research — read for **your** margin mode. |
| Malaysia accessibility | 1 | Licensing/geo page excerpt: Malaysia **not** in named prohibited list; **Kraken on SC Investor Alert List** — same offshore tension as other globals. |

**Hard blockers:** **strategy fit**: often **not** “mid-tier” for BTC/ETH crowding; not a legal MY block in cited excerpts.

---

### KuCoin

| Category | Score | Notes |
|----------|-------|-------|
| API quality | 2 | Mature REST/WS patterns ([API docs](https://www.kucoin.com/docs-new)); good for instrumented trials. |
| Liquidity | 2 | Broad futures book; majors generally workable — tails still need checks. |
| Funding behavior | 1 | Research warns: don’t confuse **margin borrow** costs with **perp funding** — explicit modeling required. |
| Costs | 1 | VIP/tier assumptions must be pinned; promos move. |
| Operational reliability | 1 | Typical global CEX ops — log your own incidents. |
| Risk controls | 1 | Document isolated/cross and liquidation for futures account type you use. |
| Malaysia accessibility | 0 | **KuCoin on SC Investor Alert List**; research marks **MY resident onboarding** as **unknown** without verified Terms — **cannot score “accessible” honestly**. |

**Hard blockers:** **K1 unknown / alert-list** combination — treat as **stop or heavy caution** until you personally confirm access **and** accept regulatory risk.

---

### Deribit

| Category | Score | Notes |
|----------|-------|-------|
| API quality | 2 | Reference-grade JSON-RPC/WebSocket docs ([docs.deribit.com](https://docs.deribit.com/)). |
| Liquidity | 2 | Excellent on **crypto options/perp** core suite; long-tail alts may be thin or absent. |
| Funding behavior | 2 | Strong transparency culture; verify contract-specific funding rules still before trades. |
| Costs | 2 | Fee schedule clear for product classes; confirm **your** fee tier. |
| Operational reliability | 2 | Generally strong track record among derivatives natives — still monitor incidents. |
| Risk controls | 2 | Insurance fund / ADL documentation is a known strength — re-read for instrument type. |
| Malaysia accessibility | 2 | Restricted jurisdictions PDF (cited in research): **Malaysia not enumerated**; offshore venue caveat still applies. |

**Hard blockers:** none identified for MY in cited restricted list — **not** legal clearance to trade.

---

### Hyperliquid

| Category | Score | Notes |
|----------|-------|-------|
| API quality | 2 | On-chain **Info** API documented ([Gitbook](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/info-endpoint)); different ops model than CEX keys. |
| Liquidity | 1 | Growing book; **capacity by symbol** must be measured; bridge latency affects execution. |
| Funding behavior | 1 | On-chain funding mechanics — compare **like-for-like** only vs other perps. |
| Costs | 1 | Gas, builder fees, and routing — model **all-in** differently from CEX fee tables. |
| Operational reliability | 1 | L1/bridge dependencies — new stack, fewer traditional “exchange status page” patterns. |
| Risk controls | 1 | Smart-contract / wallet / key risk dominates — map liquidations and deleveraging in docs. |
| Malaysia accessibility | 1 | No Malaysia-specific restriction found in cited API docs; **regulatory classification in Malaysia** treated as **unknown** in research. |

**Hard blockers:** none from geo list in cited docs — **operational complexity** may be a practical blocker for beginners.

---

### Gate.io

| Category | Score | Notes |
|----------|-------|-------|
| API quality | 2 | Broad developer docs ([API v4](https://www.gate.io/docs/developers/apiv4/en/)) suitable for funding pulls + execution trials. |
| Liquidity | 2 | Deep perp catalog; strong for many symbols — still measure your watchlist. |
| Funding behavior | 2 | Funding sections generally discoverable for USDT-margined perps — confirm per contract. |
| Costs | 2 | Fee schedules published; VIP assumptions still required. |
| Operational reliability | 2 | Major global exchange operational surface — log your own uptime experience. |
| Risk controls | 2 | Mature futures risk pages — read for your margin mode. |
| Malaysia accessibility | 0 | **Malaysia on Gate restricted locations** (per research citation) — **hard geo block for MY residents**. |

**Hard blockers:** **Malaysia restricted** — **do not use** as a candidate if you operate from MY, regardless of other scores.

---

### dYdX (v4 chain)

| Category | Score | Notes |
|----------|-------|-------|
| API quality | 2 | Chain-native indexer/API patterns ([dYdX docs](https://docs.dydx.exchange/)) — different integration than CEX. |
| Liquidity | 1 | Liquidity varies by market; measure **your** symbols; cross-venue hedge is harder. |
| Funding behavior | 1 | Funding **mechanics differ** from CEX USDT perps — only compare **like-for-like** edges. |
| Costs | 1 | Include gas, order-type, and fee parameters for v4 — rebuild cost model vs CEX. |
| Operational reliability | 1 | Validator/indexer stack dependencies — monitor chain health and upgrades. |
| Risk controls | 1 | On-chain liquidation and position management — read latest protocol params. |
| Malaysia accessibility | 1 | Wallet-based access; **local regulatory** treatment still user-specific — not resolved in repo research. |

**Hard blockers:** none cited for MY — **cross-stack hedge complexity** is the main practical gate.

---

## Optional: legacy ten-criterion mapping

An earlier draft of this file used **ten** criteria (funding transparency, fee clarity, … crowding). The **seven** category headers above are what **JTI-218** asked for. If you need comparability with older notes, map roughly as:

| New (7) | Legacy (10) overlap |
|---------|---------------------|
| API quality | #5 API reliability & limits |
| Liquidity | #3 Liquidity / depth |
| Funding behavior | #1 Funding transparency + #4 Contract / index alignment |
| Costs | #2 Fee clarity |
| Operational reliability | #7 Operational track record + #8 Withdraw / treasury path (partial) |
| Risk controls | #6 Margin & risk engine + #9 Insurance / ADL |
| Malaysia accessibility | Jurisdiction / access lens (was implicit) |

---

*Scores are subjective without live measurement; the scorecard’s job is to force **explicit** tradeoffs and unknowns. Template path: `docs/templates/exchange-suitability-scorecard.md`.*
