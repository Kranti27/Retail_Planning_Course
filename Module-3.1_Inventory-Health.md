# Module 3.1: Inventory Health — Reading Stock Like a Doctor Reads Vitals

> *"A doctor doesn't look at a patient and say 'you have blood.' They check blood pressure, hemoglobin, WBC count, cholesterol — each a specific vital sign that tells a specific story. Inventory health is the same. 'We have $40 Million of stock' tells you nothing. HOW OLD is it? WHERE is it? WHAT is it? Those answers tell you whether your stock is healthy or terminal."*

**Semester:** 3 — The Stock  
**Prerequisites:** Module 0.2 (Retail Math), Module 2.1 (Margin Architecture)  
**Estimated Study Time:** 6–7 hours  
**Level:** Core — this is the diagnostic foundation for all inventory decisions

---

## Executive Summary & Core Dilemma

**How do you assess whether your inventory is healthy, sick, or terminal — and what are the specific diagnostic tools that tell you exactly where the problems are?**

Sarah, VP of Merchandising, "rightsized inventory from 12 to 8 months stock holding." Before rightsizing, he had to diagnose. This module gives you the diagnostic toolkit. Your allocation and MIS role makes this especially critical — you're the one building the dashboards that surface inventory health.

---

## What Inventory Health Means (First Principles)

### The Hospital Analogy

Think of your category's inventory as a hospital ward:

| Patient Status | Inventory Equivalent | Characteristic |
|---------------|---------------------|----------------|
| **Healthy** | Fresh, selling well | Age < 90 days, sell-through on plan, good ROS |
| **Recovering** | Slow but responding | Age 90-120 days, below plan but improving with action |
| **Chronic** | Persistent slow mover | Age 120-180 days, requires markdown intervention |
| **Critical** | Significant aging, minimal sales | Age 180-365 days, deep markdown or clearance channel |
| **Terminal** | Dead stock, won't sell at any reasonable price | Age > 365 days, write-off or liquidate |

**A healthy inventory has most patients in the first two categories.** When Sarah found 12 months of stock, the ward was overcrowded with critical and terminal patients — consuming space, capital, and management attention while contributing nothing to sales.

### The Five Vital Signs of Inventory

Every doctor checks five vitals. Every planner should check five inventory vitals:

| Vital Sign | What It Measures | Healthy Range (Home & Lifestyle) |
|-----------|-----------------|----------------------------------|
| **1. Aging Profile** | How old is the stock? | 60%+ under 90 days |
| **2. Weeks of Cover (WOC)** | How long will current stock last? | 8-14 weeks |
| **3. Sell-Through Rate** | What % of buy has sold? | 65-75% at season end |
| **4. Rate of Sale (ROS)** | How fast is stock moving? | Category-dependent |
| **5. Stock-to-Sales Ratio (SSR)** | How much stock per unit of sale? | 2.5-4.0x |

---

## Vital Sign 1: Aging Analysis — The Most Important Diagnostic

### What Aging Tells You

Aging measures how long each unit of stock has been in your system since it was received. It's the single most powerful diagnostic because age correlates directly with:
- Probability of selling at full price (decreases with age)
- Markdown risk (increases with age)
- Working capital lock-up (increases with age)
- Relevance to customer (decreases with age — fashion products especially)

### Building an Aging Report

**Step 1: Define aging buckets**

| Bucket | Age Range | Meaning |
|--------|-----------|---------|
| **Current** | 0-30 days | Just arrived, peak freshness |
| **Fresh** | 31-60 days | Early selling phase |
| **Maturing** | 61-90 days | Mid-season, should be selling steadily |
| **Aging** | 91-120 days | Past peak, needs monitoring |
| **Old** | 121-180 days | Requires markdown intervention |
| **Severe** | 181-365 days | Aggressive clearance needed |
| **Terminal** | 365+ days | Write-off or liquidate |

**Step 2: Categorize all stock**

**Example — Cushions & Covers Aging Report (Snapshot: August 15):**

