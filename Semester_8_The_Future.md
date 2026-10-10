# Module 8.1: Omnichannel Planning — When Channels Blur

**Semester:** 8 — The Future  
**Prerequisites:** Module 7.4 (Building Planning Capability)  
**Estimated Study Time:** 4–5 hours  
**Level:** Advanced

![The Future Roadmap](assets/Retail%20Planning%20University_%20The%20Future%20Roadmap.png)

---

## 1. Executive Brief & Operating Dilemma

**Date:** June 14, 2029  
**Context:** Aura Global Retail Holiday Fulfillment Crisis.  
**The Dilemma:** A customer in New York ordered a premium hand-painted vase on the website. The Order Management System (OMS) found the vase in the central DC, but also saw one sitting in a Grade A retail store in Brooklyn, just 2 miles from the customer. The algorithm prioritized "Proximity" and routed the order to the Brooklyn store as a "Ship-From-Store" (SFS) order. 

The Brooklyn store staff took the vase off a highly visible front-window display, shoved it into a brown box, and shipped it. 
Three things happened: 
1. The window display looked broken, dropping walk-in sales by 15% that week. 
2. The store staff used the wrong packing material, and the vase arrived shattered. 
3. The store incurred $15 in picking labor, destroying the transaction margin. 
The algorithm perfectly optimized distance but destroyed the brand, the product, and the profit. Omnichannel planning requires mathematical guardrails to protect physical retail from digital demand.

---

## 2. Competency Targets (Bloom's Taxonomy)

Upon completing this module, you will be able to:
1. **Architect** Order Routing Heuristics to balance Fulfillment Speed vs. Margin Dilution.
2. **Synthesize** Pooled Safety Stock calculations using the Square Root Law of Inventory.
3. **Formulate** proper E-commerce return rate math to prevent gross demand shortfalls.
4. **Evaluate** the operational threat of Buy Online, Return In-Store (BORIS).

---

## 3. Theoretical Architecture & Mathematical Formulation

### 3.1 The Square Root Law (Pooled Safety Stock)
When you transition from siloed channel warehouses to a single "Endless Aisle" omnichannel pool, your total safety stock requirement plummets. 
**Formula:** `Total Safety Stock = Individual Node Safety Stock × √n`
If 9 regional DCs each need 100 units of safety stock (900 total), pooling them into one virtual network means you only need (100 × √9) = 300 units total. You just freed up 600 units of working capital.

### 3.2 The Return Rate Mathematical Fix
Never multiply to account for returns. If you need 1,000 units of Net Demand, and returns are 30%, (1,000 × 1.30 = 1,300) will result in a shortfall, because 30% of 1,300 is 390 (Net = 910).
**Correct Formula:** `Gross Sales Required = Net Demand / (1 - Return Rate)`
1,000 / (1 - 0.30) = 1,429 units. 

### 3.3 Ship-From-Store (SFS) Protection Levels
To prevent the Brooklyn store disaster, you must code a floor. 
`IF Store SOH <= Display Minimum, THEN SFS Availability = 0.`

---

## 4. Authentic Industry Data Artifacts & Exhibits

### Exhibit A: The Order Routing Waterfall
*How a mature OMS decides where to pull inventory from.*

| Priority | Logic | The Commercial Rationale |
|---|---|---|
| **1. Split Minimization** | Find one node that has all 5 items the customer ordered. | Shipping 5 separate boxes destroys the margin entirely. |
| **2. Markdown Prevention**| Route to the store that has the highest Weeks of Cover (WOC). | It is cheaper to pay high shipping from a distant, overstocked store than to take a 50% markdown on that stock later. |
| **3. DC Margin Priority** | If neither #1 nor #2 applies, route to the central DC. | DC labor costs $3 to pack. Store labor costs $10. Protect the margin. |
| **4. Geographic Proximity** | Only if the DC is out of stock, route to the closest physical store. | Last resort for speed. Requires SFS Protection Levels to be active. |

*Conclusion: Never default to the closest store. Default to the most profitable execution.*

---

## 5. Cross-Functional Tension & Alignment Playbook

