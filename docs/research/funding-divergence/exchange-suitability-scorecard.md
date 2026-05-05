# Exchange suitability scorecard — funding divergence (mid-tier lens)

Use one row per venue. **Score** each criterion **0–2** where:

- **0** = fails / unacceptable for our trial  
- **1** = usable with friction or unknowns  
- **2** = strong for this criterion  

**Total** is out of **20** (sum of ten criteria). Treat **totals as a tie-breaker only** after knockouts.

## Knockout rules (any “no” → do not shortlist for trial)

| Knockout | Question |
|----------|----------|
| K1 | Can you **legally access** perps from your operating jurisdiction (verified, not assumed)? |
| K2 | Is there a **documented public API** sufficient to fetch funding and trade (even if you start manual)? |
| K3 | Can you verify **how funding is calculated** in the official docs for the exact contract type? |

If any knockout fails, **stop**—do not proceed to compare headline funding.

## Criteria (10 × 0–2)

| # | Criterion | What “good” looks like | Notes |
|---|-----------|-------------------------|-------|
| 1 | **Funding transparency** | Clear formula, caps, payment cadence; easy historical access (API or export). | Prefer primary docs over third-party aggregators. |
| 2 | **Fee clarity** | Published maker/taker; VIP tiers documented; funding-related rebates (if any) explicit. | Recompute **all-in** with *your* tier. |
| 3 | **Liquidity / depth** | Enough top-of-book depth for your trial size on the symbols you care about. | Use your own size, not “exchange average.” |
| 4 | **Contract / index alignment** | Index constituents and weights understandable; not wildly different from your hedge leg. | Misaligned index = fake divergence. |
| 5 | **API reliability & limits** | Sensible rate limits; stable endpoints; websocket where needed. | Capture error behavior during a dry run. |
| 6 | **Margin & risk engine** | Clear liquidation rules; isolated vs cross documented; portfolio margin (if any) explained. | Surprises here blow up hedges. |
| 7 | **Operational track record** | Reasonable uptime history; transparent status page; credible incident comms. | Subjective—use evidence you trust. |
| 8 | **Withdraw / treasury path** | Predictable on/off ramps for **your** workflow (may be none—then plan transfer risk). | Stablecoins vs bank vs internal transfer. |
| 9 | **Insurance / ADL / clawback policy** | Documented socialized loss / auto-deleveraging rules if applicable. | Know tail scenarios. |
| 10 | **“Crowding” / edge hygiene** | For **your** niche symbols, evidence that the book is not the single most scanned global venue *for that niche*. | Qualitative; cite what you observed. |

## Optional weights (advanced)

If you already know your bottleneck (e.g., API-first), double-weight criteria **1, 2, 5** in a separate column. Keep the default unweighted total for comparability across researchers.

## Template row (copy into a spreadsheet)

| Venue | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | Total | Knockouts OK? | Evidence links |

---

*Scoring is subjective without live measurement; the scorecard’s job is to force **explicit** tradeoffs and unknowns.*