| Aging Bucket | Stock Value ($00,000) | % of Total | Units | Action Required |
|-------------|---------------------|-----------|-------|----------------|
| 0-30 days | 18.5 | 26% | 2,800 | None — peak selling time |
| 31-60 days | 14.2 | 20% | 2,200 | None — healthy |
| 61-90 days | 10.6 | 15% | 1,600 | Monitor sell-through |
| 91-120 days | 9.2 | 13% | 1,400 | **Review — markdown if < 50% ST** |
| 121-180 days | 8.5 | 12% | 1,300 | **Markdown 20-30%** |
| 181-365 days | 6.4 | 9% | 1,000 | **Aggressive markdown 40-50%** |
| 365+ days | 3.6 | 5% | 600 | **Write-off or liquidate** |
| **Total** | **71.0** | **100%** | **10,900** | |

**Reading this report:**
- **Good news:** 61% of stock ($43.3) is under 90 days — reasonably healthy
- **Warning:** 13% ($9.2) is 91-120 days — these products are losing momentum
- **Problem:** 26% ($18.5) is over 120 days — this is where margin bleeds
- **Critical:** 5% ($3.6) is terminal — this stock is likely unsalvageable

**Sarah's "before" state** would have looked much worse: perhaps only 25% under 90 days and 45% over 180 days.

### Aging Pyramid — The Ideal Shape

A healthy inventory aging profile looks like a pyramid — wide at the bottom (fresh stock), narrow at the top (old stock):

```
    IDEAL SHAPE                    UNHEALTHY SHAPE

     ┌─┐ 365+ (2-3%)                ┌─────┐ 365+ (15%)
    ┌┘ └┐ 181-365 (5-8%)          ┌─┘     └─┐ 181-365 (20%)
   ┌┘   └┐ 121-180 (8-12%)      ┌─┘         └─┐ 121-180 (15%)
  ┌┘     └┐ 91-120 (12-15%)    ┌─┘             └─┐ 91-120 (15%)
 ┌┘       └┐ 61-90 (15-18%)   ┌─┘                 └─┐ 61-90 (15%)
┌┘         └┐ 31-60 (18-22%)  ┌─┘                     └─┐ 31-60 (10%)
┘           └ 0-30 (25-30%)   └─────────────────────────── 0-30 (10%)
```

If your pyramid is inverted (more old stock than new), you have a structural problem that requires the kind of restructuring Sarah executed (Module 3.4).

### Age-Based Action Triggers

Every aging bucket should have a predefined action:

| Age | Trigger | Action | Who Decides |
|-----|---------|--------|-------------|
| 60 days | Sell-through check | If ST < 40%, flag for review | Planner (auto-alert from MIS) |
| 90 days | Formal review | If ST < 50%, initiate markdown or reallocation | Planner + David |
| 120 days | Mandatory action | Markdown 20-30% OR reallocate OR RTV | David approves |
| 180 days | Escalation | Aggressive markdown 40-50% OR clearance channel | Sarah reviews |
| 270 days | Write-down | Provision 50% of cost value in books | Finance team |
| 365 days | Write-off/liquidate | Write off remaining value, sell to liquidator | Sarah + Finance |

**The power of triggers:** They remove emotion from the decision. Without triggers, teams hold onto aging stock hoping "it'll sell next month." With triggers, action is automatic and timely.

---

## Vital Sign 2: Weeks of Cover (WOC) — The Forward-Looking Metric

### What WOC Tells You

WOC answers: "At the current rate of sale, how many weeks will your current stock last?"

**WOC = (Current Stock (units or value)) / (Average Weekly Sales (units or value))**

### Worked Example

| Sub-Category | Current Stock ($00,000) | Avg Weekly Sales ($00,000) | WOC |
|-------------|----------------------|--------------------------|-----|
| Cushion Covers | 71.0 | 5.5 | 12.9 weeks |
| Curtains | 58.0 | 4.2 | 13.8 weeks |
| Table Linen | 32.0 | 2.8 | 11.4 weeks |
| Bed Linen | 85.0 | 5.0 | 17.0 weeks |
| Rugs | 45.0 | 2.1 | 21.4 weeks |
| **Category** | **291.0** | **19.6** | **14.8 weeks** |

**Interpreting WOC:**

| WOC | Status | Interpretation |
|-----|--------|---------------|
| < 6 weeks | **Under-stocked** | Risk of stockouts before next delivery. Chase inventory! |
| 6-8 weeks | **Lean** | Efficient but tight. Good if replenishment is reliable |
| 8-14 weeks | **Healthy** | Adequate buffer with reasonable capital efficiency |
| 14-20 weeks | **Heavy** | Building up — check if seasonal build or problem |
| > 20 weeks | **Over-stocked** | Serious — action required (cut buying, accelerate markdowns) |

