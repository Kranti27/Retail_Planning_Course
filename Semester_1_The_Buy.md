# Module 1.1: Demand Forecasting — The Science of Predicting Sales

**Semester:** 1 — The Buy  
**Prerequisites:** Module 0.2 (Retail Math Essentials), Module 0.3 (Decision Frameworks)  
**Estimated Study Time:** 5–7 hours  
**Level:** Core

![Retail Buying Plan](assets/Retail%20Buying%20Plan%20Infographic.png)

---

## 1. Executive Brief & Operating Dilemma

**Date:** September 3, 2026  
**Context:** Aura Global Retail's Q3 Supply Chain Summit.  
**The Dilemma:** The DC is overflowing with $18M of excess Winter textiles. The CEO demands an explanation. The Planning team pulls the forecast model: they had used a "Naïve Forecast" (Last Year + 10%). Because last year included a massive, one-off post-pandemic spending surge, the algorithm dutifully replicated an anomaly and added 10% on top of it. 

Meanwhile, the new highly-anticipated Ceramics line is stocking out across all Tier A stores because it was forecasted conservatively using a smoothing average that completely ignored the aggressive marketing campaign launched by Merchandising.

An elite planning executive doesn't need a perfect forecast—they need to quantify the uncertainty, understand HOW WRONG the forecast might be, and strip out historical anomalies before committing capital.

---

## 2. Competency Targets (Bloom's Taxonomy)

Upon completing this module, you will be able to:
1. **Deconstruct** unconstrained demand using the Algorithmic Demand Framework (Base + Trend + Seasonality + Noise).
2. **Calculate** and differentiate statistical forecasting models (Moving Average, Exponential Smoothing, Seasonal Indexing).
3. **Measure** forecast accuracy using MAPE (Magnitude) and Bias (Directional toxicity).
4. **Formulate** a judgment-overlaid consensus forecast that aligns mathematical reality with strategic intent.

---

## 3. Theoretical Architecture & Mathematical Formulation

### 3.1 The Algorithmic Demand Framework
`Forecast = Base Demand + Trend + Seasonality + Events + Noise`
Your job is to separate the signal from the stochastic noise. A forecast should never attempt to model random noise.

### 3.2 The Methodologies
*   **Naïve Forecast:** `Actual(LY) × (1 + Growth Rate)`. Flawed but necessary as a baseline.
*   **Moving Average:** Absorbs noise but perpetually lags a true growth trend.
*   **Exponential Smoothing (α):** `Forecast(t+1) = α × Actual(t) + (1 - α) × Forecast(t)`. Adaptive algorithm. High alpha (0.8) chases recent trends; low alpha (0.2) respects historical stability.
*   **Seasonal Index:** `Month Avg / Grand Avg`. Identifies the exact macroeconomic curve of a business (e.g., Q4 index = 1.56).

### 3.3 MAPE vs. BIAS: The Twin Metrics of Risk
*   **MAPE (Mean Absolute Percentage Error):** Measures the *magnitude* of your error. Industry standard is 10-20%.
*   **Bias:** Measures the *direction* of your error. 
    *   *Positive Bias:* Systemically over-forecasting (Destroys Cash & Margin).
    *   *Negative Bias:* Systemically under-forecasting (Destroys Revenue & Market Share).

---

## 4. Authentic Industry Data Artifacts & Exhibits

### Exhibit A: The "Bias Bleed" Dashboard (Q1-Q2 Trailing)
*Why a 10% error is fine, but a +4.4% Bias destroys companies.*

| Month | Forecast ($M) | Actual ($M) | Error (Abs) | Direction (F-A) |
|---|---|---|---|---|
| April | 8.8 | 8.5 | 0.3 | **+0.3** (Overbought) |
| May | 8.2 | 7.8 | 0.4 | **+0.4** (Overbought) |
| June | 7.2 | 7.0 | 0.2 | **+0.2** (Overbought) |
| July | 6.6 | 6.2 | 0.4 | **+0.4** (Overbought) |
| **Totals** | **30.8** | **29.5** | **MAPE: 4.2%** | **BIAS: +4.4%** |

