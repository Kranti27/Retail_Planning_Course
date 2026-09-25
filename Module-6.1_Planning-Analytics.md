# Module 6.1: Planning Analytics — From Data to Decisions

> *"Data without a decision is just trivia. The job of a retail planner is not to produce reports; it is to consume raw data, synthesize it into actionable insight, and trigger a physical action in the supply chain that protects or generates margin."*

**Semester:** 6 — The Data  
**Prerequisites:** Module 5.4 (Supply Chain Integration)  
**Estimated Study Time:** 6-7 hours  
**Level:** Core

---

## Executive Summary & Core Dilemma

**How do you look at a spreadsheet with 250,000 rows of raw POS (Point of Sale) data and extract the three insights that will change your inventory allocation tomorrow morning?**

For the first five semesters, we discussed the mathematics and theories of retail planning—OTB, Margin Architecture, Service Levels, and Vendor Lead Times. In Semester 6, we shift to the raw execution of these theories. As a planner building MIS dashboards at Aura Global Retail, you are drowning in data: Store grades, daily sales, warehouse stock, transit times, vendor POs.

Analytics is the lens that focuses that chaotic data into a laser beam of decision-making.

---

## The Analytics Hierarchy (First Principles)

Retail analytics is not a monolith. It exists on a maturity curve. Most junior planners are stuck at the bottom; elite planners operate at the top.

### Stage 1: Descriptive Analytics (What happened?)
- **The Data:** "We sold 400 Indigo Bedcovers last week."
- **The Value:** Low. It tells you the past but doesn't tell you why or what to do next. Most basic MIS reports stop here.

### Stage 2: Diagnostic Analytics (Why did it happen?)
- **The Data:** "We sold 400 Indigo Bedcovers, but we could have sold 600. Sales dropped 33% because 15 of our Grade A stores stocked out on Thursday."
- **The Value:** Medium. It identifies the root cause of the failure or success.

### Stage 3: Predictive Analytics (What will happen next?)
- **The Data:** "Based on current ROS and the upcoming Diwali footprint, we will stock out across the entire A and B network in 14 days if we don't intervene."
- **The Value:** High. It forecasts the future state of the business based on the current trajectory.

### Stage 4: Prescriptive Analytics (What should we do about it?)
- **The Data:** "To prevent the stockout in 14 days, execute an immediate inter-store transfer of 100 units from the C-stores to the A-stores, and air-freight 250 units from the vendor, which will cost $1,500 but save $8,500 in lost margin."
- **The Value:** Supreme. The data dictates the exact physical action required to maximize margin.

As you build MIS dashboards, your goal is to automate Stages 1 and 2 so that David, Director of Planning, and Sarah, VP of Merchandising, can spend their time arguing over Stages 3 and 4.

---

## The Core Data Dimensions in Retail

To build any planning model, you must master the intersection of the four core data dimensions. If your data is missing one of these, you cannot make a localized decision.

1. **Product (The 'What'):** Category -> Sub-Category -> Style -> Color -> SKU.
2. **Location (The 'Where'):** Zone -> Cluster -> Store Grade -> Store.
3. **Time (The 'When'):** Year -> Season -> Month -> Week -> Day.
4. **Metric (The 'How Much'):** Units Sold, Value Sold, Cost, Margin %, Stock on Hand.

### The Dimension Intersection
A bad data query asks: "What is the Margin % of Bedcovers?" (Too vague).
A prescriptive data query asks: "What is the Margin % of Indigo Bedcovers (Product) in Grade A Stores (Location) during Week 42 (Time) compared to the Target Margin (Metric)?"

---

## Predictive Analytics in Practice

Predictive analytics is where retail planning transitions from reactive to proactive. You are using historical patterns to model future outcomes with mathematical probability.

### Moving Average Forecasting Recap
The simplest predictive model is the moving average. If a SKU sold 10, 12, 15, and 14 units over the last four weeks, a simple 4-week moving average predicts 12.75 units for next week. 
However, elite planners use **Weighted Moving Averages** to give more recency bias to immediate past weeks.
- Week -1 (Last Week): 40% weight
- Week -2: 30% weight
- Week -3: 20% weight
- Week -4: 10% weight

### Seasonal Decomposition
Time-series data in retail is inherently noisy. A spike in sales could be a true trend, or it could be seasonality. Seasonal decomposition splits historical POS data into three components:
1. **Trend:** The underlying direction (e.g., overall bed linen sales are growing 5% YoY).
2. **Seasonality:** Predictable, recurring fluctuations (e.g., Q4 Diwali peak).
3. **Residual (Noise):** Random, unpredictable variations (e.g., a one-off corporate bulk order).

By isolating the "Trend," planners can forecast base demand without being fooled by seasonal spikes or random noise.

