# Module 5.2: Sourcing & Lead Time Planning

> *"Time is the only asset we can't buy more of, but we sure pay for it when we waste it. Every day a product sits in transit is a day it isn't generating cash, and every week of lead time is another week we have to predict an unpredictable future."*

**Semester:** 5 — The Chain  
**Prerequisites:** Module 5.1 (Vendor Economics)  
**Estimated Study Time:** 3-5 hours  
**Level:** Core  

---

## Executive Summary & Core Dilemma

**How do we orchestrate time across the supply chain to ensure the right product arrives exactly when the customer is ready to buy it, without tying up excessive working capital in the process?**

---

## What This Is (First Principles Definition)

**Lead Time** is the total elapsed time between recognizing the need for inventory and having that inventory available for sale on the shop floor. 

It is not a single block of time. It is a pipeline of sequential and parallel events. **Sourcing** is the strategic act of selecting where and how products are made, fundamentally dictating the structure of that lead time pipeline. **Lead Time Planning** is the mathematical and operational discipline of managing this pipeline.

At Aura Global Retail, if a customer buys a hand-painted ceramic bowl in Mumbai, the journey of that bowl started months earlier in a kiln in Khurja or a factory elsewhere. Managing the gap between when we decide we need that bowl and when it hits the shelf is Lead Time Planning.

---

## Why This Exists (The Problem It Solves)

Retail is a game of predicting the future. The longer the lead time, the further into the future you must predict.

1.  **The Forecasting Problem:** Forecasting demand 4 weeks out is relatively easy. Forecasting 24 weeks out is practically guesswork. Long lead times force planners to make high-stakes bets on minimal data.
2.  **The Working Capital Trap:** Inventory in transit is inventory you have paid for (often partially or fully) but cannot sell. It is dead money.
3.  **The Seasonality Cliff:** If Diwali diyas arrive three days after Diwali, their value drops by 90% instantly. Timing is not a luxury; it is the entire value proposition.

Lead Time Planning exists to compress the forecasting horizon, minimize tied-up capital, and hit crucial seasonal launch windows with mathematical precision.

---

## How It Connects to the Retail System

Recall the Value Chain from Module 0.1. Sourcing and Lead Time act as the bridge between **Merchandise Planning (The What)** and **Allocation (The Where)**. 

-   Module 1.3 taught us Open-to-Buy (OTB). OTB tells us *how much* to spend. 
-   Sourcing calendars dictate *when* we must commit that OTB.
-   Lead time dictates when that OTB physically turns into inventory (receipts).

If your lead time math is wrong, your OTB will show receipts in October, but the physical goods will arrive in November. Your October sales will crash (no stock), and your November inventory will bloat (double stock).

---

## The Lead Time Pipeline: Deconstructing Time

Lead time is an aggregate metric composed of distinct segments. We must manage each segment.

### The Pipeline Segments

Let's look at a typical PO for hand-carved wooden trays (Hardgoods) from a vendor in Saharanpur to a Aura Global Retail store in Bangalore.

| Segment | Owner | Description | Duration |
| :--- | :--- | :--- | :--- |
| **1. Order Creation & Approval** | Planning/Buying | Finalizing quantities, creating the PO in ERP, getting internal financial approvals. | 1 Week |
| **2. Vendor Acknowledgment & Raw Material** | Vendor | Vendor accepts PO, procures seasoned wood, books labor capacity. | 3 Weeks |
| **3. Production** | Vendor | Carving, polishing, finishing. | 4 Weeks |
| **4. Quality Control (QC) & Packing** | QA Team / Vendor | Aura Global Retail QA inspects the batch. Vendor packs into master cartons. | 1 Week |
| **5. Origin Transit** | Logistics | Truck journey from Saharanpur factory to the central DC in Delhi. | 1 Week |
| **6. DC Receiving & Put-away** | Warehouse | Unloading, GRN (Goods Receipt Note), binning in the warehouse. | 1 Week |
| **7. DC to Store Transit (Allocation)** | Logistics / Stores | Picking from DC, trucking to Bangalore, store receiving, placing on shelf. | 1 Week |

**Total Lead Time = 12 Weeks (84 Days)**

### The Cost of One Extra Week of Lead Time

Lead time is not just time; it is working capital. Let's calculate the financial impact of extending lead time.

**The Scenario:**
-   Sarah, VP of Merchandising, manages a $100 Million Hardgoods category.
-   Average Cost of Goods Sold (COGS) is 40% of Retail ($40 Million).
-   Cost of Capital (WACC - Weighted Average Cost of Capital) is 12% annually.

If the average lead time increases from 12 weeks to 13 weeks, what is the cost?