*CFO Note: The planner celebrated a world-class 4.2% MAPE. The CFO fired them because the +4.4% Bias meant they systematically over-bought every single month, locking up $1.3M in trapped working capital that now requires a 40% markdown to liquidate.*

---

## 5. Cross-Functional Tension & Alignment Playbook

### The Agency Problem of Forecasting
Forecasts are heavily influenced by the bonus structures of the people making them.

| Function | Forecast Incentive | The Systemic Bias | The Executive Mitigation |
|---|---|---|---|
| **Merchandising** | Securing large OTB budgets | **Optimism Bias.** Over-forecasts to ensure infinite options. | Require empirical elasticity models to justify "event lifts". |
| **Operations/SCM** | Zero Stockouts | **Hoarding Bias.** Over-forecasts to guarantee warehouse safety stock. | Link supply chain KPIs directly to GMROI, not just in-stock %. |
| **Finance** | Protecting EBITDA | **Conservatism Bias.** Under-forecasts to limit capital exposure. | Measure "Lost Sales" due to under-funding to prove the opportunity cost. |

---

## 6. Step-by-Step Operational Modeling Lab

**The Scenario:** Calculating Unconstrained Demand (Lost Sales)
In Week 8, a flagship ceramic vase completely sold out. If you feed Week 9-12 (Zero Sales) into the algorithm, it will lower next year's forecast, causing another stockout. You must reconstruct the demand.

**Step 1: Identify the True Trailing Velocity**
- Weeks 4-7 Sales: 400, 420, 410, 430. (Average = 415 units/week).

**Step 2: Adjust for Seasonality**
- Week 9-12 has a historical Seasonal Index lift of 1.2x over the Week 4-7 period.
- Projected Unconstrained Demand = 415 × 1.2 = 498 units/week.

**Step 3: Repopulate the Database**
- Overwrite the "Zero" sales in the database with "498" units for the out-of-stock weeks. The algorithm will now forecast accurately for next year.

---

## 7. Post-Mortem: How Retailers Fail

### Autopsy: The Bullwhip Effect
In 2022, a major US home retailer experienced a 5% drop in consumer demand due to weather.
1. **Stores:** Saw a 5% drop, panicked, cut DC orders by 10%.
2. **DC Planners:** Saw a 10% drop, assumed a macroeconomic crash, cut Factory POs by 25%.
3. **Factories:** Slashed production.
4. **The Result:** When the weather normalized in June, demand spiked. The retailer had no stock. They lost 15% market share to a competitor who trusted the long-term Moving Average and ignored the short-term stochastic noise.
**The Lesson:** Disconnected reactions at localized nodes amplify error. Forecasts must govern the whole chain.

---

## 8. Executive Practicum & C-Suite Memo

### The Simulation
You are the Director of Planning. The statistical model forecasts $15.6M for October based purely on the 3-year Seasonal Index.
However, Merchandising has submitted a "Judgmental Override" demanding the forecast be raised to $18.0M (+15%) because they are launching a "highly disruptive, influencer-led collection."

**Your Task:** Write a BLUF memo to the VP of Merchandising either approving or rejecting the $18.0M override. 

### Grading Rubric
- **Fail:** Blindly accepts the $18.0M forecast, submitting to organizational pressure.
- **Pass:** Rejects the $18.0M based purely on "trusting the algorithm," showing inflexibility.
- **Executive Grade:** Approves a compromise of $16.5M. Defends it by capping the judgmental override at +5% (historical benchmark for influencer lifts), and clearly outlines that funding the full $18.0M introduces an unacceptable +15% Positive Bias risk that would destroy Q4 GMROI if the trend fails.

---

**Next Module:** [Module 1.2: Assortment Planning](Module-1.2_Assortment-Planning.md)


---

# Module 1.2: Assortment Planning — Architecting the Range

**Semester:** 1 — The Buy  
**Prerequisites:** Module 1.1 (Demand Forecasting)  
**Estimated Study Time:** 5–7 hours  
**Level:** Core

---

## 1. Executive Brief & Operating Dilemma

