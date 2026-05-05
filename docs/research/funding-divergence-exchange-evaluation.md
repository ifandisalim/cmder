# Funding divergence — exchange evaluation (decision-ready shortlist)

This note turns desk research in [`exchange-research-outputs.md`](funding-divergence/exchange-research-outputs.md) and the project spec [`funding-divergence-mid-tier-exchange-research.md`](../specs/funding-divergence-mid-tier-exchange-research.md) into a **specific, evidence-backed, actionable** choice set for a **first validation** of a funding-divergence workflow (measurement + execution discipline), not a production mandate.

**Evidence bar (from spec):** claims below tie to **official docs / URLs already cited in the research outputs** (access date on that file: **2026-05-05**). Re-verify URLs, terms, and APIs before any capital or integration work.

**Precondition:** You must pass the scorecard **knockouts** in [`exchange-suitability-scorecard.md`](funding-divergence/exchange-suitability-scorecard.md) for **your** jurisdiction and product type (legal access, documented API, verifiable funding formula). If a venue is unavailable or unlawful for you, **drop it**—do not optimize around the name.

---

## Executive summary

| Decision | Choice |
|----------|--------|
| **Top 3 to score deeply** | **Gate.io (Gate)**, **Bitget**, **KuCoin** |
| **First exchange to test** | **Gate.io (Gate)** — best fit for a repeatable **funding history + fee + API** measurement loop on a **broad perp catalog** while staying off the single most “default” global retail perp venue for many bots |
| **Success in week one** | Documented funding pulls, fee assumptions, and API/error logs for a **small watchlist**—not headline PnL |

---

## Top 3 exchanges (pros, cons, key risks)

The three below match the **shortlist** in [`exchange-research-outputs.md`](funding-divergence/exchange-research-outputs.md): they balance **API and documentation depth**, **market breadth**, and **distance from the most crowded default** global perp attention for many symbols.

### 1. Gate.io (Gate)

**Why it ranks first for this strategy lens**