### The War Over Store Labor
| Function | Incentive | The Dangerous Bias | The Executive Mitigation |
|---|---|---|---|
| **E-Commerce** | Digital Revenue. | **The Infinite Warehouse.** Treating every physical store as a free fulfillment center, flooding them with SFS orders to boost online conversion. | Implement strict SFS Daily Capacity Caps. (e.g., "Store X can only receive a maximum of 20 SFS orders per day"). |
| **Store Operations** | Walk-in Sales. | **The Rejection Reflex.** Store managers hating SFS because it pulls staff off the floor. They click "Reject Order" in the system, bouncing the order and delaying customer shipping. | Credit the SFS revenue directly to the Store's P&L. If they pack the box, they get the sales target credit. Alignment is instantly achieved. |

---

## 6. Step-by-Step Operational Modeling Lab

**The Scenario:** Liquidating Stranded Inventory via Omnichannel
At season end, you have 500 units of an obsolete cushion scattered across 250 stores (2 units per store). You cannot sell them in-store. Bringing them back to the DC (Reverse Logistics) costs $5 per unit in freight.

**The Execution (The SFS Flip):**
1. Drop the SFS Protection Level to `0` for this specific SKU.
2. Run an aggressive 40% off "Online Flash Sale."
3. The OMS receives the digital orders and routes them exclusively to the stores.
4. The stores ship the dead stock directly to the customer.
*Result: You liquidated the stranded inventory at 60% of retail value without paying the $2,500 reverse logistics freight penalty.*

---

## 7. Post-Mortem: How Retailers Fail

### Autopsy: The BORIS Paralysis
Aura Global Retail launched a new "Buy Online, Return In-Store" (BORIS) policy to drive footfall. 
A customer bought a massive 9x12 wool rug online. They hated it. They drove to the nearest Aura Global Retail store—a tiny Grade C mall kiosk—and returned it. 
The Grade C store did not sell 9x12 rugs. The rug took up 40% of their backroom space. Because the system lacked a BORIS auto-transfer rule, the rug sat there for 6 months, blocking the store from receiving its core replenishment shipments. 
**The Lesson:** If your system allows BORIS, it must have an automated trigger to instantly generate an inter-store transfer to move inappropriate returns out of small stores and back to the DC.

---

## 8. Executive Practicum & C-Suite Memo

### The Simulation
You are the Director of Planning. The E-Commerce Director is demanding that you remove the "Display Minimum Protection Level" for all Tier 1 stores for the final week of Q4, arguing that "we cannot afford to show 'Out of Stock' online when we have physical units sitting in store windows."

**Your Task:** Write a BLUF memo to the E-Commerce Director and the CEO rejecting the demand.

### Grading Rubric
- **Fail:** Refuses purely because "store managers will complain."
- **Pass:** Explains that breaking displays is bad, but doesn't quantify the financial impact.
- **Executive Grade:** Quantifies the destruction of physical conversion. Mathematically proves that the average Walk-In Conversion Rate of a Flagship store drops by 12% when key window displays are stripped. Contrasts the $5,000 of online revenue gained by breaking the displays against the $45,000 of lost physical sales caused by an uninspiring, broken store environment during the highest-traffic week of the year.

---

**Next Module:** [Module 8.2: Sustainability & Circularity](Module-8.2_Sustainability.md)


---

# Module 8.2: Sustainability & Circularity: The New Constraint

**Semester:** 8 — The Future  
**Prerequisites:** Module 5.2 (Sourcing & Lead Time Planning), Module 7.1 (Category Strategy)  
**Estimated Study Time:** 3–5 hours  
**Level:** Advanced

---

## 1. Executive Brief & Operating Dilemma

**Date:** August 5, 2029  
**Context:** Aura Global Retail Margin Audit & Compliance Review.  
**The Dilemma:** A buyer sourced 50,000 units of a synthetic polyester cushion because it boasted a massive 75% Initial Gross Margin. It looked like a brilliant financial move. 

Two years later, the government enacted an Extended Producer Responsibility (EPR) tax on non-biodegradable retail goods, charging $15 per unit for end-of-life disposal. Furthermore, a new corporate carbon tax penalized the massive emissions generated by air-freighting the synthetics.
The $15 EPR fee and the carbon tax instantly wiped out the entire 75% gross margin. The company lost money on every unit sold. 
The buyer thought they were saving money, but they were just deferring a massive environmental liability to the P&L. Sustainability is no longer a marketing exercise; it is a hard mathematical constraint.