**Date:** October 12, 2026  
**Context:** Aura Global Retail's Q3 Category Review.  
**The Dilemma:** The Ceramics division hit its $10M revenue target, but the COO is furious. The division introduced 400 unique SKUs this season. A post-mortem revealed that the top 50 SKUs generated 75% of the revenue but frequently stocked out. The bottom 200 SKUs generated 8% of the revenue, but required 200 unique factory POs, consumed 40% of the warehouse space, and cluttered the store fixtures. 

Merchandising is defending the 400 SKUs as "necessary for brand storytelling." Planning is demanding a ruthless 50% SKU amputation to free up working capital. 

Assortment planning is not about picking beautiful products. It is a zero-sum mathematical game of capital and space allocation. 

---

## 2. Competency Targets (Bloom's Taxonomy)

Upon completing this module, you will be able to:
1. **Calculate** the mathematical trade-off between Assortment Width (Options) and Depth (Units).
2. **Design** a Good/Better/Best (G/B/B) pricing architecture that protects aggregate category margin.
3. **Evaluate** physical space constraints to engineer an Option Density cap.
4. **Execute** a SKU rationalization (ABC Analysis) to amputate the long tail and redirect capital to high-yielding assets.

---

## 3. Theoretical Architecture & Mathematical Formulation

### 3.1 Width vs. Depth (The Iron Law of Assortment)
Given a fixed Open-to-Buy (OTB) budget, Width and Depth are inversely proportional. You cannot increase variety without starving your inventory depth.
`Total Capital Units = Width (Number of Unique Options) × Depth (Units per Option)`

If you have capital for 10,000 units across 100 stores:
- **High Width (100 Options):** 100 units per option = 1 unit per store. (Guaranteed display failure and immediate stockout).
- **High Depth (10 Options):** 1,000 units per option = 10 units per store. (Highly commercial, robust presentation).

### 3.2 The Good / Better / Best (G/B/B) Cascade
A healthy assortment captures entry-level traffic while driving margin through premium tiers. 
- **Good (Entry):** 20% of Options, 35% of Revenue. Traffic driver. Margin: 45%.
- **Better (Core):** 50% of Options, 50% of Revenue. The profit engine. Margin: 55%.
- **Best (Premium):** 30% of Options, 15% of Revenue. Brand halo. Margin: 65%+.

### 3.3 The Physics of Space Constraints
`Max Option Count = (Total Linear Feet of Fixtures) / (Linear Feet per Option)`
If a wall bay holds 10 options, and a store has 5 wall bays for your category, your absolute maximum assortment width is 50 options. Introducing option #51 requires removing an existing option.

---

## 4. Authentic Industry Data Artifacts & Exhibits

### Exhibit A: ABC SKU Productivity Audit (Ceramics Division)
*The mathematical proof of the "Long Tail" disease.*

| SKU Class | Option Count | % of Total Width | Revenue Generated | % of Total Rev | Markdown Liability |
|---|---|---|---|---|---|
| **A-Class** | 40 Options | 10% | $7.5M | 75% | Minimal (Often Out of Stock) |
| **B-Class** | 160 Options | 40% | $1.7M | 17% | Moderate |
| **C-Class** | 200 Options | 50% | $0.8M | 8% | Critical (Trapped Capital) |

*Conclusion: The business is funding 200 styles to capture 8% of sales. The C-Class is destroying enterprise ROIC.*

---

## 5. Cross-Functional Tension & Alignment Playbook

### The Fight Over the Assortment
| Function | Objective | The Dangerous Bias | The Executive Mitigation |
|---|---|---|---|
| **Merchandising** | Trend leadership and visual storytelling. | **The "Peanut Butter" Approach.** Spreading finite capital thinly across too many new ideas. | Enforce a "Critical Minimum Depth" floor. No option can be bought below 4 units per store. |
| **Visual (VM)** | Flawless aesthetic presentation. | **Over-assorting.** Demanding extra styles simply to make the fixtures look full. | Enforce rigid physical fixture caps before the buy season begins. |
| **Planning** | Maximum ROIC and zero markdowns. | **Hyper-Rationalization.** Cutting the assortment so deep the brand looks sterile. | Protect the "Best" tier. Accept lower turn on premium halo items to defend brand equity. |

---

## 6. Step-by-Step Operational Modeling Lab

