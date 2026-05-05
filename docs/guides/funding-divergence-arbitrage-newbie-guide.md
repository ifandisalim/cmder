# Funding divergence arbitrage — a beginner’s guide (simple English)

This page explains **funding divergence** trading in everyday language. **Perpetual swaps** (“perps”) are crypto futures that never expire; they stay near the spot price partly through **funding** — money that longs and shorts pay each other on a schedule. **Funding divergence** means **two exchanges charge noticeably different funding** for essentially the **same** exposure (same coin, similar contract rules). Some traders try to **earn that gap** after all costs — that idea is often called **funding arbitrage** or **funding divergence** strategy.

This is **not** financial, legal, or tax advice. Rules, fees, and risks change; you must verify everything with each venue’s official docs and your own situation.

---

## What is the strategy, in one sentence?

You try to **collect a steady edge from funding** by holding **offsetting positions** on two places (for example long on one venue and short on another) so you are **roughly neutral** on whether price goes up or down, while **net funding** (minus fees and friction) works in your favor **often enough** to be worth it.

Think of it less like “betting on Bitcoin” and more like “running a small, hedged carry trade between two markets that price **holding** the contract differently.”

---

## How do people actually make money?

**Funding is cash flow, not magic.** On many venues, when funding is **positive**, longs pay shorts; when it is **negative**, the direction flips (exact rules are venue-specific — always read the rulebook for **your** contract).

The **play** is roughly:

1. You find two venues where funding **does not match** for the same idea (e.g. one pays longs more than the other, or one charges longs much more).
2. You put on **hedged** exposure: one side receives what the other side pays, so **spot direction** matters less than **who pays whom and how much**.
3. You **subtract real costs**: trading fees, any borrow or margin costs, transfers, slippage (price moving against you when you trade), and **time** (money stuck while moving collateral).

**Profit** (when it happens) is mostly: **net funding you collect**, minus **those costs**, over the days or weeks you hold the hedge — **not** a guarantee every hour.

If the funding gap is **tiny** or **disappears quickly**, or fees eat it, there may be **no** meaningful edge left.

---

## Why do people talk about “mid-tier” or less crowded exchanges?

The **largest** global books are watched by many bots and professionals; simple gaps can vanish fast. **Smaller or mid-sized** venues can still be serious, but **liquidity**, **fees**, **promotions**, and **who trades there** may differ.

**Plain English:** you are not automatically safer on a smaller venue. You are trading in a **different crowd** and **different rules**. You still need to study **liquidity**, **reliability**, and **how you get money in and out**.

---

## Pros (why anyone bothers)

- **Direction-neutral-ish:** you are not mainly betting that price will moon; you are trying to harvest **structural differences** in **funding** and **costs**.
- **Repeatable workflow:** you can compare venues with a checklist (fees, funding formula, caps, intervals, API, withdrawals).
- **Transparent inputs (if you do the work):** funding schedules and fee tables are often published; you can **paper-trade** or use **tiny size** to learn before scaling.

---

## Cons and harsh realities (read these carefully)

- **Edges move:** funding and promotions change; yesterday’s picture may be wrong today.
- **Costs are sneaky:** maker/taker fees, VIP tiers, withdrawals, and **bad fills** can erase a “pretty” funding number.
- **Not fully risk-free:** hedges can **break** if contracts are not really the same (different index, different funding formula, different leverage or margin rules).
- **Operational drag:** APIs throttle, exchanges pause withdrawals, networks congest — **you** still carry those risks.
- **Capacity:** if you are too big for the book, you **worsen** your own prices and funding.

---

## Key risks (what can hurt you)

| Risk | In simple words |
|------|------------------|
| **Imperfect hedge** | You thought you were neutral, but the two products diverge (different index, funding math, or liquidation rules). Price moves can still hurt. |
| **Fee and funding math** | You estimated profit using headline funding but forgot fees, borrow, or tier rules. |
| **Liquidity** | You cannot enter or exit at a fair price; **slippage** eats the edge. |
| **Credit / counterparty** | Exchange issues, pauses, or policy changes — your capital and positions are exposed to **that venue**. |
| **Operational** | Bugs, wrong ticket size, API outage during a move — **human and system** errors are real. |
| **Regulatory / access** | Products may be unavailable in your region; access rules change. |

When in doubt, **assume** the edge is smaller than it looks and **size down**.

---

## Realistic expectations (what “success” might look like)

- **No guaranteed profit.** This is **not** a savings account. Funding prints **fluctuate**; costs **bite**; gaps **close**.
- **Small, steady edges** are more plausible than huge risk-free wins — and **only after** honest costing.
- **Learning curve:** understanding **your** venues’ rulebooks, funding intervals, and fee tiers matters more than chasing the highest number on a leaderboard.
- **Validation first:** many serious people **paper-trade** or use **tiny size** until logging and execution feel boring and reliable.

**You are doing well as a beginner** if you can say in your own words: *what* perp funding is, *why* two venues might differ, *how* hedging is supposed to work, *what* costs must be subtracted, and *what* could break — **before** putting meaningful capital at risk.

---

## Where to go next in this repo

- Research vocabulary and workflow: [`../research/funding-divergence/beginner-guide.md`](../research/funding-divergence/beginner-guide.md)
- Deeper spec (definitions and evidence bar): [`../specs/funding-divergence-mid-tier-exchange-research.md`](../specs/funding-divergence-mid-tier-exchange-research.md)
- Scorecard and venue notes: [`../research/funding-divergence/`](../research/funding-divergence/)

---

*This guide aligns with the research spec; numbers and venue rankings are not copied here because they go stale — verify live data and official documentation before trading.*