---

## 2. Competency Targets (Bloom's Taxonomy)

Upon completing this module, you will be able to:
1. **Synthesize** the True Cost Matrix (Carbon-Adjusted COGS).
2. **Architect** vendor selection using the Green GMROI formula.
3. **Formulate** a Carbon Open-To-Buy (OTB) constraint model.
4. **Evaluate** the reverse logistics capacity required for Circularity (Take-Back) programs.

---

## 3. Theoretical Architecture & Mathematical Formulation

### 3.1 Carbon-Adjusted COGS & Green GMROI
Traditional COGS only measures the factory invoice and freight. 
**Carbon-Adjusted COGS** = `Traditional Landed Cost + (Carbon Footprint in kg × Carbon Tax Rate) + EPR Disposal Fee.`
**Green GMROI** = `Carbon-Adjusted Gross Margin / Average Inventory Cost.` 
This formula mathematically forces planners to favor vendors with clean energy and short lead times, even if their FOB cost is slightly higher.

### 3.2 The Carbon Open-To-Buy (OTB)
You now have two budgets. 
1. Financial OTB: $5 Million. 
2. Carbon OTB: 400,000 kg CO2e. 
If a proposed assortment hits the financial budget but exceeds the carbon budget, you cannot buy it. You must mix-shift the assortment toward low-carbon SKUs (which often have higher unit costs) to balance the equation.

---

## 4. Authentic Industry Data Artifacts & Exhibits

### Exhibit A: The True Cost Matrix
*Why cheap fast-fashion is a financial trap.*

| Metric | Product A: Synthetic Cushion (Fast Fashion) | Product B: Organic Cotton (Sustainable) |
|---|---|---|
| **Retail Price** | $39 | $45 |
| **Traditional COGS** | $9 (77% Margin) | $26 (42% Margin) |
| **Carbon Footprint** | 4.5 kg CO2e | 1.2 kg CO2e |
| **Carbon Tax ($2/kg)** | $9.00 | $2.40 |
| **EPR Disposal Fee** | $15.00 | $2.00 |
| **Carbon-Adjusted COGS**| **$33.00** | **$30.40** |
| **True Gross Margin** | **$6 (15%)** | **$14.60 (32%)** |

*Conclusion: The synthetic product appeared highly profitable under archaic accounting, but is a severe liability under modern ESG constraints.*

---

## 5. Cross-Functional Tension & Alignment Playbook

### The War Over Price Elasticity
| Function | Incentive | The Dangerous Bias | The Executive Mitigation |
|---|---|---|---|
| **Merchandising**| Margin & Volume. | **The Price Panic.** Refusing to source sustainable goods because they cost 30% more, believing the customer will absolutely not tolerate a 30% retail price increase. | Cross-Subsidization. Do not pass the entire 30% increase to the sustainable item. Raise the price of high-volume, price-inelastic conventional items by $1 to subsidize the eco-line. |
| **ESG / Marketing**| Brand Equity. | **The Greenwash Demand.** Demanding that 100% of the assortment be organic overnight, completely ignoring the margin collapse and supply chain realities. | Institute the Margin-Impact Framework. Phase the transition over 3 years. Use high-impact sustainable goods as "Pioneer SKUs" (marketing spend) while slowly transitioning the cash-cow core. |

---

## 6. Step-by-Step Operational Modeling Lab

**The Scenario:** Planning Reverse Logistics for Circularity
Aura Global Retail launches a "Take-Back" program for old rugs. Historical sales = 1,000,000 units. Expected Return Yield = 2.5% (25,000 rugs returning over 10 weeks = 2,500 rugs/week).

**The Execution (Capacity Planning):**
A planner must secure DC space *before* the marketing campaign launches.
1. 1 pallet holds 50 rolled rugs.
2. 2,500 rugs / 50 = 50 Pallets of inbound volume per week.
3. Sorting Labor: 5 mins per rug = 12,500 minutes (208 hours / 5 full-time workers).
*If the planner does not secure 50 pallet locations and 5 workers, the DC will paralyze within 48 hours of the campaign launching.*

