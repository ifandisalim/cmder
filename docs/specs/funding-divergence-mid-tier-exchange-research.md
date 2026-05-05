# Funding divergence on mid-tier exchanges — research spec (source of truth)

This document defines **what** we are studying, **how** we evaluate venues, and **where** the evidence-backed outputs live. It is the single spec for parent issue **JTI-214** and any child issues that produce research artifacts.

## Purpose

Build a **beginner-friendly, repeatable workflow** for researching **funding-rate divergence** (a type of *funding arbitrage*): you look for situations where two venues imply different costs to hold the same (or very similar) perpetual position, then design execution and risk controls around that edge.

We focus on **mid-tier / less crowded** perpetual venues (not only the top-two global books) because competition, queue position, and fee structures can differ materially from the most scanned exchanges.

## Plain definitions

- **Perpetual swap (“perp”)**: A futures-like contract with no fixed expiry; price is tethered to spot mainly via **funding**.
- **Funding rate**: A periodic payment between longs and shorts. When funding is **positive**, longs typically pay shorts; when **negative**, the direction reverses (exact mechanics depend on the venue’s rulebook).
- **Funding divergence**: A **persistent or predictable gap** in implied funding cost between **two venues** for the same underlying exposure (same coin, similar index, similar contract economics), **after** fees, borrow, basis, and operational risk.
- **Mid-tier (for this project)**: Perpetual venues with meaningful liquidity and API access, but **materially lower** “default” attention from global HFT and crowded arb fleets than the single largest global perp book. The list is **not** a quality ranking of the exchange as a whole—only suitability **for this strategy lens**.

## Scope and non-goals

**In scope**

- Qualitative and desk-research workflow suitable for someone new to funding arb.
- A **scorecard** you can reuse for each candidate venue.
- A **longlist → shortlist** path with explicit evidence notes and “unknowns.”
- One **recommended first venue** for a **trial / validation** phase (paper or tiny size), not a production mandate.

**Out of scope**

- Guaranteed profitability, signal backtests, or live PnL claims.
- Legal, tax, or compliance advice (jurisdiction varies; readers must verify).

## Deliverables (file map)

| Deliverable | Path |
|-------------|------|
| Beginner guide (plain English) | [`../research/funding-divergence/beginner-guide.md`](../research/funding-divergence/beginner-guide.md) |
| Exchange suitability scorecard | [`../research/funding-divergence/exchange-suitability-scorecard.md`](../research/funding-divergence/exchange-suitability-scorecard.md) |
| Longlist, shortlist, first validation pick | [`../research/funding-divergence/exchange-research-outputs.md`](../research/funding-divergence/exchange-research-outputs.md) |

## Evidence standard (“done when” for research)

Each scoring row and each longlist entry should cite **at least one** of:

1. **Official** product or API documentation (URL + access date in the research doc footer).
2. **Observable** market data you can re-fetch (e.g., public funding history endpoint, or exchange UI with timestamps noted as a screenshot reference—not stored in this repo unless policy allows).
3. **Explicit “unknown”** if a field cannot be verified without an account or paid tier—**do not guess**.

Child issues should attach or link evidence in the tracker; this repo holds the **templates and initial pass** so the workflow is clear.

## Workflow (for researchers)

1. Read the beginner guide once for vocabulary alignment.
2. Copy the scorecard table; score each longlist venue independently; keep notes in the same row.
3. Apply **knockout rules** from the scorecard (API, jurisdiction, product availability) before comparing finer points.
4. Shortlist **three to five** venues with the smallest number of unknowns.
5. Pick **one** venue for trial planning based on: API quality, fee clarity, funding transparency, and your operational constraints.

## Child issues (Linear)

Track granular work under **JTI-214** as child issues, for example:

- “Verify API + funding history for shortlist A”
- “Document fee schedule and VIP assumptions”
- “Trial plan: paper trading checklist”

Update this spec only when definitions or the evidence bar change—not when rankings change week to week.

---

*Last updated: 2026-05-05 — initial repo commit for JTI-214 handoff.*