1.  **Calculate Weekly COGS Flow:**
    $40 Million (Annual COGS) / 52 weeks = $769,200 per week.
    
    *This means every week, roughly $769,000 of inventory enters the pipeline.*

2.  **Calculate Capital Tied Up in 1 Extra Week:**
    An extra week of lead time means one more week's worth of inventory is permanently stuck in the pipeline.
    Capital Tied Up = $769,200.

3.  **Calculate the Interest Cost on that Capital:**
    Annual cost of holding $769,000 = $769,200 × 12% ≈ $92,300 per year.

**Conclusion:** One extra week of lead time across the category burns almost $92,300 in pure interest cost, invisible on the P&L but destroying cash flow. Furthermore, it increases the risk of markdowns due to trend shifts.

---

## Sourcing Calendars (The T-Minus Concept)

Retail planning works backward from the customer. The most critical tool for this is the **T-Minus Calendar** (Time Minus).

### Building the Critical Path

Let's say Diwali falls on **October 24th**.
For a major festival, the product must be on the floor 4 weeks prior to capture early shoppers and build visual impact. 
**Target Floor Date (TFD): September 26th.**

We map backward using our 12-week lead time pipeline.

*   **T-Minus 0 (Sept 26):** Product live on floor.
*   **T-Minus 1 Week (Sept 19):** DC to Store transit (Allocation execution).
*   **T-Minus 2 Weeks (Sept 12):** DC Receiving & Put-away.
*   **T-Minus 3 Weeks (Sept 5):** Origin Transit (Factory to DC).
*   **T-Minus 4 Weeks (Aug 29):** QC & Packing.
*   **T-Minus 8 Weeks (Aug 1):** Production begins.
*   **T-Minus 11 Weeks (July 11):** Vendor procures Raw Material.
*   **T-Minus 12 Weeks (July 4):** PO Creation & Approval Deadline.

If David's team does not issue the PO by **July 4th**, the product will not make the Diwali floor set on time.

### The Impact of a Missed Milestone

If the PO is delayed to July 18th (2 weeks late), the new floor date becomes October 10th. We have lost 2 out of the 4 weeks of peak Diwali selling time. We will likely be left with unsold inventory post-Diwali, which must be marked down by 40% to clear.

**Financial Impact Example:**
-   Planned Buy: 50,000 units of Brass Urli.
-   Retail Price: $50.-   Cost: $20.-   Planned Sales pre-Diwali (4 weeks): 40,000 units.
-   Due to a 2-week delay, we only sell 20,000 units pre-Diwali.
-   Post-Diwali, 20,000 missed units are marked down 40% (New price: $30).

Lost Margin = 20,000 units × ($50- $30) = $400,000.
A two-week delay at the PO stage cost $400,000 in margin.

---

## The Bullwhip Effect in Lead Times

The Bullwhip Effect occurs when small fluctuations in demand at the retail level cause progressively larger fluctuations in orders at the wholesale, distributor, and manufacturer levels.

**How Lead Time Exacerbates the Bullwhip:**

Imagine a steady selling staple item: White Ceramic Mugs. Lead time is 8 weeks.
-   **Week 1:** Sell 100 units. Order 100 units.
-   **Week 2:** A local corporate buys 50 extra mugs for an event. Sales = 150.
-   **The Planner's Panic:** The planner sees a 50% spike. Because lead time is 8 weeks, they worry this is a new trend. If they under-order, they will be out of stock for 2 months. 
-   **The Over-Correction:** They increase the safety stock parameter. They order 150 to replace sales, PLUS an extra 100 to build buffer. Total order = 250 units.
-   **Week 10:** The 250 units arrive. But normal demand has returned to 100 units/week.
-   **Week 11:** The planner realizes they have too much stock. They order 0 units to let the stock burn down.
-   **The Vendor's Pain:** The vendor saw an order of 100, then a massive spike to 250, then a drop to 0. They cannot plan their labor or raw materials, driving up their costs, which they eventually pass back to you.

Long lead times force planners to react violently to small demand signals. Short lead times allow planners to wait and see if a spike is a trend or an anomaly.

---

## Agile vs. Traditional Sourcing

Not all products should be sourced the same way. We must segment sourcing strategies.

### Traditional Sourcing (Long Lead Time, Low Cost)
-   **Product Type:** Core basics, highly stable demand, complex manufacturing (e.g., imported glassware, large furniture).
-   **Lead Time:** 16 - 24 weeks.
-   **Advantage:** Lowest possible unit cost. High margin percentage.
-   **Disadvantage:** Requires massive forecasting accuracy. High working capital tie-up.