**From the example:**
- Cushion Covers (12.9 wks) and Table Linen (11.4 wks) are healthy
- Bed Linen (17.0 wks) is getting heavy — investigate
- Rugs (21.4 wks) is **over-stocked** — needs immediate attention

### WOC Must Be Read With Context

**Trap 1: Seasonal build-up is not a problem**

If it's Week 36 (September) and festive stock is arriving for October-November selling, WOC will spike temporarily. This is planned. The right WOC to track is "WOC vs. WOC Plan" — the variance, not the absolute number.

**Trap 2: Low WOC isn't always good**

WOC of 4 weeks sounds "lean and efficient," but if your replenishment lead time is 8 weeks, you'll run out of stock by Week 5. WOC must be evaluated relative to replenishment lead time.

**Safe WOC >= Lead Time (weeks) + Safety Buffer (weeks)**

If lead time is 8 weeks and you want a 2-week safety buffer:

**Safe WOC >= 8 + 2 = 10 weeks**

**Trap 3: Average WOC hides sub-category problems**

Category WOC = 14.8 weeks looks acceptable. But Rugs at 21.4 weeks is a problem hidden inside the average. Always look at the next level down.

### Forward WOC — The Predictive Version

Standard WOC uses backward-looking average weekly sales. **Forward WOC** uses the planned weekly sales for the coming period:

**Forward WOC = (Current Stock) / (Planned Average Weekly Sales (next 8 weeks))**

This is more accurate because it accounts for seasonal changes. If you're heading into the festive peak (higher weekly sales), forward WOC will be lower than backward WOC — and that's the true picture.

**Example:**
- Current stock: $85 (Bed Linen)
- Backward avg weekly sales: $5.0 → Backward WOC = 17.0 weeks
- Forward avg weekly sales (Oct-Nov festive): $8.5 → Forward WOC = 10.0 weeks

Forward WOC of 10 weeks is healthy — the stock is building AHEAD of a peak. Backward WOC of 17 made it look problematic. **Always use forward WOC for decision-making.**

---

## Vital Sign 3: Sell-Through Rate — The Scorecard of Buying Decisions

### What Sell-Through Tells You

**Sell-Through (%) = (Units Sold) / (Units Received (bought + transferred in)) × 100**

Sell-through measures how much of what you BOUGHT has actually SOLD. It's the ultimate scorecard of the buy decision.

### Sell-Through at Different Time Points

| Measurement Point | Healthy ST | What It Tells You |
|-------------------|-----------|-------------------|
| **Week 4** | 20-25% | Early signal — is the product moving? |
| **Week 8** | 40-50% | Mid-season check — on track or need action? |
| **Week 12** | 55-65% | Late-season — markdown candidates identified |
| **Week 16 (season end)** | 65-80% | Final scorecard — planning quality measure |

### Sell-Through by Product Type

| Product Type | Target ST at Season End | Why |
|-------------|------------------------|-----|
| Fashion/Seasonal | 75-85% | Must clear by season end — style goes stale |
| Core/Year-round | 65-75% | Less urgency — can carry over |
| Basics/Continuity | 60-70% | Designed for ongoing replenishment, not full clearance |
| New/Untested | 60-70% | Higher uncertainty = lower expectations |

### The Sell-Through vs. Sell-Through Curve

Tracking sell-through over time creates a curve that reveals product health:

**Example — Three Products Launched Same Week:**

| Week | Product A (Star) | Product B (Slow Burn) | Product C (Dud) |
|------|-----------------|---------------------|-----------------|
| 2 | 12% | 5% | 3% |
| 4 | 28% | 12% | 6% |
| 6 | 42% | 20% | 8% |
| 8 | 55% | 30% | 10% |
| 10 | 65% | 38% | 12% |
| 12 | 73% | 45% | 13% |
| 14 | 80% | 52% | 14% |
| 16 | 85% | 58% | 15% |

**Reading the curves:**
- **Product A:** Fast start, strong mid-season — a star. Should you have bought more? YES. This is a chase candidate (Module 1.3 chase budget).
- **Product B:** Slow start, steady climb — a solid performer that needs patience. Don't markdown too early. It'll get there.
- **Product C:** Weak start, flat progression — a dud. By Week 6, this pattern is clear. Markdown at Week 8 at latest.