**The Scenario:** Cascading the G/B/B Budget.
You have a $2M OTB budget (at Cost) for new cushions. The CFO mandates a 55% average IMU. 

**Step 1: Assign Revenue Targets**
- Good (35%): $700K
- Better (50%): $1M
- Best (15%): $300K

**Step 2: Assign Unit Cost Targets to Hit Margin**
- Good Target ASP: $20 (Cost: $10. IMU 50%) -> Need 70,000 Units
- Better Target ASP: $45 (Cost: $20. IMU 55%) -> Need 50,000 Units
- Best Target ASP: $80 (Cost: $28. IMU 65%) -> Need 10,714 Units

**Step 3: Engineer the Width**
You need high volume per option in "Good" and exclusivity in "Best".
- Good: 5 Options (Depth: 14,000 units/option)
- Better: 20 Options (Depth: 2,500 units/option)
- Best: 15 Options (Depth: 714 units/option)

*Result: Merchandising is handed a strict mathematical mandate: Design exactly 40 options to fit these exact cost slots.*

---

## 7. Post-Mortem: How Retailers Fail

### Autopsy: Cannibalization by Choice Overload
In 2019, a national apparel retailer noticed their $40 basic denim was generating $50M annually. Assuming more choice equaled more revenue, they expanded the denim assortment from 4 washes to 12 washes. 
- **The Result:** Total denim revenue stayed completely flat at $50M. 
- **The Damage:** The demand fractured across 12 styles. Because they tripled the width, their inventory depth per style crashed. They stocked out of core sizes in the most popular washes, while the new niche washes sat untouched. Markdown liability soared by 40%.
**The Lesson:** Adding similar options at the same price point rarely scales top-line revenue; it just cannibalizes existing demand and destroys capital efficiency.

---

## 8. Executive Practicum & C-Suite Memo

### The Simulation
You are the Director of Planning. Review **Exhibit A** (The ABC Audit). The COO has given you a mandate to fix the Ceramics division's working capital crisis. Merchandising is fighting you, claiming that cutting the 200 C-Class SKUs will cost the company $800,000 in revenue.

**Your Task:** Write a BLUF memo to the COO authorizing the amputation of the C-Class tail. 

### Grading Rubric
- **Fail:** Agrees with Merchandising to keep the C-Class items to protect the $800k revenue.
- **Pass:** Authorizes the cut, but fails to explain how the company will recover the "lost" $800k.
- **Executive Grade:** Cuts the 200 C-Class options and mathematically proves that redirecting their manufacturing capital into the A-Class options will cure the A-Class stockouts, generating $1.5M in highly profitable, full-margin replacement revenue.

---

**Next Module:** [Module 1.3: Open-To-Buy (OTB)](Module-1.3_OTB.md)


---

# Module 1.3: Open-to-Buy (OTB) — The Financial Spine of Planning

**Semester:** 1 — The Buy  
**Prerequisites:** Module 0.2 (Retail Math), Module 1.1 (Demand Forecasting)  
**Estimated Study Time:** 5–7 hours  
**Level:** Core

---

## 1. Executive Brief & Operating Dilemma

**Date:** November 2, 2026  
**Context:** Aura Global Retail is entering Q3. 
**The Dilemma:** The Merchandising team just identified a massive viral trend in home décor and requested an immediate $3M capital injection to chase the inventory. 
The CFO's response: "Declined. Your division exhausted its entire 6-month capital budget before the season even started. You have zero liquidity."

Merchandising protests that they hit their pre-season sales plan. But they violated the cardinal rule of retail finance: **Never deploy 100% of your capital preemptively.**

OTB is not a spreadsheet. It is the enterprise governance framework that dictates exactly how much capital can be legally committed to inventory in any given month. If you over-buy your OTB, you bankrupt the company's free cash flow.

---

## 2. Competency Targets (Bloom's Taxonomy)

Upon completing this module, you will be able to:
1. **Calculate** the fundamental OTB equation (Sales + Markdowns + EOM - BOM - On Order).
2. **Formulate** a Weekly Sales, Stock, and Intake (WSSI) ledger to govern working capital velocity.
3. **Reconcile** the strategic tension between Top-Down financial mandates and Bottom-Up merchandising models.
4. **Synthesize** a liquidity reserve ("Chase Budget") strategy to capitalize on emerging in-season trends.