### Agile Sourcing (Short Lead Time, Higher Cost)
-   **Product Type:** Fashion/Trend items, highly volatile demand (e.g., seasonal block-printed cushion covers, topical festive decor).
-   **Lead Time:** 4 - 6 weeks. Local vendors.
-   **Advantage:** "Read and React" capability. Buy a small test quantity, see if it sells, chase into winners immediately.
-   **Disadvantage:** Higher unit cost (vendor charges a premium for speed and smaller batch sizes).

### How this changes the Open-to-Buy (OTB)

If Sarah is planning a $10 Million budget for Cushion Covers:
-   **Traditional Approach:** Place POs for $9 Million upfront (90%) to get volume discounts. Keep $1 Million (10%) for reorders.
-   **Agile Approach:** Place POs for $4 Million upfront (40%). Keep $6 Million (60%) in "Open OTB" to chase trends as the season unfolds.

The Agile OTB structure protects the business from markdown risk on wrong trends, but requires a vendor base capable of 4-week turnarounds.

---

## Managing Vendor Delays: Air vs. Sea Freight

A vendor in Vietnam (Lead time: 14 weeks via sea) calls David. Production is delayed by 3 weeks.
The product is a critical summer outdoor furniture set. 

David has two options:
1.  **Accept the delay via Sea Freight:** Product arrives 3 weeks late, missing peak summer sales.
2.  **Upgrade to Air Freight:** Product arrives on time, but shipping cost skyrockets.

We must use math to decide.

**The Data:**
-   Units: 1,000 sets.
-   Retail Price: $50.-   Original Cost (FOB + Sea Freight): $20.-   Original Margin: $30 per unit (60%).
-   Air Freight Premium: An extra $10 per unit.
-   Sales Impact: If delayed 3 weeks, we will miss selling 400 units at full price. Those 400 units will have to be cleared in an end-of-season sale at 30% off.

**Option 1: Sea Freight (Delayed)**
-   Sell 600 units @ full price ($500) = $300,000
-   Sell 400 units @ 30% off ($350) = $140,000
-   Total Revenue = $440,000
-   Total Cost (1,000 × $200) = $200,000
-   **Net Margin = $240,000**

**Option 2: Air Freight (On Time)**
-   Sell 1,000 units @ full price ($500) = $500,000
-   Total Cost (1,000 × ($200+ $125extra freight)) = 1,000 × $325= $325,000
-   **Net Margin = $175,000**

**Decision:** Despite missing sales and taking markdowns, accepting the delay via Sea Freight yields $65,000 *more* total margin than paying for Air Freight. Air freighting bulky items (like furniture) is almost always a margin destroyer. For lightweight fashion, the math often flips.

---

## Executive Perspectives

### How David Operates on Sourcing
David focuses on the **WIP (Work In Progress) Track**. Every Monday, his team reviews a dashboard showing every PO in the pipeline.
He looks for exceptions:
-   *Are raw materials delayed?*
-   *Did a QC fail require a 2-week rework?*
-   *Is a vessel stuck at the port?*
He manages lead time variance. If a vendor is consistently 2 weeks late, David mathematically increases their system lead time from 10 weeks to 12 weeks, forcing the system to trigger orders earlier.

### How Sarah Thinks About Sourcing
Sarah looks at the macro capability of the vendor base.
-   *Aura Global Retail wants to grow Home Decor by 30% next year.*
-   *Do our brass artisans in Moradabad have the physical kiln capacity to increase output by 30%?*
-   *If not, as volume scales, their lead times will blow out from 8 weeks to 16 weeks.*
Sarah must identify these bottlenecks 12 months in advance and either help the vendor invest in capacity or onboard a secondary vendor.

---

## Strategic Trade-Offs & Risk Matrices

### Unit Cost vs. Lead Time (GMROI Analysis)

The eternal debate in sourcing: Do we buy cheap and slow, or expensive and fast? We use GMROI (Gross Margin Return on Investment) to settle this.

**Scenario:** We need to source 10,000 units of a ceramic vase annually.

**Vendor A (China - Slow & Cheap)**
-   Unit Cost: $30-   Lead Time: 16 weeks
-   Because of the long lead time, we must hold 8 weeks of safety stock and order in massive batches (16 weeks of supply at a time).
-   Average Inventory on hand: 12 weeks of supply = approx 2,300 units.
-   Average Inventory Cost: 2,300 × $30= $69,000

**Vendor B (Local India - Fast & Expensive)**
-   Unit Cost: $40-   Lead Time: 4 weeks
-   Because of the short lead time, we only hold 2 weeks of safety stock and order in small batches (4 weeks of supply).
-   Average Inventory on hand: 3 weeks of supply = approx 575 units.
-   Average Inventory Cost: 575 × $40= $23,000

**The Math (Assuming Retail is $100)**