**Your MIS dashboard should show sell-through curves** — not just the latest number. The trajectory tells you far more than the snapshot.

---

## Vital Sign 4: Rate of Sale (ROS) — The Speed Metric

### What ROS Tells You

**ROS = (Units Sold in Period) / (Number of Selling Weeks (or Days))**

ROS is the velocity of sales. Unlike sell-through (which is cumulative), ROS tells you the CURRENT speed.

### Why ROS Matters for Your Allocation Role

When you're deciding how much stock to send to each store, ROS is the primary input:

| Store | ROS (units/week) | Current Stock | WOC at Store | Action |
|-------|------------------|---------------|-------------|--------|
| Mumbai Bandra | 4.2 | 12 | 2.9 | **Replenish URGENTLY — will stockout this week** |
| Delhi Khan Market | 3.5 | 28 | 8.0 | Adequate — next replenishment on schedule |
| Bangalore Indiranagar | 2.8 | 35 | 12.5 | Over-stocked — reduce next allocation |
| Pune Koregaon Park | 1.2 | 30 | 25.0 | **Massively over-stocked — transfer out or markdown** |

**ROS at the store-product level drives your daily allocation decisions.** A good replenishment system (Module 4.3) uses ROS automatically.

### ROS Decay: The Warning Sign

When a product's ROS starts declining week over week, it's a decay signal:

| Week | ROS | Trend |
|------|-----|-------|
| W1 | 45 units | — |
| W2 | 42 units | ↓ slight |
| W3 | 38 units | ↓ notable |
| W4 | 30 units | ↓ significant |
| W5 | 22 units | ↓ **Alarm — 51% drop from peak** |

**Rule of thumb:** If ROS drops 30%+ from its 4-week average over 2 consecutive weeks, the product is entering decline. Time to evaluate markdown (Module 2.3).

---

## Vital Sign 5: Stock-to-Sales Ratio (SSR) — The Balance Check

### What SSR Tells You

**SSR = (BOM Stock (at retail)) / (Monthly Sales (at retail))**

SSR tells you how many months of sales you're carrying in stock at any given time.

### SSR Interpretation

| SSR | Meaning | Typical For |
|-----|---------|------------|
| 1.5-2.5 | Lean | Fast-turn categories, basics |
| 2.5-4.0 | Balanced | Home & Lifestyle, moderate turn |
| 4.0-6.0 | Heavy | Furniture, long lead time |
| > 6.0 | Over-invested | Problem — unless pre-season build |

### SSR Over Time — The Breathing Pattern

Healthy inventory "breathes" — SSR rises before a peak (stock building) and falls during the peak (stock selling):

| Month | Sales Plan | BOM Stock | SSR | What's Happening |
|-------|-----------|-----------|-----|-----------------|
| Sep | $109k | $381k | 3.5 | Building for festive |
| Oct | $156k | $420k | 2.7 | Festive peak — lean selling |
| Nov | $141k | $300k | 2.1 | Post-peak — stock depleting |
| Dec | $114k | $220k | 1.9 | Winding down — very lean |
| Jan | $88k | $180k | 2.0 | Off-peak |

**This breathing pattern is healthy.** SSR drops during high-sales months (the stock is converting to sales efficiently) and rises before peaks (planned build-up).

**Unhealthy pattern:** SSR stays flat or increases during selling months — meaning stock is building even as you SHOULD be selling. This signals over-buying or demand shortfall.

---

## The Integrated Health Dashboard

### Pulling All Five Vitals Together

For David's weekly review, an integrated dashboard would show:

| Sub-Category | WOC | ST% (cumulative) | ROS Trend | SSR | Aging (>120 days %) | **Health Score** |
|-------------|-----|-------------------|-----------|-----|--------------------|--------------------|
| Cushions | 12.9 | 52% | Stable | 3.2 | 26% | ⚠️ Moderate |
| Curtains | 13.8 | 48% | Declining ↓ | 3.4 | 30% | ⚠️ Watch |
| Table Linen | 11.4 | 58% | Rising ↑ | 2.8 | 18% | ✅ Healthy |
| Bed Linen | 17.0 | 45% | Declining ↓ | 4.1 | 35% | 🔴 Concerning |
| Rugs | 21.4 | 38% | Flat | 5.2 | 42% | 🔴 Critical |