---

## 7. Post-Mortem: How Retailers Fail

### Autopsy: The Air-Freight Hypocrisy
A brand built its entire identity around "100% Sustainable Organic Cotton." 
During a peak holiday season, their organic core line fell behind schedule at the factory in India. To prevent a stockout in their London stores, the planner authorized an emergency air-freight shipment of 20,000 units. 
Air freight generates approximately 40x the CO2 emissions of ocean freight. 
The emissions from that single flight entirely wiped out the carbon savings of the organic farming process for the entire year. An investigative journalist published the shipping logs. The brand was sued for greenwashing and their stock plummeted. 
**The Lesson:** Sustainability cannot just exist in the Bill of Materials (BOM). It must govern the logistics execution. 

---

## 8. Executive Practicum & C-Suite Memo

### The Simulation
You are the Director of Planning. A massive supply chain delay has put your top-selling sustainable furniture line 4 weeks behind schedule. The Head of Sales is demanding you authorize a $250,000 air-freight charter to get the goods into stores before the Black Friday promotion, arguing that the lost sales will devastate the Q4 target. 

**Your Task:** Write a BLUF memo to the CEO rejecting the air-freight request based on the Carbon OTB.

### Grading Rubric
- **Fail:** Approves the air freight to save the sales target.
- **Pass:** Rejects the air freight to "save the environment" without financial justification.
- **Executive Grade:** Rejects the air freight using integrated Carbon/Financial math. Calculates that the air charter will add 180 Metric Tons of CO2 to the category ledger, violently breaching the corporate Carbon OTB. Models the resulting internal carbon tax penalty, proving that the financial penalty of the emissions (plus the $250k charter cost) is actually greater than the net margin dollars lost by missing the Black Friday window. Recommends shifting the Black Friday promotional budget to a high-inventory, domestically sourced category instead.

---

**Next Module:** [Module 8.3: AI & Machine Learning](Module-8.3_AI-and-ML.md)


---

# Module 8.3: AI & Machine Learning — The End of Naive Forecasting

**Semester:** 8 — The Future  
**Prerequisites:** Module 8.2 (Sustainability & Circularity)  
**Estimated Study Time:** 7-9 hours  
**Level:** Advanced

---

## 1. Executive Brief & Operating Dilemma

**Date:** September 2, 2029  
**Context:** Aura Global Retail New Product Introduction (NPI) Meeting.  
**The Dilemma:** A buyer launched a new premium Blue Ceramic Bowl priced at $50. Because there was no historical data for this exact SKU, the buyer manually mapped it to last year's best-selling Blue Ceramic Bowl as a "Like-for-Like" (LFL) baseline, forecasting 5,000 units of demand. 

The buyer ignored a critical variable: last year's bowl was priced at $20. 
The company bought 5,000 units. They sold 800. The markdown liability was massive. 
The buyer was emotionally attached to the color attribute. A Machine Learning (ML) model, running in parallel, looked at the $50 price elasticity attribute, cross-referenced it with the "Blue" and "Ceramic" attributes across 5 years of historical data, and predicted a demand of exactly 850 units. 
AI will not replace planners. But planners who know how to manage AI will absolutely replace planners who rely on naive manual guessing.

---

## 2. Competency Targets (Bloom's Taxonomy)

Upon completing this module, you will be able to:
1. **Architect** tabular data engineering for Gradient Boosted Decision Trees (XGBoost/LightGBM).
2. **Evaluate** AI model health using WAPE, RMSE, and Bias metrics.
3. **Formulate** Reinforcement Learning / Multi-Armed Bandit structures for markdown optimization.
4. **Synthesize** human override protocols when algorithmic models experience "Drift."

---

## 3. Theoretical Architecture & Mathematical Formulation

### 3.1 Why GBDTs (XGBoost) Dominate Retail
Deep learning (Neural Networks) is excellent for unstructured data (images, text). Retail planning relies on tabular data (rows and columns of POS transactions). **Gradient Boosted Decision Trees (GBDTs)** like XGBoost mathematically dominate tabular data because they handle missing values natively, find non-linear relationships instantly, and crucially, they provide **Explainability** (Feature Importance) so a planner can see *why* the AI made a decision.