*Vendor A GMROI:*
-   Annual Revenue: 10,000 × $100= $1 Million
-   Annual COGS: 10,000 × $30= $300,000
-   Gross Margin = $700,000
-   GMROI = Gross Margin / Average Inventory Cost = $700,000 / $69,000 = **10.14**

*Vendor B GMROI:*
-   Annual Revenue: 10,000 × $100= $1 Million
-   Annual COGS: 10,000 × $40= $400,000
-   Gross Margin = $600,000
-   GMROI = Gross Margin / Average Inventory Cost = $600,000 / $23,000 = **26.08**

**Conclusion:** Even though Vendor B costs $10more per unit (sacrificing $100,000 in pure gross margin), the capital efficiency is massive. Vendor B generates $26of margin for every $1invested in inventory, compared to Vendor A's $10.For cash-constrained or trend-driven categories, Vendor B is the vastly superior choice.

---

## Strategic & Operational Pitfalls

1.  **Planning Without Buffer Time:** Assuming a 12-week lead time means goods will arrive *exactly* in 12 weeks. Rain delays transport; QA finds defects. Always pad critical launches with 1-2 weeks of buffer.
2.  **Ignoring Holiday Shutdowns:** Chinese New Year shuts down production and shipping for 3-4 weeks. Indian festivals like Diwali severely impact local transport and factory labor availability. Planners who forget to add these weeks into the lead time face massive stockouts.
3.  **Not Communicating Revised Forecasts:** Planners update internal forecasts but fail to tell the vendor. If you know demand is spiking, tell the vendor to secure raw material 3 months out, even if you haven't issued the PO yet.
4.  **Treating Lead Time as Static:** A vendor's lead time is 8 weeks in March, but might be 14 weeks in September when they are swamped with holiday orders. Lead time is dynamic based on factory capacity.
5.  **The "Push it Through" Fallacy:** Believing that yelling at a vendor or logistics provider will magically compress a 4-week production cycle into 2 weeks. Physics and chemistry (drying wood, setting glaze) cannot be yelled at.

---

## Case Application & Discussion Questions

**Exercise 1: Building a T-Minus Calendar**
You are launching a new bedding collection. Target Floor Date (TFD) is August 15th. 
Lead times are: DC to Store (1 week), Receiving (1 week), Transit (2 weeks), QA (1 week), Production (6 weeks), Raw Material (3 weeks). 
Calculate the exact date the PO must be approved. If approval takes 1 week, when must you start building the PO?

**Exercise 2: The Cost of Delay**
You have 100,000 units of a winter quilt (Retail $100,Cost $40) arriving on December 1st instead of November 1st. 
You expect you will lose 30% of your total full-price sales because of this delay, and those units will be sold in January at a 40% discount. 
Calculate the total lost gross margin in $ due to this one-month delay.

**Exercise 3: Air Freight vs. Margin**
A shipment of 50,000 silk table runners is delayed. 
Retail: $30.Original Cost: $12.Air freight will cost an additional $6per unit. 
If you ship by sea, they arrive late and you must discount the entire batch by 20% to clear them. 
Should you air freight or sea freight? Prove it with math.

**Exercise 4: Working Capital Calculation**
Your category generates $60 Million in annual COGS. Your current weighted average lead time is 14 weeks. Your WACC is 10%. 
If you implement an agile sourcing program that reduces average lead time to 10 weeks, how much cash is freed up from working capital, and what is the annual interest savings?

---

## Connection to Next Module

Now that we understand how to manipulate time and structure the sourcing pipeline, we need to decide *how much* to order when we do pull the trigger. In **Module 5.3: Vendor Negotiation**, we will dive into Min/Max levels, Safety Stock formulas, and how to automate the replenishment of core lines once the initial sourcing pipeline is flowing.

**Next Module:** [Module 5.3: Vendor Negotiation](Module-5.3_Vendor-Negotiation.md)

---

## Key Takeaways

1. **Lead Time is Working Capital.** Every week of lead time is a week of capital tied up in inventory that cannot be sold.
2. **Sourcing Calendars (T-Minus) are mandatory.** You must work backward from the Target Floor Date to ensure POs are placed accurately.
3. **The Bullwhip Effect is magnified by lead times.** Shorter lead times allow you to react correctly to demand fluctuations, while longer lead times force you to over-correct and guess.
4. **Different items need different strategies.** Use traditional sourcing (cheap/slow) for core basics and agile sourcing (expensive/fast) for seasonal trend items.
5. **Air freighting bulky items destroys margin.** Always run the math before accepting an air freight premium. Delay markdowns are often cheaper than the air freight itself.
6. **GMROI reveals the true cost of lead times.** A more expensive, local supplier often generates better returns than a cheaper, overseas one due to massive working capital efficiencies.