**Reading the dashboard:** The traffic light system draws immediate attention to Rugs and Bed Linen. Both have high WOC, low sell-through, and significant aging. These sub-categories need intervention — markdown planning (Module 2.3) and possible ISQ cuts for forward buys.

### Health Score Calculation (Simple Model)

You can create a composite health score:

**Health Score = w_1 × WOC Score + w_2 × ST Score + w_3 × Aging Score + w_4 × ROS Score**

Where each component is scored 1-5 (1 = critical, 5 = excellent) and weights reflect importance:

| Component | Weight | Score 1 (Critical) | Score 2 (Poor) | Score 3 (Average) | Score 4 (Good) | Score 5 (Excellent) |
|-----------|--------|--------------------|----------------|-------------------|----------------|---------------------|
| WOC vs Plan | 30% | WOC > 2× plan | WOC 1.5×-2× plan | WOC 1.2×-1.5× plan | WOC ±20% of plan | WOC within ±10% of plan |
| Sell-Through vs Plan | 25% | ST < 60% of plan | ST 60%-75% of plan | ST 75%-90% of plan | ST 90%-100% of plan | ST ≥ 100% of plan |
| Aging (>120 days %) | 25% | >40% of stock aged | 30%-40% of stock aged | 20%-30% of stock aged | 10%-20% of stock aged | <10% of stock aged |
| ROS Trend | 20% | Declining >20%/week | Declining 10-20%/week | Flat / minor decline | Growing slightly | Growing >10%/week |

---

## Inventory Health at Different Levels

### Level 1: Category (Sarah's View)

One number, one chart: Total category WOC trend over the last 12 months. Is it improving (trending down toward target) or deteriorating (trending up)?

### Level 2: Sub-Category (David's View)

Table of sub-categories with all five vitals. Focus on outliers — the best and worst performers.

### Level 3: Style/Option (Your Current Level)

Individual product health. This is where your allocation decisions live. Which specific products need replenishment? Which need markdown? Which need reallocation?

### Level 4: Store-SKU (Operational Detail)

The most granular level. Store-level stock health by SKU. This powers the replenishment system (Module 4.3).

**Key insight:** Information needs differ by level. Sarah doesn't need store-SKU data daily. You do. Build dashboards for the right audience at the right granularity.

---

## Executive Perspectives

### How David Thinks About Inventory Health

David, Director of Planning, checks inventory health weekly. His process:

1. **Start with WOC at sub-category level:** Any sub-category > target WOC? If yes, investigate.
2. **Check aging profile:** Has the aging mix worsened from last week? If >120 day bucket is growing, flag.
3. **Review sell-through curves for flagged products:** Are they on trajectory or deteriorating?
4. **Trigger actions:** Prepare markdown proposals for products hitting age triggers.
5. **Check forward receipt plan:** Is more stock arriving for an already over-stocked sub-category? If yes, defer or cancel.

### How Sarah Thinks About Inventory Health

Sarah reviews monthly at the category level:

1. **Total inventory value vs. target:** Are we tracking toward the 8-month target?
2. **Aging improvement:** Is the >180 day bucket shrinking month over month?
3. **GMROI trend:** Is margin × turn improving?
4. **Working capital deployment:** How much capital is locked vs. available?

### How You Should Read Inventory Health

In your allocation role, focus on:
1. **Store-level WOC for key products:** Which stores are running out? Which are overstocked?
2. **Product-level sell-through curves:** Spot duds early and escalate to David.
3. **Aging flags in your MIS:** Automate the age-based action triggers.

---

## Strategic Trade-Offs & Risk Matrices

### Trade-Off 1: Freshness vs. Availability

Aggressively clearing old stock improves aging profile but might leave gaps if new stock doesn't arrive on time.

### Trade-Off 2: Accuracy vs. Timeliness

The most accurate inventory health analysis uses physical count data (which might be monthly). System data is available daily but may have errors. Use system data for daily decisions but validate against physical counts periodically.

### Trade-Off 3: Granularity vs. Actionability

A store-SKU-level health report with 50,000 rows is accurate but overwhelming. Summarize for action: top 20 products needing replenishment, top 20 needing markdown, top 10 stores with health issues.

---

## Strategic & Operational Pitfalls