### 3.2 Model Evaluation Math (WAPE & Bias)
- **WAPE (Weighted Absolute Percentage Error):** Standard MAPE breaks if actual sales are zero. WAPE fixes this. 
`Formula: Sum(Absolute(Actual - Forecast)) / Sum(Actual)`
- **Bias:** Measures directional error. Is the AI structurally over-forecasting (bloated inventory) or under-forecasting (stockouts)?
`Formula: Sum(Forecast - Actual) / Sum(Actual)`

### 3.3 Multi-Armed Bandit (MAB) Markdowns
Instead of blanket "30% off" sales, MAB algorithms balance **Exploration** (testing 15%, 20%, and 25% discounts in small clusters of stores) and **Exploitation** (instantly shifting the entire network to the 20% discount once the math proves it maximizes the gross margin dollars).

---

## 4. Authentic Industry Data Artifacts & Exhibits

### Exhibit A: Attribute Data Engineering (One-Hot Encoding)
*How the machine reads a product.*

| SKU | Raw Description | Encoded_Color_Blue | Encoded_Material_Cotton | Encoded_Price_Tier |
|---|---|---|---|---|
| A1 | Blue Cotton Shirt ($20) | 1 | 1 | 1 |
| A2 | Red Silk Shirt ($80) | 0 | 0 | 4 |

*Conclusion: The algorithm does not know what "Blue" is. It only understands binary presence (1 or 0) and scales (1 to 4). If the Master Data is tagged incorrectly, the AI's forecast will be catastrophic garbage.*

---

## 5. Cross-Functional Tension & Alignment Playbook

### The War Over Model Trust
| Function | Incentive | The Dangerous Bias | The Executive Mitigation |
|---|---|---|---|
| **Data Science** | Algorithmic Purity. | **The Black Box Defender.** Refusing to let Planners override the AI forecast, even when the Planner knows a viral celebrity event just rendered the historical data irrelevant. | Implement a strict Override Protocol. Planners cannot touch the P50 forecast for the 80% core business. Planners have total override authority on the 20% high-volatility/NPI assortment, provided they log a qualitative reason. |
| **Planning** | Control. | **AI Theater.** Buying a $2 Million forecasting tool, but planners secretly download the output to Excel, change the numbers based on "gut feel," and re-upload it, rendering the AI useless. | Measure the WAPE of the AI against the WAPE of the Human Override. If the AI is consistently more accurate, revoke the planner's manual edit permissions. |

---

## 6. Step-by-Step Operational Modeling Lab

**The Scenario:** Diagnosing Model Drift
You deployed an ML forecasting model in January. It is now October. Macro-inflation has spiked. You pull the error logs for 5 stores for a key SKU.
- Actual Sales: 120, 95, 210, 20, 280 (Total = 725)
- AI Forecast: 150, 80, 200, 50, 300 (Total = 780)

**The Execution (WAPE & Bias Check):**
1. **Absolute Errors:** 30, 15, 10, 30, 20. (Total Absolute Error = 105).
2. **WAPE:** 105 / 725 = **14.4%**. (Excellent error rate).
3. **Bias:** (780 - 725) / 725 = **+7.5%**. 
*Conclusion:* While the WAPE is highly accurate, the positive bias indicates the model is structurally beginning to over-forecast, likely because inflation is dampening consumer demand. The planner must flag Data Science to recalibrate the price elasticity weights.

---

## 7. Post-Mortem: How Retailers Fail

### Autopsy: The Weather Ignorance
A traditional rules-based planning system looked at historical data and predicted a massive spike in winter coats for the first week of November in New York, exactly as it had happened for the past 5 years. 
The system shipped 50,000 coats to the stores. 
A modern ML model, running in a Sandbox environment, had ingested real-time API weather data indicating an unseasonable 75-degree heatwave for that exact week in New York. The ML model predicted zero sales. 
The planners ignored the ML model and trusted the traditional system. The 50,000 coats sat untouched, blocking the backrooms. 
**The Lesson:** Demand is multivariate. If your system relies purely on the passage of time (Seasonality) and ignores external context (Weather, Google Trends), it will fail violently.

