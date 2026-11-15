# How recruiting operations moves headcount, revenue and cost

Most companies plan headcount in seats: "we'll be 80 people by Q3." Revenue plans assume those seats are producing. The gap between a seat being *approved* and a person being *productive in it* is where recruiting operations shows up on the P&L.

```mermaid
flowchart LR
    A[Seat approved] -->|time to fill| B[Offer accepted]
    B -->|offer to start| C[Day 1]
    C -->|ramp| D[Fully productive]
    style B fill:#fde68a,stroke:#b45309
    style C fill:#fde68a,stroke:#b45309
```

Sourcing and interviewing get most of the attention. This system works on the highlighted part: **offer to start, and the first days after**. It's the part leadership usually assumes is instant.

The [calculator](../index.html) runs these formulas on your numbers. **All defaults below are illustrative, not measured results.** Replace them with your own.

---

## 1. Productive days recovered

Every day a new hire's start slips, or they spend Day 1 waiting for a laptop, is a day of planned output that doesn't happen.

```
daily value per hire   = revenue per employee ÷ 260 working days × ramp factor
days recovered per hire = (start-date slip before − after) + (onboarding days lost before − after)
value recovered        = hires per year × days recovered per hire × daily value per hire
```

- **Revenue per employee** is a proxy for the output a seat is expected to produce. Use your plan's number.
- **Ramp factor** discounts for the fact that a new hire isn't fully productive yet. 0.5 assumes half-productivity in the early weeks, which keeps the estimate conservative.

| Illustrative input | Before | After |
|---|---|---|
| Hires per year | 40 | 40 |
| Avg business days a start date slips (paperwork, approvals, equipment) | 5 | 1 |
| Avg days lost in Week 1 (no laptop, no access, no plan) | 3 | 0.5 |
| Revenue per employee | $250,000 | |
| Ramp factor | 0.5 | |

→ 6.5 days × 40 hires × ~$481 a day ≈ **$125,000 a year**

## 2. Effective headcount

The same days, expressed the way leadership plans:

```
effective headcount recovered = hires per year × days recovered per hire ÷ 260
```

→ 40 × 6.5 ÷ 260 ≈ **1.0 FTE-year**. Fixing the handoff is worth roughly one extra person on the plan, without hiring one.

## 3. Offers kept

A slow, disorganized offer stage loses candidates. Each lost offer restarts the search for that seat.

```
offers per year      = hires per year ÷ acceptance rate (before)
offers kept          = offers per year × (acceptance after − acceptance before)
cost of a lost offer = direct cost to refill + days to refill × daily value per hire
value of offers kept = offers kept × cost of a lost offer
```

| Illustrative input | Value |
|---|---|
| Acceptance rate before → after | 80% → 85% |
| Days to refill a lost offer | 30 business days |
| Direct cost to refill (ads, agency, interview hours) | $5,000 |

→ 50 offers × 5 points = 2.5 searches avoided × ~$19,400 ≈ **$48,600 a year**

## 4. Coordination hours returned

Chasing status, updating trackers and writing summaries by hand.

```
hours returned = (weekly coordination hours before − after) × 52
value          = hours returned × loaded hourly cost
FTE equivalent = hours returned ÷ 2,080
```

→ (8 − 2) × 52 = 312 hours × $75 ≈ **$23,400 a year**, about 0.15 FTE

---

## Total, on the illustrative numbers

| Lever | Annual value |
|---|---|
| Productive days recovered | ~$125,000 |
| Offers kept | ~$48,600 |
| Coordination hours returned | ~$23,400 |
| **Total** | **~$197,000** |
| Effective headcount recovered | ~1.1 FTE |

## Why this compounds as hiring speeds up

Every term above multiplies by **hires per year**. A process that works fine at 10 hires a year quietly breaks at 40, and the cost of each broken handoff grows with the hiring plan. Teams usually notice only when a board-approved headcount number is met on paper but output lags behind it.

## What this model leaves out

- **Early attrition.** A poor first week is linked to early exits, but the effect varies too much to put a reliable number on it here.
- **Manager time.** Hiring managers spend less time asking for status. Not counted.
- **Risk.** Fewer places where pay and personal data can leak. Real, but not a dollar figure.

## How to measure it for real

Track these from the tracker and project tool, weekly, starting before the change:

1. Business days from offer accepted to Day 1, against the original start date
2. Share of hires marked *On time, fully ready* on Day 1
3. Offer acceptance rate
4. Hours per week spent on status and reporting (a two-week time log is enough)