1. **Looking only at total stock value:** "We have $291 of stock" is meaningless without age, composition, and velocity context. $291 of fresh, fast-selling stock is excellent. $291 of 9-month-old stock is a disaster.
2. **Using backward WOC for forward decisions:** Backward WOC (based on past sales) misleads during seasonal transitions. If you're entering the festive peak, forward WOC will be much lower. Use forward WOC with planned sales.
3. **Setting uniform WOC targets across sub-categories:** Cushion covers (fast turn, replenishable) might target 10 weeks WOC. Furniture (long lead time, slow turn) might need 20 weeks. Uniform targets over-stock slow movers and under-stock fast movers.
4. **Ignoring the "healthy old stock" scenario:** Continuity/basics items that are 6+ months old but selling steadily are NOT a problem — they're by design. Don't markdown basics just because they're old. Apply aging triggers to seasonal/fashion products, not to evergreen basics.
5. **Celebrating sell-through without checking margin:** A product with 90% sell-through at full price is excellent. A product with 90% sell-through because you marked it down 50% is a planning failure that looks successful.
6. **Not comparing sell-through to the PLAN:** 50% sell-through at Week 8 sounds low. But if the plan was 45% at Week 8, you're actually AHEAD. Always measure against plan, not against arbitrary benchmarks.
7. **Building dashboards with too much data and too little insight:** A 50-column report that nobody reads is worse than a 5-metric dashboard that drives weekly action. Design for decision-making, not for comprehensiveness.

---

## Case Application & Discussion Questions

1. **Build an Aging Report (45 minutes):** For any sub-category you can access (or estimate from knowledge):
   - Categorize current stock into the 7 aging buckets
   - Calculate the % distribution
   - Draw the aging pyramid — is it healthy or inverted?
   - Identify the top 5 SKUs in the >120 day bucket
   - For each, recommend: markdown, reallocate, RTV, or write-off
2. **WOC Analysis (30 minutes):** Calculate WOC for your top 5 sub-categories using both backward WOC (last 4 weeks average sales) and forward WOC (planned sales for next 8 weeks). Where do they differ? Why? Which should drive your action?
3. **Sell-Through Curve Tracking (30 minutes):** Pick 3 products launched at the same time:
   - Plot their sell-through curves (Week 2, 4, 6, 8, 10, 12)
   - Which is a star? Which is a dud?
   - At what week could you first identify the dud?
   - What action would you have recommended, and when?
4. **Design the Health Dashboard (45 minutes):** Design (on paper or in Excel mock-up) the "Inventory Health Dashboard" for David:
   - What metrics to show
   - At what granularity (sub-category? product? store?)
   - What frequency (daily? weekly?)
   - What alert thresholds
   - What visual format (table? chart? traffic light?)
5. **Health Score Calculation (20 minutes):** Using the composite health score model, score these 4 sub-categories (assume data provided in class). Score each component 1-5. Calculate the composite health score. Which sub-category needs the most urgent attention?

---

## Connection to Next Module

Module 3.1 gave you the diagnostic tools — the ability to read inventory health. Module 3.2 goes into the financial consequence: what does inventory health mean for **stock turn and working capital**? When Sarah reduced stock from 12 to 8 months, he freed $24 Million of working capital. Module 3.2 teaches you the math behind that transformation.

**Next Module:** [Module 3.2: Stock Turn and Working Capital](Module-3.2_Stock-Turn-and-Working-Capital.md)

---

## Key Takeaways

1. **Inventory health is measured by five vitals,** not one number. Aging, WOC, sell-through, ROS, and SSR each tell a different part of the story.
2. **Aging is the most important diagnostic.** It directly predicts margin erosion, markdown risk, and working capital lock-up.
3. **Set age-based action triggers.** Automated alerts at 90, 120, 180, and 365 days remove emotion and ensure timely action.
4. **Always use forward WOC,** not backward WOC, for decision-making. Backward WOC misleads during seasonal transitions.
5. **Track sell-through curves, not just snapshots.** The trajectory reveals whether a product is a star, slow burn, or dud — often by Week 6.
6. **Build dashboards for the right audience.** Sarah needs category-level monthly trends. David needs sub-category weekly action triggers. You need store-product daily operational data.
7. **Healthy inventory breathes.** SSR rises before peaks and falls during peaks. An SSR that only rises is a warning sign.
