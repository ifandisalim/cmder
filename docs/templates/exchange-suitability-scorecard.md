# Exchange suitability scorecard — template (funding divergence / mid-tier lens)

Copy this structure for each venue. **Scores** use **0–2** per category:

- **0** = fails or unacceptable for our trial (or unknown in a way that blocks planning)
- **1** = usable with friction, caveats, or material unknowns
- **2** = strong for this criterion

**Total** = sum of the **seven** category scores (**maximum 14**). Use totals only **after** hard blockers and knockouts are resolved.

---

## Hard blockers (flag explicitly)

Record any **hard blocker** for *your* operating context (examples: explicit geo-restriction, no API path to funding history, cannot verify funding formula in official docs, legal/compliance bar you will not cross). A flagged hard blocker means **do not shortlist** for trial, regardless of headline scores.

---

## Knockout rules (any “no” → do not shortlist for trial)

| Knockout | Question |
|----------|----------|
| **K1** | Can you **legally access** perps from your operating jurisdiction (verified, not assumed)? |
| **K2** | Is there a **documented public API** sufficient to fetch funding and trade (even if you start manual)? |
| **K3** | Can you verify **how funding is calculated** in the official docs for the exact contract type? |

---

## Categories (seven × 0–2)

| # | Category | What “good” looks like | Score notes |
|---|----------|------------------------|-------------|
| 1 | **API quality** | Stable REST/WebSocket; clear auth and rate limits; funding and market data endpoints documented with examples. | Prefer a dry-run log of errors/throttles. |
| 2 | **Liquidity** | Enough top-of-book depth for **your** trial size on **your** watchlist symbols; avoids chronic partial fills on the hedge. | Use your size, not exchange marketing. |
| 3 | **Funding behavior** | Official formula, caps, cadence; historical funding retrievable (API or export); comparable index story vs your other leg. | Misaligned index ⇒ fake divergence. |
| 4 | **Costs** | Published maker/taker; VIP tiers or rebates documented; easy to build **all-in** with *your* tier. | Include transfer/withdraw assumptions if they matter. |
| 5 | **Operational reliability** | Credible uptime/status comms; predictable maintenance; support paths if API breaks mid-hedge. | Subjective—tie to evidence you trust. |
| 6 | **Risk controls** | Liquidation, margin mode (isolated/cross), ADL/socialized loss rules documented for the exact product. | Surprises here blow up hedges. |
| 7 | **Malaysia accessibility** | For Malaysia-based researchers: terms/geo lists, SC registration vs Investor Alert List signals, and **your** comfort with enforcement/onboarding risk. | Not legal advice; cite primary sources. |

---

## One row per venue (spreadsheet-friendly)

| Venue | API | Liq | Funding | Costs | Ops | Risk | MY | Total | K1 | K2 | K3 | Hard blockers (short text) |

---

## Per-venue detail (optional paste-under)

```text
Venue:
API quality (0–2):    Notes:
Liquidity (0–2):     Notes:
Funding (0–2):       Notes:
Costs (0–2):         Notes:
Operational (0–2): Notes:
Risk controls (0–2): Notes:
Malaysia access (0–2): Notes:
Evidence links + access date:
```

---

*Template aligned with JTI-218; evidence bar matches the parent spec in `docs/specs/funding-divergence-mid-tier-exchange-research.md`.*
