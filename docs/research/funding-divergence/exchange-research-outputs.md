# Funding divergence — longlist, shortlist, and first validation pick

**Evidence bar:** each row should eventually link to official docs or reproducible data pulls (see spec). Rows below include **starter citations**; re-verify before any capital deployment.

**Access date for citations below:** 2026-05-05 (desk research pass for repo handoff).

---

## Malaysia-accessibility longlist (JTI-215)

This table is **Malaysia-specific**: it pairs **perpetual (or perpetual-style) products** with **what we could verify from official pages** about geographic access. It does **not** replace legal advice. Under Malaysian rules, spot crypto exchanges must generally register with the Securities Commission (SC) as recognised market operators (RMOs); many global derivatives venues are **not** on that register and may appear on the SC **Investor Alert List**—see [SC list of registered digital asset exchanges](https://www.sc.com.my/regulation/guidelines/recognizedmarkets/list-of-registered-digital-asset-exchanges) and [SC Investor Alert List](https://www.sc.com.my/investor-alert-list).

| # | Venue | Type | Perp / funding-related product (evidence) | Malaysia user accessibility (desk finding, 2026-05-05) | Primary sources |
|---|-------|------|-------------------------------------------|--------------------------------------------------------|-----------------|
| 1 | **Bitget** | CEX | USDT-margined futures / perps; API ([Bitget API intro](https://www.bitget.com/api-doc/common/intro)) | **Terms:** `Prohibited Countries` in the Terms of Use does **not** name Malaysia (list includes e.g. Singapore, US, Canada). **Regulatory:** “Bitget” appears on the SC Investor Alert List — offshore venue, not an SC-registered DAX. | [Bitget Terms of Use](https://www.bitget.com/support/articles/360014944032-terms-of-use) (Feb 2026); [SC Investor Alert List](https://www.sc.com.my/investor-alert-list) |
| 2 | **MEXC** | CEX | Perpetual futures among “Futures Trading” services ([User Agreement](https://www.mexc.com/en-US/terms) §13(j)) | **Terms:** `Prohibited Jurisdictions` include US, UK, Singapore, etc., but **not** Malaysia. **Regulatory:** “MEXC Global” appears on the SC Investor Alert List. | [MEXC User Agreement](https://www.mexc.com/en-US/terms) (May 2025); [SC Investor Alert List](https://www.sc.com.my/investor-alert-list) |
| 3 | **HTX (Huobi)** | CEX | Crypto derivatives stack (verify exact product names in live UI); group branding HTX | **Public restrictions list:** HTX OTC post lists restricted **countries/regions** for services; **Malaysia is not named** (list includes e.g. Singapore, UK, US). **Regulatory:** “Huobi Global/HTX” appears on the SC Investor Alert List. | [HTX — Restricted countries/regions](https://www.htx.com/en-in/feed/community/2770559/) (Nov 2024); [SC Investor Alert List](https://www.sc.com.my/investor-alert-list) |
| 4 | **BingX** | CEX | “Futures Trading” section in Customer Agreement | **Terms:** Users must not be in **Restricted Jurisdictions** per BingX **Disclaimer** (exact country list is on that Disclaimer page); explicit bar for **US and Canada** users in §2. **Regulatory:** “BingX” appears on the SC Investor Alert List — offshore venue, not an SC-registered DAX. | [BingX Customer Agreement](https://www.bingx.com/en/support/articles/360033286474) (Aug 2025); [SC Investor Alert List](https://www.sc.com.my/investor-alert-list) |
| 5 | **Kraken** | CEX | **Crypto perpetual futures** on Kraken Pro ([product page](https://www.kraken.com/features/futures/perpetual)); multi-collateral perps ([support](https://support.kraken.com/articles/4844429542676-trading-multi-collateral-derivatives)) | **Geography:** Kraken’s licensing page states Malaysia is **not** among named “Prohibited Regions” (list ends with Syria in the excerpt we used). **Regulatory:** “Global Kraken” appears on the SC Investor Alert List — same “offshore vs local registration” tension as other majors. | [Where is Kraken licensed or regulated?](https://support.kraken.com/articles/360001368823-Where-can-I-use-Kraken) (May 2026); [SC Investor Alert List](https://www.sc.com.my/investor-alert-list) |
| 6 | **KuCoin** | CEX | Futures / perps via KuCoin Futures ([announcement hub example](https://www.kucoin.com/announcement)) | **Regulatory:** KuCoin (`kucoin.com`) is on the SC Investor Alert List as operating a DAX without SC registration. **Platform geo:** not verified from a fetched Terms PDF in this pass — treat onboarding/KYC for MY residents as **unknown until tested or confirmed with KuCoin**. | [SC Investor Alert List](https://www.sc.com.my/investor-alert-list); [KuCoin site](https://www.kucoin.com/) |
| 7 | **Deribit** | CEX (crypto derivatives) | Inverse perpetual-style products among futures; see [API docs](https://docs.deribit.com/) | **Restricted jurisdictions PDF** (Aug 2025) lists Canada, US, Japan, etc. — **Malaysia is not** in the enumerated list. **Regulatory:** venue is offshore; users in Malaysia should still verify local law and tax. | [Restricted Jurisdictions (PDF)](https://statics.deribit.com/files/StatementRestrictedCountriesDeribit.pdf); [Deribit documentation](https://docs.deribit.com/) |
| 8 | **Hyperliquid** | DEX / on-chain | Perpetuals via L1 + documented **perp** API ([Info endpoint](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/info-endpoint)) | **Geo:** protocol access is wallet-based; **no Malaysia-specific restriction** found in the cited API docs. **Regulatory / banking:** treat as **unknown** for Malaysia licensing — compare to SC messaging on unregistered venues. | [Hyperliquid docs — Info endpoint](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/info-endpoint); [SC digital assets overview](https://www.sc.com.my/digital-assets) |

### Venues with explicit Malaysia **blocks** on major global books (for divergence pair planning)

These are **negative screens** if you need accounts on large offshore CEXs:

| Venue | Malaysia signal | Source |
|-------|-----------------|--------|
| **Gate.io** | **Restricted regions** include Malaysia | [Gate — Restricted Locations](https://www.gate.io/help/guide/faq/40959/restricted-locations) (Aug 2025) |
| **OKX** | **Restricted Locations** include Malaysia | [OKX Risk & Compliance Disclosure](https://www.okx.com/help/risk-compliance-disclosure) (updated Mar 2026) |
| **Bybit** | SC directed platform disable / cease marketing (enforcement Dec 2024) | [SC media release — Bybit](https://www.sc.com.my/resources/media/media-release/sc-takes-enforcement-action-against-bybit-for-illegally-operating-dax-in-malaysia) |
| **Binance** | SC enforcement Jul 2021 + Binance announcement on MYR / Malaysia offerings | [SC media release — Binance](https://www.sc.com.my/resources/media/media-release/sc-takes-enforcement-actions-on-binance-for-illegally-operating-in-malaysia); [Binance announcement — Restricting product offerings in Malaysia](https://www.binance.com/en/support/announcement/restricting-of-product-offerings-in-malaysia-ab37eace9146494d990293d60423a34e) |

### Obvious blockers / caveats (Malaysia lens)

1. **Regulatory mismatch:** SC registration lists ([link](https://www.sc.com.my/regulation/guidelines/recognizedmarkets/list-of-registered-digital-asset-exchanges)) cover **Malaysia-licensed** spot DAX operators — **not** most offshore perpetual venues. Several global brands appear on the **[Investor Alert List](https://www.sc.com.my/investor-alert-list)** even when their **Terms** omit Malaysia from `Prohibited` lists.
2. **Two different questions:** (a) Can you load the website / pass KYC? (b) Are you comfortable with enforcement risk? This longlist cites **(a)** where possible; **(b)** is outside repository scope.
3. **Unknowns:** BingX **Restricted Jurisdictions** country names are on BingX’s **Disclaimer** page linked from the Customer Agreement — verify Malaysia there before relying on access. KuCoin **resident restrictions** were not confirmed from a single fetched Terms page in this pass.

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