---

## 8. Executive Practicum & C-Suite Memo

### The Simulation
You are the Director of Planning. The AI allocation engine has just recommended sending 2,000 units of a high-margin, fast-moving product to Store 104 in downtown Chicago based on flawless historical run-rates and demographic matching. 
However, you just received an email from the Store Manager informing you that the city is ripping up the street directly in front of the store starting tomorrow, blocking the main entrance for 30 days. Footfall will drop by 70%.

**Your Task:** Write a BLUF memo to the Data Science lead executing a manual override of the AI allocation.

### Grading Rubric
- **Fail:** Lets the algorithm run because "the math is always right."
- **Pass:** Overrides the algorithm but doesn't explain why to Data Science, polluting the future training data.
- **Executive Grade:** Executes the manual override, cutting the allocation by 70%. Instructs Data Science to manually tag the upcoming 30 days of sales data for Store 104 with a binary `Local_Disruption = 1` flag. Explains that if the AI is allowed to ingest the artificially low sales data without this contextual flag, it will falsely learn that the product is failing in Chicago, permanently crippling next year's forecast.

---

**Next Module:** [Module 8.4: Capstone Simulation](Module-8.4_Capstone-Simulation.md)


---

# Module 8.4: Capstone Simulation

**Semester:** 8 — The Future  
**Prerequisites:** Module 8.3 (AI & Machine Learning)  
**Estimated Study Time:** 10-12 hours  
**Level:** Mastery

---

## 1. Executive Brief & Operating Dilemma

**Date:** Tuesday, 8:30 AM, Week 3 of Q3 (October).  
**Context:** Aura Global Retail Diwali Crisis Management.  
**The Dilemma:** You have just poured your coffee when Sarah, VP of Merchandising, waves you into her office. The whiteboard is covered in red ink. 
The Home & Lifestyle category is bleeding. Gross margin has plummeted from 65% to 36% because stores are choking on a dead inventory line ("Modernist Wood") and marking it down desperately. Finance has hard-frozen your Open-To-Buy (OTB). You cannot spend a single new dollar. 
To make it worse, your primary vendor for Brass Decor just filed for bankruptcy, wiping out 15,000 units of Diwali bestsellers. 

The CEO wants a turnaround plan presented to the board in 48 hours. You must diagnose the trapped cash, execute a strategic vendor pivot without spending new money, tactically rebalance the starving stores, and communicate the brutal reality to an emotional Buying team. In retail, anyone can steer the ship when sales are up 20%. A true planner is forged in the fire of a frozen OTB.

---

## 2. Competency Targets (Bloom's Taxonomy)

Upon completing this simulation, you will have demonstrated the ability to:
1. **Deconstruct** complex ERP data dumps to diagnose trapped working capital and GMROI collapse.
2. **Architect** a strategic vendor pivot and inventory liquidation plan (Strategic Exit).
3. **Formulate** Inter-Store Transfer (IST) and Scarcity Allocation algorithms.
4. **Synthesize** a high-stakes executive communication plan (BLUF) to manage cross-functional panic.

---

## 3. Theoretical Architecture & Mathematical Formulation

*This module tests your mastery of the preceding 35 modules. The core mathematical engines you must deploy include:*
- **GMROI Equation:** `Gross Margin / Average Inventory Cost`
- **Trapped Capital Math:** `Tier Inventory Weighting × Obsolescence %`
- **Scarcity Allocation Logic:** `IF SOH < Demand, THEN Starve Tier C to Feed Tier A.`
- **Margin Erosion Math:** A 60% discount on a 60% IMU product yields a 0% Realized Margin.

---

## 4. Authentic Industry Data Artifacts & Exhibits

### Exhibit A: The Crisis Data Dump (Excerpts)
*You must analyze the full data tables provided in the simulation briefing.*

| Entity | The Reality | The Planner's Constraint |
|---|---|---|
| **Tier C Stores** | Holding 28 Weeks of Cover (WOC). 68% of it is >180 days old. | They are suffocating on dead stock and cannot take new receipts. |
| **Brass Decor** | Best sellers (IMU 73%). Turning at 1-3 WOC. Vendor bankrupt. | You will stock out before Diwali. Lost sales exposure is massive. |
| **Modernist Wood** | "Dogs" (IMU 57%). Turning at 320 WOC. Choking the warehouse. | You must execute a Strategic Exit immediately to recover cash. |