---

## 3. Theoretical Architecture & Mathematical Formulation

### 3.1 The Fundamental OTB Equation
OTB is the quantum of capital authorized for procurement of new merchandise within a specific fiscal period.
`OTB = Planned Sales + Planned Markdowns + Planned EOM Stock - BOM (Beginning of Month) Stock - On Order (Pipeline)`

*Translation: What we plan to sell + What we plan to mark down + What we want to end with MINUS What we already have MINUS What is already on a boat.*

### 3.2 The Stock-to-Sales Ratio (SSR)
How do you know what your "Planned EOM Stock" should be? You use the Stock-to-Sales ratio. 
`Required BOM Stock = Planned Monthly Sales × Target SSR`
If October sales are planned at $10M and the SSR is 3.0, you must open October with $30M in inventory. 

### 3.3 The OTB-to-Margin Bridge
OTB is expressed at Retail Value. To know how much actual cash leaves the company treasury, you must convert it to cost.
`OTB at Cost = OTB at Retail × (1 - Target IMU%)`

---

## 4. Authentic Industry Data Artifacts & Exhibits

### Exhibit A: WSSI (Weekly Sales, Stock, & Intake) Variance Report
*The live control panel used by Directors of Planning.*

| Metric ($M) | Plan | Actual | Variance | Executive Diagnosis |
|---|---|---|---|---|
| **Sales** | 10.3 | 9.1 | *(1.2)* | Revenue shortfall. |
| **Markdowns** | 0.2 | 0.4 | *(0.2)* | Margin compression from discounting. |
| **Receipts** | 7.7 | 8.5 | **+0.8** | Unauthorized capital intake. |
| **EOM Stock** | 33.2 | 35.8 | **+2.6** | Severe Working Capital Bloat. |

*Action Required: May's OTB must be immediately slashed by $2.6M to absorb the April bloat, or the division will trigger a liquidity crisis.*

---

## 5. Cross-Functional Tension & Alignment Playbook

### The War Between Top-Down and Bottom-Up
| Function | The Methodology | The Bias | The Reconciliation |
|---|---|---|---|
| **Finance (Top-Down)** | Macro target based on corporate EBITDA goals (e.g., "$50M budget"). | Blind to product-level realities. | The ceiling. |
| **Merchandising (Bottom-Up)** | SKU-level roll-ups (e.g., "Adding up my styles equals $62M"). | Blind to corporate cash constraints. | The floor. |
| **Planning (The Bridge)** | Negotiates the gap. | Must strip out Merchandising's emotional attachment to underperforming styles to fit the $50M ceiling. |

---

## 6. Step-by-Step Operational Modeling Lab

**The Scenario:** Calculating the Monthly OTB.
Calculate the OTB for August.
- August Sales Plan: $9.0M
- August Markdowns: $1.0M
- September Target BOM (August EOM): $38.15M
- August Actual BOM: $27.0M
- Already On-Order (On boats): $3.0M

**Step 1: The Gross Requirement**
Sales ($9M) + Markdowns ($1.0M) + Target EOM ($38.15M) = **$48.15M** Total Capital Required.

**Step 2: The Existing Capital Base**
Actual BOM ($27.0M) + On-Order ($3.0M) = **$30.0M** Total Capital Sourced.

**Step 3: The Net OTB**
$48.15M (Required) - $30.0M (Sourced) = **$18.15M OTB (Retail)**. 

---

## 7. Post-Mortem: How Retailers Fail

### Autopsy: The 100% Pre-Commitment Death Spiral
In 2021, a mid-market fashion brand authorized a $40M Fall OTB. Fearful of supply chain delays, Merchandising committed 100% of the $40M in February. 
In August, the season launched. A new competitor entered the market, and sales immediately fell 20% behind plan. 
Because 100% of the capital was already on cargo ships, the Planner could not throttle receipts. Inventory backed up into the DCs. To clear the bloat, the brand executed a 40% fleet-wide markdown. They wiped out their entire annual EBITDA in one quarter. 
**The Lesson:** Never commit 100% pre-season. Elite planners hold a 15-20% "Chase Budget" (Liquidity Reserve) to throttle risk and chase in-season winners.

