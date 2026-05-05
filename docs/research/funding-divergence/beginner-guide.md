# Beginner guide: funding divergence research (plain English)

This guide explains **what you are looking for** when the spec talks about “funding divergence” on **mid-tier** perpetual exchanges, and **how to think about risk** before you write code or size positions.

## What problem are people trying to solve?

Many crypto **perpetual** contracts use **funding payments** so the contract price stays near the **index** (a reference price). Over time, those payments are **real cash flows** for holders of the contract.

Sometimes **two different exchanges** charge **meaningfully different** funding for exposure to the **same coin** (and similar contract design). If the difference is **stable enough** and **large enough** after costs, a trader might try to **capture that gap** by holding **offsetting** positions across venues—classic **pairs / hedged** thinking.

That **gap in funding** (plus fees, slippage, and operational drag) is what we loosely call **funding divergence** in this project.

## Why mention “mid-tier” or “less crowded”?

On the **most scanned** venues, simple edges can disappear quickly because many participants watch the same screen. **Smaller or mid-sized** books can still be serious venues—but the **mix of participants**, **fee promos**, and **latency** can differ.

**Plain English:** you are not automatically safer on a mid-tier venue. You are **changing the competitive field** you must study. Liquidity, insurance funds, and operational risk still matter—a lot.

## What you are *not* doing (common beginner mistake)

You are usually **not** trying to predict whether Bitcoin goes up tomorrow.

You are trying to answer a **narrower** question:

> “If I run a **hedged** setup across two venues, do I expect **funding minus all costs** to favor my side **often enough** to survive bad stretches?”

If you cannot hedge cleanly (different index, different leverage rules, different margin asset), the “divergence” can be **illusory**.

## The basic checklist (conceptual)

1. **Same economic exposure**  
   Same underlying asset, **compatible** contract specs (how funding is computed, caps, intervals). If the formulas differ a lot, you are comparing **two different products**.

2. **All-in costs**  
   Trading fees, rebates, withdrawals, transfer time, and any **borrow** or **margin** costs. A pretty funding print means little if fees eat it.

3. **Capacity**  
   How much size can you put on before you move the market or worsen your average funding?

4. **Operational risk**  
   API limits, downtime, withdrawal pauses, and how you would **exit** under stress.

5. **Jurisdiction and access**  
   Some products are not available everywhere. This is a **hard** gate—not a nice-to-have.

## How to use the other documents

- **Scorecard**: a table of criteria and knockouts. Use it like a **flight checklist**, not a popularity contest.
- **Research outputs**: a **longlist** (cast a wide net), a **shortlist** (few serious candidates), and **one** venue flagged for **first validation** (small or paper trial—not “go live big”).

## Important limitations (read this twice)

- Numbers **change** (fees, promos, funding). Treat snapshots as **perishable**.
- This repo’s research pass is a **starting point**. You must **re-verify** anything material before risking money.
- Nothing here is **financial, legal, or tax advice**.

When in doubt, **shrink the trial**, **increase logging**, and **re-check** the venue’s official rulebook for the exact contract you trade.
