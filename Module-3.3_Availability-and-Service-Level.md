# Module 3.3: Availability vs. Investment — The Fundamental Trade-Off

> *"Every planner faces the same impossible tension: carry more stock and you waste capital; carry less stock and you lose sales. The art of planning is not choosing one over the other — it's finding the precise point where one more unit of stock costs more to hold than the sale it would generate. That point is your optimal service level."*

**Semester:** 3 — The Stock  
**Prerequisites:** Module 3.1 (Inventory Health), Module 3.2 (Stock Turn & Working Capital)  
**Estimated Study Time:** 6–7 hours  
**Level:** Core — this is the central tension of retail planning

---

## Executive Summary & Core Dilemma

**How much stock should you carry to maximize product availability while minimizing the cost of holding that stock — and how do you formalize this trade-off into a repeatable, data-driven system?**

Sarah reduced stock from 12 to 8 months AND simultaneously reduced lost sales from 5% to 2%. That seems paradoxical — less stock but fewer stockouts? It's possible because availability isn't about QUANTITY of stock. It's about having the RIGHT stock in the RIGHT place at the RIGHT time. This module teaches the framework.

---

## What Availability Means (First Principles)

### The Availability Question

At any given moment, a customer walks into a store looking for a product. Is it there?

**Availability (%) = (Number of times product is in stock when customer wants it) / (Number of times customer wants it) × 100**

This is also called the **Service Level** or **In-Stock Rate**.

### Why 100% Availability Is Impossible (and Undesirable)

To achieve 100% availability, you would need infinite stock of every product in every store at all times. That's obviously impossible. But even if you could, you shouldn't — because the COST of achieving that last percentage point of availability increases exponentially.

**The diminishing returns curve:**

| Service Level | Relative Stock Required | Marginal Cost to Add 1% |
|--------------|------------------------|-------------------------|
| 80% | 1.0× | Low |
| 85% | 1.2× | Low |
| 90% | 1.5× | Moderate |
| 93% | 1.8× | Moderate |
| 95% | 2.2× | High |
| 97% | 2.8× | Very High |
| 99% | 4.0× | Extremely High |
| 99.9% | 6.0× | Astronomical |

Moving from 95% to 99% availability requires nearly DOUBLING your stock investment. Is that extra 4% of availability worth the extra $ Cr of working capital?

The answer depends on the product.

---

## Service Level Targeting: Not All Products Deserve Equal Availability

### The Differentiated Service Level Framework

| Product Type | Target Service Level | Rationale | Stock Strategy |
|-------------|---------------------|-----------|---------------|
| **A-Class (Top 20% of sales)** | 95-98% | These are your revenue drivers. A stockout here directly hits the top line | Carry safety stock, replenish frequently |
| **B-Class (Next 30% of sales)** | 90-95% | Important but not critical. Occasional stockout is acceptable | Moderate safety stock |
| **C-Class (Bottom 50% of sales)** | 80-90% | Low volume, high variety. Stockouts have minimal revenue impact | Minimal safety stock, accept stockouts |
| **New/Untested** | 85-90% | Unknown demand — need enough to test but not over-commit | Conservative initial stock, chase if successful |

**Worked Example — Aura Global Retail Cushion Covers:**

| Class | # of SKUs | Revenue Share | Target SL | Avg Stock Investment |
|-------|-----------|--------------|-----------|---------------------|
| A | 15 SKUs | 60% ($83.6) | 96% | $28 (high depth) |
| B | 25 SKUs | 30% ($41.8) | 92% | $18 (moderate) |
| C | 60 SKUs | 10% ($13.9) | 85% | $8 (minimal) |
| **Total** | **100 SKUs** | **100% ($139.3)** | **Weighted: 93%** | **$54** |

If you applied 96% service level to ALL 100 SKUs, total stock required would be ~$75 — $21 more for only marginal revenue improvement from B and C class items.

---

## The Cost of Stockouts: Quantifying Lost Sales

### What Happens When a Customer Can't Find What They Want

| Customer Response | Probability | Revenue Impact | Brand Impact |
|------------------|------------|---------------|-------------|
| **Buys a substitute** (different color/style) | 30-40% | Partial — may buy lower margin item | Neutral |
| **Defers purchase** (comes back later) | 15-25% | Delayed — might come back | Slight negative |
| **Switches to competitor** | 20-30% | Full loss — sale gone | Negative |
| **Abandons purchase entirely** | 10-20% | Full loss — need evaporates | Negative |

**Calculating the cost of a stockout:**

**Lost Sale Cost = Probability of Lost Sale × Average Transaction Value × Margin %**

If 60% of stockout encounters result in a lost sale (competitor switch + abandon):

**Lost Sale per Stockout = 0.60 × $30 × 62% = $11.16 margin lost per incident**