---

## Market Basket Analysis

Market Basket Analysis (MBA) uses association rules to discover which items are frequently bought together. This directly impacts allocation, promotions, and visual merchandising.

The three core metrics of MBA:
1. **Support:** How often do these two items appear together in ALL transactions?
   - Formula: (Transactions containing Item A and Item B) / (Total Transactions)
2. **Confidence:** If a customer buys Item A, how likely are they to buy Item B?
   - Formula: (Transactions containing A and B) / (Transactions containing A)
3. **Lift:** How much more likely is Item B to be bought when Item A is bought, compared to Item B's normal baseline?
   - Formula: Confidence(A -> B) / Support(B)
   - A Lift > 1 means the items are positively correlated.

### Worked Example: Aura Global Retail
Let's analyze 10,000 transactions at Aura Global Retail:
- 1,000 transactions contain "Velvet Cushion Covers" (Item A).
- 800 transactions contain "Knitted Throws" (Item B).
- 200 transactions contain BOTH.

**Calculations:**
- **Support:** 200 / 10,000 = 2% (These two items appear together in 2% of all baskets).
- **Confidence:** 200 / 1,000 = 20% (If a customer buys Velvet Cushion Covers, there is a 20% chance they will buy Knitted Throws).
- **Lift:** 20% / (800 / 10,000) = 0.20 / 0.08 = 2.5

**The Insight:** A Lift of 2.5 is massive. A customer buying the cushion cover is 2.5 times more likely to buy the throw than a random customer. 
**The Prescriptive Action:** You must allocate these two SKUs together. If you send 50 Cushion Covers to the Mumbai Flagship store but 0 Throws, you are leaving guaranteed margin on the table.

---

## The Planner's Diagnostic Toolkit

When sales drop, a planner doesn't panic. They pull out their diagnostic toolkit.

### Tool A: The Sell-Through vs. Cover Matrix
This is the fastest way to diagnose a category. You plot every SKU on a 2x2 matrix based on its Sell-Through % (Module 3.1) and its Weeks of Cover (WOC) (Module 3.2).

- **Quadrant 1 (High Sell-Through, Low Cover):** The Winners. Action: Chase inventory, air-freight replenishment, increase price if inelastic.
- **Quadrant 2 (High Sell-Through, High Cover):** The Cash Cows. Action: Monitor closely. They are selling well and have plenty of stock.
- **Quadrant 3 (Low Sell-Through, High Cover):** The Toxic Dogs. Action: Stop replenishment, initiate markdowns, execute RTV (Return to Vendor).
- **Quadrant 4 (Low Sell-Through, Low Cover):** The Phantoms. Action: Liquidate and exit. Do not reorder.

---

## Data Cleaning & Integrity (The Unsexy Reality)

You cannot run prescriptive analytics on dirty data. Planners spend 30% of their time cleaning data before they ever analyze it.

### Identifying Phantom Zeros vs. True Zeros
If a store shows 0 sales for a product, why?
1. The customer didn't want it (True zero demand).
2. The store was out of stock (Phantom demand).
3. The store had it in the backroom but didn't put it on the shelf (Execution failure).
4. The system showed stock, but it was stolen/damaged (Shrinkage).

If you feed "0 sales" into your replenishment algorithm (Module 4.3) without knowing *why* it's zero, the algorithm will assume True Zero Demand and stop ordering the product. 

**Analytics Rule:** You must cross-reference Sales Data with Stock Data. If Sales = 0 AND Stock = 0, you exclude those days from the ROS calculation.

**SQL/Power Query Snippet for Filtering Phantom Zeros:**
```sql
SELECT 
    Store_ID, 
    SKU_ID, 
    Sales_Units
FROM POS_Data
WHERE NOT (Sales_Units = 0 AND Closing_Stock = 0)
```
This simple WHERE clause ensures your ROS denominator only counts days where the product was actually available to be sold.

### Normalizing Promotional Spikes
If sales spike 400% in Week 42 because of a 50% off Diwali promotion, you cannot use Week 42 data to forecast Week 44 demand. You must "smooth" or normalize the data by stripping out the promotional lift.

To normalize:
1. Calculate the baseline average of the 4 weeks prior to the promotion.
2. Replace the anomalous promotion week data with the baseline average.
3. Add a "Promo Flag" column in your dataset (0 or 1) so future forecasting models understand that the historical spike was artificially induced.

---

## Executive Perspectives

### How Sarah Thinks About Analytics
Sarah uses analytics to allocate OTB budget. He looks at GMROI (Gross Margin Return on Investment) by Sub-Category. 
- "Tableware is generating a GMROI of $3.20.Apparel is generating a GMROI of $2.10.I am going to shift $5 Million of OTB budget from Apparel to Tableware next season."
Sarah uses data to justify his strategy to the CEO.