- **API / docs surface:** Futures/perp sections and developer docs are called out in research as a practical base for **repeatable funding pulls** and execution trials ([Gate API docs](https://www.gate.io/docs/developers/apiv4/en/) — verify live).
- **Catalog breadth:** Deep symbol lists support building a **small, stable watchlist** without immediately hitting “only on one niche venue” gaps (per research rationale).

**Pros**

- Strong fit for **validation mechanics**: historical funding access, fee tables, and integration paths are the bottleneck for learning—not guessing funding numbers from screenshots.
- Useful as the **first leg** when you later pair against another mid-tier or major book for **divergence** comparisons.

**Cons**

- **Jurisdiction:** Gate is listed among **restricted regions including Malaysia** on Gate’s own help content ([Restricted Locations](https://www.gate.io/help/guide/faq/40959/restricted-locations), cited in research). If you operate from a blocked region, **Gate is not a candidate** regardless of API quality.
- **“Mid-tier” is strategy-relative:** On some symbols, liquidity and attention may still resemble a major book; **your** size and symbol matter more than the label.

**Key risks**

| Risk | What it means |
|------|----------------|
| **Access / compliance** | Terms and geo lists change; offshore derivatives access is a **user-specific** decision—not covered here. |
| **Index / spec mismatch vs hedge leg** | If the second venue uses a different index or funding cadence, apparent “divergence” can be **artifact**, not edge (scorecard § contract alignment). |
| **Operational** | Withdrawals, maintenance windows, and API limits can break a hedge—log incidents during trial (scorecard § API reliability, treasury path). |

---

### 2. Bitget

**Why it’s on the shortlist**

- Research positions Bitget as **trial-friendly for integrators**: API documentation and product packaging are cited as workable for structured validation ([Bitget API intro](https://www.bitget.com/api-doc/common/intro)).
- Suggested in research as a strong **second comparison leg** after a Gate baseline (not necessarily the first integration).

**Pros**

- Good candidate when you need a **second venue** with clear API entry points for **side-by-side** funding and fee accounting.
- Fits the “not only the single largest default book” lens while still offering a broad perp stack.

**Cons**

- **Regulatory signaling:** Research notes **Bitget** appears on Malaysia’s SC **Investor Alert List** (offshore venue vs local registration framing). That is **not** legal advice; it is a flag to align platform choice with **your** compliance comfort.
- **Regional product variance:** Research flags **regional product availability** as an unknown without account verification.

**Key risks**

| Risk | What it means |
|------|----------------|
| **Campaign-driven fees / promos** | Headline attractiveness can change; anchor decisions to **documented** fee tier + logs. |
| **Liquidity on tail symbols** | Long-tail perps may look good on funding screens but fail on **depth** at your size. |
| **Counterparty / policy** | Same class of CEX tail risks as other globals—incident history and withdrawal behavior matter for hedges. |

---

### 3. KuCoin

**Why it’s on the shortlist**

- **Mature API culture** and broad futures coverage ([KuCoin API docs](https://www.kucoin.com/docs-new) — verify current portal).
- Research recommends KuCoin as a **cross-check venue** when testing whether observed divergence is **index- or spec-driven** vs a durable gap.

**Pros**

- Strong for **diagnostics**: comparing Gate ↔ KuCoin (or KuCoin ↔ another leg) helps separate **true** cross-venue funding differences from **contract-definition** noise.
- Fits teams that already think in **API-first** validation (rate limits, historical pulls).

**Cons**

- Research notes **KuCoin** on Malaysia’s SC **Investor Alert List** and marks **onboarding/KYC for Malaysia residents** as **unknown** without a verified Terms pass—**do not assume** access from docs alone.
- **Ambiguity across products:** Research warns to distinguish **futures funding** vs **margin borrow** funding where relevant—easy to mix costs.

**Key risks**

| Risk | What it means |
|------|----------------|
| **Product confusion** | Mis-modeling borrow vs perp funding breaks **all-in** edge math. |
| **Symbol churn / listing noise** | Long-tail venues may list/delist perps; your watchlist needs **governance**. |
| **Access uncertainty** | Until KYC/geo is confirmed, integration effort may be wasted—confirm **before** deep build. |

---

## Recommended first exchange to test

### **Gate.io (Gate)** — with explicit geo check

**Recommendation:** Use **Gate** as the **first** venue to stand up the **measurement and logging loop** (funding history, fee tier assumptions, API reliability, and execution errors) for a **small symbol watchlist**, **if and only if** you clear **legal/geo access** for your jurisdiction.

**Why Gate first (evidence-backed in repo research)**

1. **Workflow fit:** The shortlist rationale emphasizes Gate’s **documentation + breadth** as the fastest path to a **repeatable** process ([`exchange-research-outputs.md`](funding-divergence/exchange-research-outputs.md) — Shortlist table).
2. **Knockout alignment:** The scorecard prioritizes **funding transparency**, **fee clarity**, and **API reliability**; Gate is explicitly positioned as the primary deep-scoring target before rotating Bitget/KuCoin for comparison.
3. **Hedge of narrative risk:** The doc already warns **not** to treat any name as the permanent “winner”—**campaigns** move. Gate is recommended as **first instrumented sandbox**, not permanent home.

**If Gate is geo-blocked for you:** Treat **Bitget** or **KuCoin** as the first venue **only after** knockouts pass—Bitget for integrator-style trials, KuCoin for **cross-index** diagnostics with another leg. Re-run the scorecard; totals are **tie-breakers** after knockouts.

---

## Practical next 7-day action plan

Goals: **evidence quality and repeatability first**—per spec and handoff checklist—not profit claims.

| Day | Actions | Done when |
|-----|---------|-----------|
| **1** | Read [`beginner-guide.md`](funding-divergence/beginner-guide.md) and scorecard knockouts. Confirm you can access **official** funding docs for the **exact** contract type (USDT-margined perp vs others). | Knockouts recorded **pass/fail** with links |
| **2** | Pick **10–20** liquid symbols you would realistically hedge (not the whole catalog). Note **index composition** skims for your primary hedge leg. | Written watchlist + “same underlying?” notes |
| **3** | Register API keys (minimum scope); pull **funding history** samples per venue docs; store **one redacted sample response** (per handoff checklist). | Timestamped pull + saved JSON/text snippet |
| **4** | Build a fee assumption row: maker/taker, **your** tier or conservative default; include withdrawal/transfer thoughts for later hedge funding. | Fee table link + all-in worksheet row |
| **5** | Dry-run **read-only** Websocket/REST: measure **rate-limit behavior** and error strings; log gaps. | Short log of errors/throttles |
| **6** | **Paper or zero-risk path:** if the venue supports testnets/simulation use it; otherwise **no live hedge**—only shadow logs of **would-be** fills + funding accrual **from data**. | Log file showing scheduled funding snapshots |
| **7** | Retrospective: list **unknowns** explicitly (VIP tier, sub-accounts, insurance fund rules). Decide whether **Bitget** or **KuCoin** is the **second** venue for **divergence** comparison in week two. | Unknowns list + go/no-go for paired venue |

**Optional parallel (if geo blocks Gate):** Spend days 3–5 repeating API/funding pulls on **Bitget** or **KuCoin** only after day 1 knockouts confirm access.

---

## Limitations (read once)

- **No profitability claim:** This evaluation follows the spec’s **out of scope** rules—no backtests or live PnL assertions.
- **Not legal/tax advice:** Jurisdiction lists (e.g., SC Investor Alert List, Gate restricted regions) are **research citations**, not advice on whether you may use a platform.
- **Stale data:** Funding rules, fees, and geo policies change; the **access date** on [`exchange-research-outputs.md`](funding-divergence/exchange-research-outputs.md) is a floor—refresh before deployment.

---

## Source map

| Topic | Primary repo artifact |
|-------|------------------------|
| Definitions, evidence bar | [`../specs/funding-divergence-mid-tier-exchange-research.md`](../specs/funding-divergence-mid-tier-exchange-research.md) |
| Longlist, shortlist, first pick | [`funding-divergence/exchange-research-outputs.md`](funding-divergence/exchange-research-outputs.md) |
| Knockouts + scoring | [`funding-divergence/exchange-suitability-scorecard.md`](funding-divergence/exchange-suitability-scorecard.md) |

*Evaluation compiled for Linear **JTI-217**; aligns with desk research access date **2026-05-05** where cited.*
