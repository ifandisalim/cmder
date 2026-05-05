# Funding divergence — longlist, shortlist, and first validation pick

**Evidence bar:** each row should eventually link to official docs or reproducible data pulls (see spec). Rows below include **starter citations**; re-verify before any capital deployment.

**Access date for citations below:** 2026-05-05 (desk research pass for repo handoff).

---

## Longlist (candidate perpetual venues — mid-tier / alternative books)

“Mid-tier” here means **not** treating the single largest global perp venue as the default only place to farm funding edges. Names appear because they commonly list broad perp catalogs and publish APIs; **none** is an endorsement.

| Venue | Why on the longlist | Starter evidence (verify) | Known unknowns without account |
|-------|---------------------|---------------------------|--------------------------------|
| **Gate** | Large perp catalog; widely used outside a single dominant venue; public API ecosystem. | [Gate API docs](https://www.gate.io/docs/developers/apiv4/en/), futures/perp sections. | Exact VIP fee for your volume; sub-account rules. |
| **MEXC** | Very long tail of listed perps; often discussed in retail funding threads. | [MEXC API / developer hub](https://www.mexc.com/mexc-api) (verify current URL). | Funding history granularity; symbol churn. |
| **Bitget** | Active perp product marketing; unified account features in docs over time. | [Bitget API documentation](https://www.bitget.com/api-doc/common/intro). | Regional product availability. |
| **KuCoin** | Established futures API; broad markets. | [KuCoin API docs](https://www.kucoin.com/docs-new). | Compare futures vs margin funding where relevant. |
| **BingX** | Perps + social/retail flow mix; API advertised. | [BingX API docs](https://bingx-api.github.io/docs/) (verify current). | Depth on non-major pairs. |
| **HTX (Huobi)** | Long-running derivatives stack; API docs. | [HTX API documentation](https://www.htx.com/en-us/opend/newApiPages) (verify current portal). | Branding/domain changes—double-check official domain. |
| **Deribit** | Extremely transparent derivatives culture; strong options/perp ecosystem (often **not** “mid-tier” attention for BTC/ETH). | [Deribit API](https://docs.deribit.com/). | May be **more** institutional; fees/liquidity differ by product. |
| **dYdX (v4 chain)** | Different stack (chain-based); funding mechanics differ—only compare like-for-like. | [dYdX documentation](https://docs.dydx.exchange/). | Cross-venue hedge complexity vs CEX perps. |
| **Hyperliquid** | On-chain perp book; growing attention; distinct infra. | [Hyperliquid docs](https://hyperliquid.gitbook.io/hyperliquid-docs). | Bridge / wallet ops vs CEX hedges. |

If a venue is **illegal or unavailable** for you, **remove it**—do not score it.

---

## Shortlist (recommended set to score deeply next)

These **three** balance **API/funding documentation depth**, **breadth of markets**, and **distance from the single most crowded default** for global perp attention—while still being realistic places to run a **first** structured validation.

| Rank | Venue | Rationale (summary) |
|------|-------|---------------------|
| 1 | **Gate** | Strong documentation surface area for futures/perps; deep symbol lists; practical for building repeatable funding pulls + execution trials. |
| 2 | **Bitget** | API docs and product packaging tend to be trial-friendly for integrators; good second leg for comparisons **after** Gate baseline. |
| 3 | **KuCoin** | Mature API culture; useful cross-check venue when validating whether observed divergence is **index / spec** driven. |

**Not dropped forever:** MEXC and BingX are sensible **phase-two** longlist targets if your symbol set is niche and Gate/KuCoin/Bitget lack the exact listing.

---

## Recommended **first** exchange for next-step validation

### Pick: **Gate.io** (Gate)

**Recommendation (one sentence):** Use **Gate** as the **first** venue to validate your funding-divergence workflow because its **perp + API documentation** and **market breadth** make it easier to build a **repeatable measurement loop** (funding history, fees, and execution) while still being off the single most “default” global perp venue for many retail bots.

**What “validation” should mean here (plain English):**

1. **Read** the official funding section for the **exact** contract type you will trade.  
2. **Pull** funding history via API (or export) for a small **watchlist** of symbols.  
3. **Paper or micro-size** a **hedged** trial if you already have a second leg in mind—or **single-venue** funding carry trial **only** if your risk model explicitly allows unhedged exposure (usually **not** the same strategy).  
4. **Log** fees, slippage, and API errors for two weeks of calendar time—not one lucky hour.

**Why not declare a winner forever:** funding and promos are **campaign-driven**. The workflow and scorecard matter more than the name on the tin.

---

## Handoff checklist for child issues

- [ ] Attach **fee tier** assumption used in scoring.  
- [ ] Attach **symbol list** (10–30 names max for v1).  
- [ ] Store **one** sample API response (redacted keys) proving funding history access.  
- [ ] Record **jurisdiction** decision explicitly.  
- [ ] Define **trial success** as measurement quality first (uptime, data completeness), not PnL.

---

*Desk research starter pack — re-verify all URLs and rules on the live exchange before trading.*