### How David Operates on Analytics
David uses analytics to find the exceptions. He doesn't want to look at 5,000 SKUs that are performing normally. He wants an exception report delivered to his inbox at 8:00 AM every Monday:
- "Show me all SKUs where WOC > 12 AND Sell-Through < 15%." (Action: Markdown).
- "Show me all SKUs in Grade A stores where SOH < Display Minimum." (Action: Replenish).
David manages by exception. Your MIS must highlight the anomalies, not bury them.

---

## Strategic Trade-Offs & Risk Matrices

### Accuracy vs. Speed
You can wait until Wednesday to get perfectly reconciled, audited sales data from finance. Or you can use raw, unaudited POS data on Monday morning. 
**The Planner's Choice:** Speed wins. An 80% accurate decision made on Monday morning is better than a 100% accurate decision made on Wednesday, because by Wednesday, you have lost 3 days of sales. Planners operate in the "good enough" zone.

### Granularity vs. File Size
If you pull sales data at the SKU-Store-Day level for 2 years, your Excel file will be 15 million rows and will crash your computer. If you pull it at the Category-Region-Month level, the file is tiny, but useless for allocation. 
**The Planner's Choice:** Aggregate Time (use Weekly instead of Daily) to keep the file manageable while preserving the SKU-Store granularity needed for allocation.

---

## Strategic & Operational Pitfalls

1. **Analysis Paralysis:** Building a 40-tab spreadsheet that takes 6 hours to update, leaving no time to actually execute the decisions the data suggests.
2. **Confusing Correlation with Causation:** "Sales of umbrellas spike when we put them near the cash wrap." No, sales of umbrellas spike because it's raining outside. Always look for external variables.
3. **Ignoring the Baseline:** Celebrating a 20% sales increase without realizing the entire market category grew by 30%. You didn't win; you lost market share.
4. **Designing for the Analyst, not the Operator:** Building a mathematically brilliant MIS dashboard that the Store Manager doesn't understand. If the operator can't read it in 3 seconds, they won't use it.

---

## Case Application & Discussion Questions

### 1. The Diagnostic Query Execution
A Aura Global Retail core cushion cover saw a 15% drop in chain-wide revenue this week compared to last week. The total sales dropped from 1,200 units to 1,020 units. 
Write the precise SQL pseudo-code or Excel logic steps you would use to filter the POS dataset to check if the drop was caused by stockouts in Grade A stores vs. a genuine drop in customer demand.

### 2. Normalizing Data Calculation
SKU 123 Sales History:
- Week 1: 52 units (Full Price)
- Week 2: 48 units (Full Price)
- Week 3: 50 units (Full Price)
- Week 4: 210 units (50% off Flash Sale)
- Week 5: 15 units (Post-Sale hangover)

Calculate a mathematically defensible ROS estimate for Week 6 allocation. Detail exactly how you treat Week 4 and Week 5, and state your final normalized ROS figure.

### 3. Calculating Lift in Market Basket Analysis
Using the following transaction data for Aura Global Retail:
- Total Transactions: 50,000
- Transactions with Ceramic Vases: 4,000
- Transactions with Artificial Botanicals: 2,500
- Transactions with BOTH: 1,000

Calculate the Support, Confidence, and Lift for the association (Ceramic Vases -> Artificial Botanicals). Based on the Lift value, write a one-sentence recommendation for the visual merchandising team.

---

## Connection to Next Module

We know what data we need (6.1). Now we need the tools to manipulate it. 
In the next module, we will abandon the mouse, dive into keyboard shortcuts, and learn the specific Excel formulas and Power Query techniques that separate a junior analyst from a master retail planner. 

**Next Module:** [Module 6.2: Excel Mastery](Module-6.2_Excel-Mastery.md)

---

## Key Takeaways

1. **Data is useless without action.** The goal is Prescriptive Analytics: data that tells you exactly what to move, mark down, or reorder.
2. **Manage by Exception.** Do not build reports that show everything. Build reports that highlight anomalies (toxic stock, urgent stockouts).
3. **Clean the "Zeros".** A zero sale means nothing until you verify the stock position. Never forecast off a stockout.
4. **Normalize the Noise.** Always strip out promotional spikes and one-off events before using historical data to forecast future demand.
5. **Speed beats perfection.** Retail moves too fast for perfectly audited data. Use the 80% accurate data today rather than the 100% accurate data next week.
6. **Master the Dimensions.** Every query must lock down the Product, Location, Time, and Metric to be actionable.
7. **Leverage Market Basket Analysis.** Understand the Lift between products to ensure associated SKUs are allocated and merchandised together.