**Scaling up:** If you have 500 stockout incidents per month across the chain:

**Monthly Lost Sales Margin = 500 × $11.16 = $5,580 per month = $66,960 per year**

Sarah reduced lost sales from 5% to 2% on a $100 Million category. That's a $3 Million reduction in lost sales — at ~60% margin, that's $1.8 Million of recovered margin.

---

## Safety Stock: The Buffer Against Uncertainty

### Why Safety Stock Exists

Even with perfect planning, reality introduces variability:

| Source of Variability | Example |
|----------------------|---------|
| **Demand variability** | Week 1 sells 50 units, Week 2 sells 30, Week 3 sells 65 — unpredictable |
| **Supply variability** | Vendor promises delivery in 6 weeks, actually takes 8 weeks |
| **Quality variability** | 5% of received stock fails quality check, reducing usable inventory |
| **System errors** | System says 20 units, physical count shows 17 |

Safety stock is the extra inventory held to buffer against these variabilities.

### Calculating Safety Stock

**The Combined Variability Formula:**

**σ_combined = √(L × σ_d² + d² × σ_L²)**

Where:
- $L$ = Lead time
- $\sigma_d$ = Standard deviation of demand
- $d$ = Average demand
- $\sigma_L$ = Standard deviation of lead time

**Safety Stock = Z × σ_combined**

**Z-scores by service level:**

| Service Level | Z-Score | Meaning |
|--------------|---------|---------|
| 80% | 0.84 | Stockout 20% of the time |
| 85% | 1.04 | Stockout 15% of the time |
| 90% | 1.28 | Stockout 10% of the time |
| 93% | 1.48 | Stockout 7% of the time |
| 95% | 1.65 | Stockout 5% of the time |
| 97% | 1.88 | Stockout 3% of the time |
| 99% | 2.33 | Stockout 1% of the time |

### Worked Example: Safety Stock Calculation

**Product: Indigo Block Print Cushion Cover ($30)**

| Parameter | Value | Source |
|-----------|-------|--------|
| Average weekly demand | 45 units | Last 12 weeks |
| Standard deviation of weekly demand | 12 units | Calculated from weekly data |
| Lead time | 8 weeks | Vendor delivery + warehouse processing |
| Target service level | 95% | A-class product |
| Z-score | 1.65 | From table |

**Safety Stock = 1.65 × 12 × √8 = 1.65 × 12 × 2.83 = 56 units**

**Interpretation:** Carrying 56 extra units (beyond the expected demand during lead time) gives you a 95% probability of not stocking out during the replenishment lead time.

**The total stock you should hold at reorder point:**

**Reorder Point = (Average Demand × Lead Time) + Safety Stock**

**Reorder Point = (45 × 8) + 56 = 360 + 56 = 416 units**

When your total stock drops to 416 units, trigger a replenishment order.

**Cost of this safety stock:**

**SS Investment = 56 units × $11.40 cost = $638.40**

**Annual Carrying Cost = $638.40 × 20% = $127.68 per year**

Is $128 per year worth it to prevent stockouts on a product that generates $70,000+ in annual revenue? Absolutely.

### Safety Stock for Different Service Levels

| Target SL | Z-Score | Safety Stock (units) | Investment ($) | Carrying Cost/Year |
|-----------|---------|---------------------|----------------|-------------------|
| 85% | 1.04 | 35 | $30 | $6 |
| 90% | 1.28 | 43 | $490 | $98 |
| 95% | 1.65 | 56 | $638 | $128 |
| 97% | 1.88 | 64 | $730 | $146 |
| 99% | 2.33 | 79 | $901 | $180 |

Moving from 95% to 99% requires 23 more units ($262 more investment). Those 23 units protect against the rarest demand spikes. For an A-class product, probably worth it. For a C-class product, definitely not.

---

## The Availability-Investment Trade-Off: Finding the Sweet Spot

### The Economic Order Quantity Lens

At its core, the trade-off is between two costs that move in opposite directions:

| More Stock → | Less Stock → |
|-------------|-------------|
| ↑ Carrying cost | ↓ Carrying cost |
| ↓ Stockout cost | ↑ Stockout cost |
| ↑ Working capital tied | ↓ Working capital tied |
| ↑ Markdown risk | ↓ Markdown risk |
| ↓ Lost sales | ↑ Lost sales |

**The optimal point is where:**

**Marginal Cost of One More Unit of Stock = Marginal Benefit of One More Sale Saved**

### Worked Example: The Optimization

**Product:** Core cushion cover, $30 MRP, $11.40 cost