*Conclusion: You have a massive misallocation penalty. Capital is frozen in dead wood in rural stores, while metro flagships are starved of high-margin brass.*

---

## 5. Cross-Functional Tension & Alignment Playbook

### The War Over the Turnaround
| Function | Incentive | The Dangerous Bias | The Executive Mitigation |
|---|---|---|---|
| **Head of Buying** | Ego & Vision. | **The Emotional Defense.** Arguing that the "Modernist Wood" failure is a marketing problem, refusing to authorize the 60% markdown required to clear the warehouse. | The Confrontation Script. Acknowledge the aesthetic vision, but ruthlessly enforce the Opportunity Cost math. "Every square foot holding a dead wood vase is a square foot that cannot hold a turning brass diya. We must kill the wood to fund the future." |

---

## 6. Step-by-Step Operational Modeling Lab

**Phase 1: The Diagnostic (The Bleed)**
- **Task:** Calculate the exact $ value of Trapped Working Capital in Tier C stores.
- *Execution:* Weight the inventory by WOC. Identify that $1.18 Million of obsolete capital is frozen in Tier C.

**Phase 2: The Strategic Pivot**
- **Task:** Find the cash to replace the Brass without breaking the OTB freeze.
- *Execution:* Cancel pending POs for WoodMasters (they are past due and the category is failing). Redirect that exact cash to secure emergency Q4 capacity with GlobalMetals for Brass, and accelerate Loom&Thread Soft Furnishings (30-day lead time) to fill the immediate Diwali gap.

**Phase 3: The Tactical Execution**
- **Task:** Write the Inter-Store Transfer (IST) algorithm.
- *Execution:* `IF (Store_Tier = "C") AND (SKU = "Winner") AND (WOC > 4), THEN Execute Outbound IST to DC. IF (Store_Tier = "A") AND (WOC < 3), THEN Execute Inbound IST.` (Starve the weak, feed the strong).

---

## 7. Post-Mortem: How Retailers Fail

### Autopsy: Averaging the Pain
In a severe shortage of a key Diwali item, a junior planner looked at 800 remaining units and 400 stores. Trying to be "fair" to all Store Managers, they allocated 2 units to every store. 
**The Result:** 2 units is below the Display Minimum. The displays looked broken everywhere. Customers ignored the product. The company suffered a massive stockout on a bestseller, yet simultaneously incurred markdowns because the fragmented units couldn't sell. 
**The Lesson:** In a crisis, fairness is the enemy of profitability. You must cut off the bottom 50% of stores entirely, and consolidate 100% of the scarce inventory into the top Tier A flagships to guarantee full-price sell-through.

---

## 8. Executive Practicum & C-Suite Memo

### The Simulation
You have completed the diagnostic, the pivot, and the tactical allocation logic. You have 45 seconds of Sarah's attention before she walks into the Boardroom. 

**Your Task:** Write the final BLUF email summarizing your turnaround plan.

### Grading Rubric
- **Fail:** A rambling, emotional defense of the planning team's hard work, hiding the bad news at the bottom.
- **Pass:** Provides the numbers, but fails to propose a concrete solution to the OTB freeze.
- **Executive Grade:** 
  *Subject: Q3 Turnaround - Immediate Actions Executed.* 
  *(The Bleed): We have $1.18M of trapped capital suffocating Tier C stores. 
  *(The Pivot): I am cancelling $120k of pending WoodMasters POs to remain cash-neutral. I am redirecting these funds to GlobalMetals to secure the Q4 Brass pipeline, and accelerating Soft Furnishings for the immediate Diwali gap. 
  *(The Tactics): We are pulling all fast-movers from Tier C to consolidate in Tier A flagships, and initiating a 30-50-70% markdown ladder to surgically exit the Modernist Wood category by EOY. 
  *(The Ask): Please approve the WoodMasters PO cancellation so I can execute the ISTs this afternoon.*

---

**[End of Curriculum]**


---

