# Module 0.2: Retail Math Essentials — The Numbers That Run a Retail Business

> *"If you can't calculate it, you can't manage it. If you can't explain the calculation's impact on enterprise value to the C-suite, you don't truly understand it."*

**Semester:** 0 — Foundations  
**Prerequisites:** Module 0.1 (The Retail System)  
**Estimated Study Time:** 7–9 hours  
**Level:** Core

---

## Executive Summary & Core Dilemma

What are the fundamental calculations that every retail planning decision rests on? Not as formulas to memorize, but as strategic logic to internalize — so you can reconstruct any metric from first principles to defend your capital allocation decisions.

---

## Why Retail Math Exists (The Problem It Solves)

Retail decisions involve thousands of products, hundreds of stores, and millions of dollars. Without standardized math, planners would make decisions based on gut feeling and anecdote. Retail math does three things:

1. **Creates a common language.** When Sarah says "GMROI is 3.2," every executive knows exactly what that means — no ambiguity.
2. **Enables comparison.** Is Store A performing better than Store B? Is Category X a better use of capital than Category Y?
3. **Reveals truth that intuition misses.** A product line might FEEL successful because it generates high revenue, but the math might show it has terrible stock turn and is destroying working capital and shareholder value.

---

## Revenue Math

### Net Sales

The most basic number in retail. But even this has nuance.

**Net Sales = Gross Sales - Returns - Employee Discounts - Damaged/Defective Allowances**

**Why "Gross Sales" lies:** Gross sales includes everything sold at the register. If you plan based on gross sales, you'll overestimate revenue and misallocate capital.

**Example:**

| Metric | Value |
|--------|-------|
| Gross Sales | $1 Million |
| Returns | $30,000 (3%) |
| Employee Discounts | $5,000 |
| Net Sales | $965,000 |

### Average Selling Price (ASP)

**ASP = (Net Sales ($)) / (Units Sold)**

**What it tells you:** The average realized price after discounts.

**Example:**

| Scenario | Net Sales | Units Sold | ASP |
|----------|----------|------------|-----|
| Full price season | $500,000 | 2,000 | $250 |
| During EOSS | $500,000 | 3,125 | $160 |

Same revenue, but the EOSS (End of Season Sale) scenario sells more units at a lower price. The ASP drop of $90 tells you margin is being sacrificed for volume.

### Average Transaction Value (ATV)

**ATV = (Net Sales ($)) / (Number of Transactions)**

**ATV = ASP × UPT (Units Per Transaction)**

**Example:**

| Metric | Store A | Store B |
|--------|---------|---------|
| Net Sales | $200,000 | $200,000 |
| Transactions | 1,000 | 800 |
| Units Sold | 1,500 | 2,000 |
| ATV | $200 | $250 |
| UPT | 1.5 | 2.5 |
| ASP | $133 | $100 |

**Store B has higher ATV despite lower ASP.** Customers buy more items per visit (UPT = 2.5 vs. 1.5), indicating better cross-selling.

### Conversion Rate

**Conversion Rate = (Number of Transactions) / (Footfall (Visitors)) × 100**

**Example:**

| Metric | Flagship Store | Mall Store |
|--------|---------------|------------|
| Footfall | 5,000 | 8,000 |
| Transactions | 500 | 640 |
| Conversion | 10% | 8% |

### Like-for-Like (LFL) / Comparable Store Sales

**LFL Growth (%) = (Sales this year (same stores) - Sales last year (same stores)) / (Sales last year (same stores)) × 100**

**Why this exists:** LFL strips out the new store effect and shows organic growth, providing a true measure of operational health.

### Sales Decomposition — The Revenue Tree

Any sales result can be decomposed:

**Net Sales = Footfall × Conversion Rate × UPT × ASP**

| Scenario | Footfall | Conversion | UPT | ASP | Net Sales |
|----------|---------|-----------|-----|-----|-----------|
| Baseline | 10,000 | 10% | 1.5 | $200 | $300,000 |
| More traffic | 12,000 | 10% | 1.5 | $200 | $360,000 |
| Better conversion | 10,000 | 12% | 1.5 | $200 | $360,000 |
| Higher UPT | 10,000 | 10% | 1.8 | $200 | $360,000 |
| Higher ASP | 10,000 | 10% | 1.5 | $240 | $360,000 |