---

## 8. Executive Practicum & C-Suite Memo

### The Simulation
You are the Director of Planning. Review **Exhibit A** (The WSSI Variance). Merchandising is demanding that you leave May's OTB intact so they can launch their new Summer capsule collection. Finance is demanding you freeze May's OTB entirely to recover the $2.6M inventory bloat.

**Your Task:** Write a BLUF memo to the Operating Committee resolving the capital crisis.

### Grading Rubric
- **Fail:** Ignores the EOM bloat and fully funds the Summer capsule, driving the company further into a cash crisis.
- **Pass:** Freezes May's OTB completely, destroying the Summer capsule launch and risking future revenue.
- **Executive Grade:** Identifies the $0.8M unauthorized receipt variance as a supply chain compliance failure. Slashes May's OTB by $2.6M to recover the bloat, but surgically funds the Summer capsule using the division's protected 15% Liquidity Reserve, balancing financial discipline with commercial growth.

---

**Next Module:** [Module 1.4: ISQ & Option Planning](Module-1.4_ISQ-and-Option-Planning.md)


---

# Module 1.4: ISQ & Option Planning — Execution at the SKU Level

**Semester:** 1 — The Buy  
**Prerequisites:** Module 1.2 (Assortment Planning), Module 1.3 (OTB)  
**Estimated Study Time:** 7–9 hours  
**Level:** Core

---

## 1. Executive Brief & Operating Dilemma

**Date:** January 15, 2027  
**Context:** Aura Global Retail's Q2 Global Launch Readiness Review.  
**The Dilemma:** The OTB was perfectly managed. The Assortment Plan (Width vs Depth) was mathematically flawless. Yet, the flagship Spring collection is stalled at a factory in Vietnam. 

Why? The Design team fractionalized the capital for a new ceramic vase across 6 different glaze colors to maximize visual impact. This dropped the unit depth per color to 300 units. The factory's Minimum Order Quantity (MOQ) per glaze is 500 units. The factory refuses to start production. The entire global launch is paralyzed because the macroeconomic plan failed at the micro-execution level.

The OTB dictates *how much* capital. Assortment Planning dictates *how many* options. ISQ (Item-Style-Quantity) is the final, brutal translation where abstract strategy hits supply chain reality.

---

## 2. Competency Targets (Bloom's Taxonomy)

Upon completing this module, you will be able to:
1. **Translate** a macroeconomic capital budget into executable SKU-level purchase orders (ISQ).
2. **Calculate** the precise unit depth required to sustain a product across a specific store footprint and lifecycle.
3. **Synchronize** supply chain physics (MOQs, Lead Times) with financial capital commitments.
4. **Formulate** a Vendor Matrix optimization strategy to balance cost efficiency with enterprise risk.

---

## 3. Theoretical Architecture & Mathematical Formulation

### 3.1 What is ISQ?
**I**tem-**S**tyle-**Q**uantity. It is the final operational execution of the buy.
*   **Item:** Cushion Cover
*   **Style:** Indigo Block Print, Navy Colorway, 20x20.
*   **Quantity:** 1,200 units.
*   *Action:* $13,680 PO cut to Global Textiles for Week 12 delivery.

### 3.2 The Depth per Option Equation
How do you know that 1,200 units is the correct quantity? You back into it from the retail reality.
`Required Depth = (Stores × Minimum Visual Presentation) + (Rate of Sale × Lifespan × Stores)`

*Example:* 120 stores. Minimum 2 units on display. Rate of Sale = 0.5 units/week. Lifespan = 16 weeks.
`Depth = (120 × 2) + (0.5 × 16 × 120) = 240 + 960 = 1,200 units.`

### 3.3 The Supply Chain Physics Formula
`Order Execution Date = Required In-Store Date - Transit/QA Buffer - Production Lead Time`
A brilliant ISQ executed a month late is a guaranteed margin write-off.

---

## 4. Authentic Industry Data Artifacts & Exhibits

### Exhibit A: The Executive Buy Plan Authorization
*The final document signed by the VP of Merchandising before capital leaves the enterprise.*