| Scenario | Stock Level | Service Level | Est. Lost Sales/Year | Carrying Cost/Year | Total Cost |
|----------|-----------|--------------|---------------------|-------------------|-----------|
| A: Minimal | 300 | 80% | $445 margin lost | $70 | $515 |
| B: Moderate | 400 | 90% | $225 margin lost | $90 | $315 |
| C: Target | 450 | 95% | $110 margin lost | $105 | $215 |
| D: Heavy | 550 | 98% | $45 margin lost | $125 | $170 |
| E: Maximum | 700 | 99.5% | $10 margin lost | $160 | $170 |

**The sweet spot is around Scenario D (98% service level).** Beyond that, each additional unit of stock reduces lost sales by less than it costs to hold.

But this analysis is for an A-class product. For a C-class product that generates 1/10th the revenue, the sweet spot shifts to Scenario B (90%).

---

## Lost Sales Measurement: The Invisible Metric

### Why Lost Sales Are Hard to Measure

You can't count what didn't happen. When a customer leaves empty-handed, no transaction is recorded. Lost sales are inherently invisible.

### Proxy Methods for Estimating Lost Sales

**Method 1: Stockout Days × Estimated Daily ROS**

**Lost Sales (units) = Days Out of Stock × Average Daily ROS (when in stock)**

If a product was out of stock for 12 days and its average daily ROS (when in stock) is 3 units:

**Lost Sales = 12 × 3 = 36 units = 36 × $30 = $1,080**

**Method 2: Comparable Store Analysis**

If Store A stocked out of Product X but Stores B, C, D (similar profile) didn't:

**Estimated Lost Sales at Store A = Average Sales at B, C, D during the stockout period**

**Method 3: Pre-Stockout Run Rate**

If a product was selling 50 units/week before stockout and then dropped to 0:

**Lost Sales = 50 units/week × Weeks of Stockout × Decay Factor**

(Decay factor accounts for the fact that demand might have declined naturally — use 0.8-0.9)

### Building Lost Sales into Your MIS

**Your dashboard should track:**

1. **Stockout incidents** — how many SKU-store combinations had zero stock today?
2. **Stockout duration** — average days of stockout per incident
3. **Estimated lost sales** — using one of the proxy methods above
4. **Stockout concentration** — are stockouts concentrated in A-class products (critical) or C-class (less critical)?

Sarah's reduction from 5% to 2% lost sales implies his team was measuring and tracking this. Your MIS capability is key to enabling this measurement.

---

## The Paradox Explained: Less Stock, Fewer Stockouts

Sarah had 12 months of stock and 5% lost sales. After restructuring: 8 months of stock and 2% lost sales. How?

### The "Right Stock" Framework

| Before (12 months, 5% lost sales) | After (8 months, 2% lost sales) |
|-----------------------------------|--------------------------------|
| 15% of stock was terminal (365+ days) | Terminal stock purged to 5% |
| Wide assortment with thin depth per option | Rationalized assortment with viable depth |
| Uniform allocation regardless of store performance | Graded allocation based on store demand |
| Safety stock on all products equally | Safety stock concentrated on A-class |
| No age-based action triggers | Systematic triggers at 90/120/180/365 days |
| Slow markdown response | Timely markdown intervention |

**The insight:** 12 months of stock doesn't mean 12 months of the RIGHT stock. Much of it was dead stock occupying warehouse space and capital while the fast-selling items ran out. By clearing the deadwood and concentrating investment in the right products at the right stores, less total capital delivered BETTER availability.

Think of it as a hospital analogy: a hospital with 1,000 beds where 400 are occupied by patients who should have been discharged long ago has WORSE availability than a hospital with 600 beds where every bed is actively managed.

---

## Executive Perspectives

### How David Manages Availability

David's weekly availability review:

1. **Check overall in-stock rate:** Target 93-95% for the category
2. **Review A-class stockouts:** Any A-class product below 95% SL? Why?
3. **Check replenishment pipeline:** Are pending orders on track to maintain availability?
4. **Review safety stock levels:** Are they appropriate for current demand patterns?

### How Sarah Thinks About Availability

Sarah thinks in terms of the cost trade-off:

> "Every 1% improvement in availability costs $X in additional stock investment. Every 1% lost sales costs $Y in margin. When X > Y, we're over-investing. When Y > X, we're under-investing. My job is to find the equilibrium."

### How You Should Think About Availability

As the allocation and replenishment person, YOU directly influence availability:

- **Allocation logic** determines initial stock placement (right stores get right products)
- **Replenishment triggers** determine when stores get restocked
- **Your MIS** measures stockouts and lost sales, enabling the optimization

---

## Strategic Trade-Offs & Risk Matrices

### Trade-Off 1: Service Level vs. Working Capital
Higher service levels require more safety stock → more working capital. Use differentiated service levels (A/B/C class) to optimize the investment.