Same $360,000 result, four different strategic implications.

---

## Margin Math

### Markup vs. Margin — The Trap That Catches Everyone

**Markup** is calculated on COST:

**Markup (%) = (Selling Price - Cost Price) / (Cost Price) × 100**

**Margin** is calculated on SELLING PRICE:

**Margin (%) = (Selling Price - Cost Price) / (Selling Price) × 100**

**Example with same product:**

| Metric | Value |
|--------|-------|
| Cost Price | $40 |
| Selling Price | $100 |
| Markup | (100 − 40) ÷ 40 = **150%** |
| Margin | (100 − 40) ÷ 100 = **60%** |

When Sarah says "driving 60%+ gross margins," she means margin on selling price, not markup.

**The conversion between them:**

**Margin (%) = (Markup (%)) / (100 + Markup (%)) × 100**
**Markup (%) = (Margin (%)) / (100 - Margin (%)) × 100**

### Initial Markup (IMU)

**IMU (%) = (MSRP - Cost Price) / (MSRP) × 100**

**The IMU planning question:** 

**Required IMU % = (Target Maintained Margin % + Reductions %) / (100% + Reductions %)**

With a 55% target margin and 8% expected reductions:
**Required IMU % = (55% + 8%) / (100% + 8%) = 63% / 108% = 58.3%**

Any product entering with IMU below 58.3% is a risk to enterprise value. This is why David reviews costings style-wise to protect GP.

### Maintained Margin (MMU) and Gross Margin (GM)

**Maintained Margin = IMU - Markdowns - Shrinkage - Employee Discounts**

**Gross Margin (%) = (Net Sales - Cost of Goods Sold) / (Net Sales) × 100**

**The Margin Waterfall:**

```
Total Retail Value (MSRP)                $108.00  (IMU is 58.3%, so Cost = $45.00)
  − Planned Markdowns (6% of net sales)   −$6.00
  − Unplanned Markdowns/Shrinkage (2%)    −$2.00
  ─────────────────────────────────────
= Net Sales                              $100.00
  − Cost of Goods Sold                   −$45.00
  ─────────────────────────────────────
= Realized Gross Margin                   $55.00  (55.0% of Net Sales)
```

### Margin Mix Effect — The Invisible Killer

Even if every product maintains its margin, the CATEGORY margin can change if the MIX of sales shifts.

**Example:**

| Product | Sales Mix (Plan) | GM% | Sales Mix (Actual) | GM% |
|---------|-----------------|-----|-------------------|-----|
| High-Margin Textiles | 40% | 65% | 30% | 65% |
| Medium-Margin Décor | 35% | 55% | 35% | 55% |
| Low-Margin Furniture | 25% | 45% | 35% | 45% |

**Planned Category GM:** 56.5%
**Actual Category GM:** 54.5%

Category margin dropped 2 percentage points because the mix shifted. On $100 Million revenue, that's a $2 Million gross margin destruction.

---

## Inventory Math

### Stock Turn (Inventory Turnover)

**Stock Turn = (Net Sales (at Retail)) / (Average Inventory (at Retail))**

| Metric | Category A | Category B |
|--------|-----------|-----------|
| Annual Net Sales | $10 Million | $10 Million |
| Average Inventory | $3.33 Million | $5 Million |
| Stock Turn | 3.0x | 2.0x |

Category A is more capital-efficient.

### Weeks of Cover (WOC)

**WOC = (Current Stock (units or $)) / (Average Weekly Sales (units or $))**

### Stock-to-Sales Ratio (SSR)