```text
EXECUTIVE BUY PLAN: SS27 — CUSHIONS & COVERS
=====================================================
Capital Commitment (Cost):    $5.29 Million
Unique Option Count:          45
Aggregate Unit Volume:        447,066
Mean Depth per Option:        9,935 units
Target IMU Profile:           62%

SUPPLY CHAIN CONCENTRATION RISK
=====================================================
Global Textiles:      40% of deployed capital ($2.12M) 
Milan Handlooms:    25% ($1.32M)
Milan Fabrics:        20% ($1.06M)
Artisan Collective:   15% ($0.79M)
*Warning: Exceeding 30% concentration with Global Textiles exposes Q2 launch to single-point-of-failure risk.*
```

---

## 5. Cross-Functional Tension & Alignment Playbook

### The Friction of SKU Execution
| Function | Incentive | The ISQ Blind Spot | The Planner's Mitigation |
|---|---|---|---|
| **Design** | Aesthetic variety. Wants 6 colorways per style. | **MOQ Failure.** Ignores factory minimums. | Enforces color consolidation. Forces 2 colorways at 900 units each to clear the 500 unit MOQ. |
| **Sourcing** | Lowest unit cost. Wants massive MOQs and 6-month ocean freight. | **Agility Death.** Traps capital early and destroys the Chase budget. | Maps ocean freight savings against the Holding Cost and Markdown risk of the excess units. |

---

## 6. Step-by-Step Operational Modeling Lab

**The Scenario:** Navigating Supply Chain Friction
You want to buy 350 units of a premium embroidered cushion (Target Retail: $80, Target Cost: $28). 
Your artisan partner (Vendor A) has a strict 500-unit MOQ. 

**Option A: Swallow the MOQ.**
Buy the 500 units. You tie up an extra $4,200 in capital (150 units × $28). If they don't sell, you take a markdown hit.
**Option B: Dilute the Assortment.**
Kill a different planned cushion and combine the capital to buy 500 units of this one.
**Option C: Pivot Vendors.**
Move to Vendor B who accepts a 300-unit MOQ, but charges $32 per unit. This crushes your IMU from 65% to 60%.

**The Planner's Math:** 
The Planner runs the Expected Value (Module 0.3). Taking the 60% IMU with Vendor B is mathematically safer than absorbing 150 units of dead stock at a 65% IMU with Vendor A. The planner pivots vendors.

---

## 7. Post-Mortem: How Retailers Fail

### Autopsy: The Phantom Margin
A buyer negotiated a brilliant 72% IMU on a summer textile collection by consolidating the entire $4M buy with a single mega-factory in China, which required a 120-day lead time.
In April, regional labor strikes shut down the port near the mega-factory. 
Because the brand had 100% vendor concentration, they had no backup supply chain. The product arrived in late July instead of early May. It entirely missed the summer selling window. The 72% IMU was liquidated at 80% off in August outlets. 
**The Lesson:** Margin without supply chain resilience is a phantom metric. Vendor diversification is an insurance policy you pay for with slightly lower IMUs.

---

## 8. Executive Practicum & C-Suite Memo

### The Simulation
You are the Director of Planning. Look at **Exhibit A** (Supply Chain Concentration Risk). Merchandising has allocated 40% of the entire Q2 capital budget to a single vendor (Global Textiles) to secure a 3% discount on unit cost.

**Your Task:** Write a BLUF memo to the VP of Merchandising refusing to sign off on the Buy Plan. 

### Grading Rubric
- **Fail:** Approves the plan to secure the 3% cost savings without addressing the risk.
- **Pass:** Refuses to sign off due to "risk," but fails to provide a quantitative alternative.
- **Executive Grade:** Rejects the Buy Plan. Defends the rejection by calculating that a 3% unit cost savings is mathematically obliterated if a disruption at Global Textiles delays 40% of the season's revenue by even two weeks. Proposes a revised matrix capping Global at 25% and distributing the balance to Milan Handlooms, accepting a slightly lower IMU to buy structural enterprise resilience.

---

**Next Module:** [Module 2.1: P&L Architecture (Pending/Next Semester)](Module-2.1_P-and-L-Architecture.md)


---