### Trade-Off 2: Centralized vs. Distributed Stock
Holding stock centrally (warehouse) is capital-efficient but slow to respond. Holding stock in stores (distributed) is responsive but capital-intensive. Module 4.3 (Replenishment) will explore this deeply.

### Trade-Off 3: Forecast Accuracy vs. Safety Stock
Better forecasts reduce demand variability (σ_d), which reduces safety stock needs. Investing in forecasting can be cheaper than carrying extra safety stock.

---

## Strategic & Operational Pitfalls

1. **Applying the same service level to all products:** C-class products don't deserve 98% service level. The carrying cost far outweighs the lost sales avoided. Use ABC classification.
2. **Not measuring lost sales:** "We don't have stockouts" is a common claim — usually because nobody is tracking them. Build stockout tracking into your MIS first. You'll be surprised.
3. **Equating high stock with high availability:** Sarah's 12 months of stock with 5% lost sales proves this is false. Availability is about RIGHT stock, not MORE stock.
4. **Setting safety stock once and never revisiting:** Demand patterns change. A product that was A-class last season might be B-class this season. Review and adjust safety stock quarterly.
5. **Ignoring lead time variability:** The safety stock formula assumes constant lead time. If your vendor sometimes delivers in 6 weeks and sometimes in 10 weeks, that variability must be factored into safety stock.
6. **Treating all stockouts as equal:** A stockout on your #1 selling cushion cover during Diwali week is catastrophic. A stockout on a niche decorative item in January is minor. Weight your stockout tracking by revenue impact.

---

## Case Application & Discussion Questions

1. **Safety Stock Calculation (30 minutes):** Calculate safety stock for these three products:
   - Product A (A-class): Avg weekly demand = 80, Std dev = 20, Lead time = 6 weeks, Target SL = 96%
   - Product B (B-class): Avg weekly demand = 30, Std dev = 10, Lead time = 8 weeks, Target SL = 92%
   - Product C (C-class): Avg weekly demand = 8, Std dev = 5, Lead time = 10 weeks, Target SL = 85%
   For each: calculate safety stock, reorder point, and annual carrying cost (at $200cost per unit, 20% carrying cost).
2. **Lost Sales Estimation (30 minutes):** From your current data, identify 5 products that stocked out in the last month.
   - How many days was each out of stock?
   - What was the ROS before stockout?
   - Estimate the lost sales (units and $)
   - What was the root cause? (Under-buy? Under-allocate? Late delivery?)
3. **Service Level Optimization (45 minutes):** You have a $20 stock budget for 50 SKUs with an average unit cost of $100,daily demand of 5, demand std dev of 2, and lead time of 7 days. Currently, you apply 95% service level uniformly.
   - Classify the 50 SKUs into A (top 10), B (next 15), C (bottom 25)
   - Calculate stock required at 95% uniform vs. differentiated (A=97%, B=92%, C=85%)
   - How much stock investment do you save?
   - What is the estimated increase in lost sales from the lower C-class service level?
   - Is the trade-off worth it?
4. **Availability Dashboard Design (20 minutes):** Design the metrics for an "Availability & Service Level" dashboard:
   - What to track (in-stock rate, stockout count, lost sales estimate, safety stock utilization)
   - At what level (category, sub-category, SKU, store-SKU)
   - What frequency
   - What alerts to automate

---

## Connection to Next Module

Module 3.3 taught you the theory of the availability-investment trade-off: how to calculate safety stock, set differentiated service levels, and measure lost sales. Module 3.4 takes all of Semester 3's concepts and applies them to a real case study: **Sarah's inventory restructuring** — how he took a bloated, unhealthy inventory and transformed it into a lean, high-performing one, achieving better availability with less stock.

**Next Module:** [Module 3.4: Inventory Restructuring](Module-3.4_Inventory-Restructuring.md)

---

## Key Takeaways

1. **100% availability is uneconomical.** The cost of achieving the last few percentage points is exponential. Target 93-95% at the category level through differentiated service levels.
2. **Not all products deserve equal service levels.** A-class products get 95-98%, C-class products get 80-90%. The savings from lower C-class service levels can fund higher A-class service levels.
3. **Safety stock is insurance against uncertainty.** The combined variability formula is σ_combined = √(L × σ_d² + d² × σ_L²). The three levers are: target service level (Z), demand variability (σ), and lead time (L).
4. **Less stock CAN mean better availability** — if you redirect investment from dead stock to fast movers and from over-stocked stores to under-stocked stores.
5. **Lost sales must be measured** — even though they're invisible. Stockout tracking is the most underbuilt capability in most retail MIS systems. Building it gives you a superpower.
6. **The economic answer to "how much stock?"** is: hold stock until the marginal carrying cost equals the marginal benefit of the next sale saved. Everything beyond that point is over-investment.