**SSR = (Beginning of Month (BOM) Stock) / (Month's Sales)**

### Sell-Through Rate (STR)

**Sell-Through (%) = (Units Sold) / (Units Received) × 100**

### GMROI — Gross Margin Return on Inventory Investment

**GMROI = (Gross Margin ($)) / (Average Inventory at Cost ($))**

**Why this is the planner's ultimate metric:** It answers: **For every dollar invested in inventory, how many dollars of gross margin did I generate for shareholders?**

**Example:**

| Category | Net Sales | GM% | Gross Margin | Avg Inventory (Cost) | GMROI |
|----------|----------|-----|-------------|---------------------|-------|
| Textiles | $10 Million | 60% | $6 Million | $1.5 Million | 4.0 |
| Furniture | $10 Million | 45% | $4.5 Million | $3 Million | 1.5 |

Same sales, but Textiles generates $4 of gross margin for every $1 of inventory investment. This amplifies return on capital.

### Aging Analysis

**Age (days) = Today's Date - Receipt Date**
**Fresh Stock Ratio = (Stock aged 0-90 days) / (Total Stock) × 100**
**Aged Stock Ratio = (Stock aged 180+ days) / (Total Stock) × 100**

---

## Productivity Math

### Sales per Square Foot

**Sales per Sqft = (Net Sales) / (Selling Area (Sqft))**

### Productivity per Store

**Productivity per Store = (Total Category Sales) / (Number of Stores Carrying the Category)**

### Revenue per Option (Productivity)

**Revenue per Option = (Net Sales) / (Number of Active Options)**
Sarah focused on this when rationalizing the SKU base to improve per-SKU yield.

### GMROF — Gross Margin Return on Floor

**GMROF = (Gross Margin ($)) / (Selling Floor Area (Sqft))**

---

## Executive Perspectives

### How Sarah Thinks About Math
Sarah looks at aggregated metrics (Category GM%, GMROI, LFL Growth). She obsesses over the **mix effect** and overall capital efficiency to maximize enterprise value.

### How David Operates
David works in the trenches with WOC, Sell-Through, and IMU. He ensures the tactical metrics track towards Sarah's strategic goals, escalating immediately when margin erodes.

---

## Strategic Trade-Offs & Risk Matrices

### Trade-Off 1: Velocity vs. Margin
Higher prices → Higher margin but slower movement. Lower prices → Lower margin but faster movement.
**Resolution:** Optimize GMROI, balancing both to maximize yield.

### Trade-Off 2: Sales vs. Productivity
More stores or SKUs → Higher total sales but potentially lower productivity.
**Resolution:** Celebrate absolute growth only if per-unit productivity (ROIC) is maintained.

### Trade-Off 3: Availability vs. Aging
More stock → Better availability but higher aging risk.
**Resolution:** Use differentiated stock targets by product lifecycle stage.

---

## Strategic & Operational Pitfalls

1. **"Our margin is 60%" without specifying WHICH margin.** IMU? Maintained margin? Confusing them destroys profitability.
2. **Comparing metrics across different denominators.** Stock turn at cost vs. retail.
3. **Celebrating high sell-through without checking for lost sales.** You may have left money on the table.
4. **Ignoring mix effect on margin.** Category margin can drop even if product margins hold.
5. **Treating WOC as static.** WOC changes as sales rates change. Use forward-looking WOC.

---

## Case Application & Discussion Questions

1. **Revenue Decomposition:** Decompose sales: **Sales = Footfall × Conversion × UPT × ASP**. Which factor presents the biggest strategic opportunity?
2. **Margin Waterfall:** Build the margin waterfall for your category. Where is capital leaking?
3. **GMROI by Sub-Category:** Calculate GMROI for each sub-category. Which is the best use of shareholder capital?
4. **Aging Dashboard:** Trace back any aged stock ratio over 30% to find the operational failure.

---

## Connection to Next Module

Knowing how to calculate GMROI doesn't tell you what to DO about it. That requires **decision frameworks** — the strategic logic for converting data into executive action.

**Next Module:** [Module 0.3: Decision Frameworks](Module-0.3_Decision-Frameworks.md)

---

## Key Takeaways

1. Retail math provides a common language that eliminates ambiguity for the executive team.
2. Revenue growth can be strategically decomposed to identify the exact source of growth or decline.
3. Markup is calculated on Cost; Margin is calculated on Selling Price. Confusing them destroys value.
4. The Margin Waterfall tracks how Initial Markup erodes into Realized Gross Margin.
5. GMROI is the ultimate metric because it combines profitability with capital efficiency (velocity).
6. A category's overall margin can drop even if individual margins hold steady, due to the Margin Mix Effect.
