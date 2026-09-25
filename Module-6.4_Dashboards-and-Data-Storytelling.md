# Module 6.4: Dashboards & Data Storytelling

> *"A dashboard that doesn't tell you what to do next is just a digital museum of past mistakes. Your job isn't to report the news; your job is to change the weather."*

**Semester:** 6 — The Data  
**Prerequisites:** Module 6.1 (Planning Analytics), Module 6.2 (Excel Mastery), Module 6.3 (Planning Systems & Platforms)  
**Estimated Study Time:** 4-6 hours  
**Level:** Core  

---

## Executive Summary & Core Dilemma

**How do we transform raw retail data—thousands of SKUs, hundreds of stores, and daily sales transactions—into a clear, actionable narrative that drives immediate decisions, prevents stockouts, and maximizes margin?**

---

## What This Is (First Principles Definition)

A **Management Information System (MIS)** dashboard in retail is a structured visual interface that translates complex underlying data into business intelligence. From first principles, a dashboard is not a data dump; it is a **decision engine**. 

A decision engine takes an input (data), applies business logic (KPIs, thresholds), and outputs a signal (what action to take). 

**Data Storytelling** is the communication framework used to present the output of these dashboards to stakeholders. It relies on structuring information as a narrative (Situation -> Complication -> Resolution) rather than a list of facts.

---

## Why This Exists (The Problem It Solves)

Retail generates overwhelming volumes of data. Consider Aura Global Retail's Home & Lifestyle category:
- 300 active options
- 250 stores
- Daily sales updates
- Weekly intake from 15 different vendor nodes

If a planner attempts to review every row of data, they will suffer from decision paralysis. They might spend 8 hours formatting an Excel sheet and 0 hours deciding what to allocate. 

Dashboards exist to enforce the **3-Second Rule**: A user must be able to look at a dashboard and within 3 seconds understand:
1. What is going right?
2. What is going wrong?
3. What is the immediate required action?

If Sarah, VP of Merchandising, asks, "How is the Hardgoods category performing?", answering "Sales are $250,000" is meaningless. Dashboards contextualize the $250,000 against plan, LY (Last Year), and inventory levels, turning data into information.

---

## How It Connects to the Retail System

As established in Module 0.1 (The Retail Value Chain), Planning is the central nervous system connecting Buying to Supply Chain to Retail Operations.
- **Inputs**: Budgets from Top-Down Planning, Actual Sales from POS, Inventory levels from the WMS (Warehouse Management System).
- **Processing**: The dashboards you build in this module.
- **Outputs**: Allocation instructions (Module 4.2), Replenishment triggers (Module 4.3), Markdown recommendations (Module 2.3).

Without dashboards, the nervous system has data but no reflexes.

---

## The Goal of an MIS (Management Information System)

The ultimate goal of any MIS is to minimize the time between a business event happening (a spike in sales, a delayed shipment) and the business taking corrective action.

### The 3-Second Rule in Practice
Imagine opening a dashboard on Monday morning.

**Bad Example (Fails the 3-second rule):** A screen with a giant data table showing 10,000 rows of SKU-Store level sales, with no color coding, and a pie chart showing sales by region. You have to download it to Excel, run a pivot table, and calculate WOC (Weeks of Cover) just to find out if you need to replenish.

**Good Example (Passes the 3-second rule):**
- Top left (Start of Z-pattern): Big red number: **DC Out of Stock: 15%**
- Middle: Bar chart showing Top 10 SKUs driving the Out of Stock.
- Action Panel: "Create emergency purchase order for Vendor X to cover Top 5 SKUs."

Within 3 seconds, you know the problem (DC OOS is high), the cause (Top 10 SKUs), and the resolution (Raise PO).

---

## The 3 Types of Retail Dashboards

Dashboards must be tailored to the user's timeline and scope of control. We divide them into three categories:

### Operational Dashboards (Daily)
**Goal:** Run today's business. Keep the lights on.
**User:** You (The Planner), Allocation Analysts, Warehouse Managers.
**Time Horizon:** Daily, Real-time (or T-1).
**Key Metrics:** 
- Allocation Fill Rates (Did the warehouse pack what we asked for?)
- Store Out of Stocks (OOS)
- Daily Sales vs Target
- DC Receiving (What arrived yesterday?)

**Worked Example:**
David, Director of Planning, opens the Operational Dashboard at 9:00 AM. 
He sees the DC Fill Rate for the "Brass Diyas" allocation was only 60%. 
He clicks in and sees the warehouse short-picked because the shipment was still in the QC area and not put away. 
*Action:* David immediately calls the Warehouse Manager to prioritize QC for Brass Diyas before the afternoon dispatch.

### Tactical Dashboards (Weekly)
**Goal:** Steer the season. Adjust course.
**User:** David, Buyers.
**Time Horizon:** Weekly (Usually reviewed on "Trading Monday").
**Key Metrics:**
- WSSI (Weekly Sales, Stock & Intake)
- Option Performance (Best/Worst Sellers)
- Category Margin Tracking
- WOC (Weeks of Cover) by Sub-category

**Worked Example:**
David reviews the Tactical Dashboard on Monday. 
The WSSI shows that the "Ceramic Dinnerware" category is tracking at a 4.5 WOC (Target is 8). Sales are +20% to plan, but intake is delayed. 
*Action:* David instructs the team to halt allocation to Grade C stores and ring-fence remaining stock for Grade A stores until the next shipment arrives.

### Strategic Dashboards (Monthly/Quarterly)
**Goal:** Inform long-term strategy and capital allocation.
**User:** Sarah, Directors.
**Time Horizon:** Monthly, Quarterly, Seasonal.
**Key Metrics:**
- Store Grade Mobility (Are Grade B stores becoming Grade A?)
- Vendor Performance (On-time in-full, returns rate)
- Long-term Category Margin (Gross Margin vs Net Margin)
- Markdown Impact

**Worked Example:**
Sarah prepares for his Quarterly Business Review (QBR). 
The Strategic Dashboard shows that Vendor Y (supplying wooden furniture) has an On-Time In-Full (OTIF) rate of 65%, costing the company $150,000 in lost sales due to stockouts. 
*Action:* Sarah uses this data in the vendor negotiation to demand a 5% cost reduction or penalty clause in the next season's contract.

---

## Data Storytelling Framework: Situation, Complication, Resolution (SCR)

Data without a narrative is just noise. Sarah does not have the time to look at an Excel sheet and figure out what it means. When you present data, you must use the SCR framework.

### The Framework
1. **Situation:** The baseline fact. Where are we? (Objective, non-controversial).
2. **Complication:** The problem or opportunity. What changed? Why is the baseline at risk?
3. **Resolution:** The action plan. What are we going to do about it?

### Worked Example: Presenting to Sarah

**Bad Presentation (Data Dump):**
"Hi Sarah. Last week sales were $100,000. Brass category is down 10%. Cushions are up 5%. Our current inventory is 20,000 units. Vendor A shipped 500 units on Monday."
*(Sarah is annoyed. He has to do the mental math to figure out if this is good or bad, and what to do next.)*

**Good Presentation (Data Storytelling with SCR):**
**Situation:** "Overall Home & Lifestyle category is tracking exactly to plan at $100,000 for the week."
**Complication:** "However, within this, Brass Decor sales dropped 10% because we hit a stockout on our top 3 SKUs in Grade A stores. The stock is stuck in transit due to transport strikes."
**Resolution:** "To protect next week's sales, we are air-freighting 500 units of the top 3 SKUs from Vendor X arriving Tuesday, which will cover the Grade A stores until the main shipment arrives."

Notice how the SCR framework immediately answers Sarah's implicit question: "Do I need to worry, and what are you doing about it?"

---

## Designing the "Inventory Health" Dashboard

The Inventory Health dashboard is a Tactical Dashboard used to identify aging stock and prevent margin erosion. Let's design it using the principles from Module 3.1.

### Layout Principles (The Z-Pattern)
In Western cultures, users read screens in a Z-pattern: Top-Left to Top-Right, then Bottom-Left to Bottom-Right.
- **Top-Left:** The most critical, aggregated KPI (e.g., Total Inventory Value at Risk).
- **Top-Right:** Contextual KPIs (e.g., Target vs Actual).
- **Middle/Bottom-Left:** Visuals and charts (e.g., Aging Pyramid).
- **Bottom-Right:** Detailed tables and action buttons.

### Key Components

**1. The Aging Pyramid (Bar Chart)**
A horizontal bar chart showing inventory value split by age buckets.
- 0-30 Days: $50 (Green)
- 31-90 Days: $30 (Yellow)
- 91-180 Days: $10 (Orange)
- 180+ Days: $5 (Red - Terminal)

**2. Sell-Through Rate (STR) vs Weeks of Cover (WOC) Scatter Plot**
- X-Axis: WOC (0 to 20 weeks)
- Y-Axis: Sell-Through Rate (0% to 100%)
- *The "Danger Zone" (Top Right):* High WOC, Low STR (Overstocked, slow moving).
- *The "Opportunity Zone" (Bottom Left):* Low WOC, High STR (Understocked, fast moving).

**Worked Example: Calculating the Dashboard KPIs**

Let's say the dashboard pulls data for SKU 1001 (Mango Wood Salad Bowl).

- **Current Inventory:** 1,200 units
- **Average Weekly Sales (Last 4 Weeks):** 150 units/week
- **Total Intake for Season:** 2,000 units

*Calculations (Backend of the dashboard):*
WOC = Current Inventory / Average Weekly Sales
WOC = 1,200 / 150 = 8 Weeks

Sell-Through % = (Total Intake - Current Inventory) / Total Intake
Sell-Through % = (2,000 - 1,200) / 2,000 = 800 / 2,000 = 40%

The dashboard plots this SKU on the scatter plot at (8, 40%). David sees that an 8 WOC is healthy, and 40% STR halfway through the season is on track.

---

## Designing the "Replenishment & Allocation" Dashboard

This is your operational home as a planner. It tracks how efficiently stock is moving from the DC to the stores.

### Key Components

**1. DC Fill Rate Gauge**
Formula: (Units Dispatched from DC / Units Requested by Allocation) × 100
*Why it matters:* If you allocate 1,000 units and the DC only dispatches 800, your stores will be understocked.

**2. Store Out-of-Stock (OOS) % Tracker**
Formula: (Number of Live SKUs with 0 Inventory in Store / Total Live SKUs Assorted to Store) × 100
*Target:* < 3%.

**3. True ROS vs Naive ROS (Critical Concept)**
Your dashboard must calculate *True ROS* (Rate of Sale) to trigger accurate replenishment.

**Naive ROS:** Total Sales / Total Days in Month
**True ROS:** Total Sales / Days In Stock (DIS)

**Worked Example: True vs Naive ROS**
SKU 2005 (Cotton Bedcover) in the Delhi Flagship Store.
- Monthly Sales: 60 units.
- Total days in month: 30 days.
- Days In Stock (DIS): 15 days (The item was out of stock for 15 days).

Naive ROS = 60 / 30 = 2 units per day.
True ROS = 60 / 15 = 4 units per day.

If your dashboard uses Naive ROS to calculate a 4-week (28 day) replenishment order:
Order = 2 units × 28 days = 56 units.

If your dashboard uses True ROS:
Order = 4 units × 28 days = 112 units.

*Conclusion:* Using Naive ROS in your dashboard will result in chronic under-stocking. The Replenishment Dashboard MUST calculate Days In Stock and compute True ROS.

---

## Executive Perspectives

### How David Uses Dashboards
David is focused on execution and tactics. 
- He uses the **Operational Dashboard** to hold the Supply Chain team accountable. If DC Fill rate drops to 85%, he uses the dashboard screenshot to escalate to the Logistics Head.
- He uses the **Tactical Dashboard** in the weekly trade meeting with you. He is looking for anomalies. He doesn't want to look at the 80% of SKUs that are performing normally; he wants the dashboard to automatically filter and highlight the top 10% (Chasers) and bottom 10% (Dogs).

### How Sarah Uses Dashboards
Sarah manages a $100 Million business. He does not care about a specific store's out-of-stock on a specific cushion cover.
- He uses the **Strategic Dashboard** to defend his budget to the CEO. 
- He looks at Category Margin. If he sees Gross Margin dropping, he will ask David for the SCR data story.
- *What makes Sarah reject a dashboard?* Too much granularity. If you show him a 50-column table of store-level data, he will say, "I can't read this. Tell me what it means."

---

## Strategic Trade-Offs & Risk Matrices

When building or using an MIS, you face distinct trade-offs.

### Detail vs. Clarity
- **Detail:** Showing every metric (Sales, Margin, Discount %, WOC, STR, ROS, Returns) gives a complete picture but violates the 3-second rule.
- **Clarity:** Showing only 3 key metrics drives fast decisions but risks missing nuance.
- **Decision Framework:** Use the "Drill-Down" approach. The top layer of the dashboard should favor Clarity (High-level KPIs). Users should be able to click on a KPI to Drill-Down into the Detail (the underlying SKU-level data).

### Real-time Data vs. Batch Processing (T-1)
- **Real-time:** Updates every minute. 
  - *Pros:* Instant visibility. 
  - *Cons:* Extremely expensive in cloud computing costs. Causes "screen-watching" behavior where planners overreact to hourly fluctuations.
- **Batch (T-1):** Updates once a night at 2:00 AM.
  - *Pros:* Cheap to run. Stable data for the whole day.
  - *Cons:* Cannot react to intra-day emergencies.
- **Decision Framework:** Retail planning rarely requires true real-time data. A T-1 (yesterday's close) batch process is standard and sufficient for 95% of planning tasks.

---

## Strategic & Operational Pitfalls

1. **The "Everything is a Pie Chart" Mistake:** 
   Pie charts are terrible for comparing more than 3 categories because humans are bad at estimating angles.
   *Correction:* Use horizontal bar charts for categorical comparisons (e.g., Sales by Region).
2. **Burying the Lede (No Call to Action):**
   Creating a beautiful dashboard that shows sales are down, but providing no "Action Required" section. A dashboard should generate exceptions (e.g., "Review these 15 SKUs").
3. **Using Red/Green Colors Incorrectly:**
   Making everything green or red creates visual fatigue. Worse, 8% of men are colorblind. 
   *Correction:* Use neutral colors (blues/grays) for standard data, and reserve Red/Green strictly for variance against target.
4. **Ignoring Data Quality:**
   "Garbage In, Garbage Out." If the POS system is offline in 10 stores, the dashboard will show 0 sales and trigger massive allocations.
   *Correction:* Always have a "Data Freshness" indicator on the dashboard (e.g., "Last Synced: 2 AM - 245/250 Stores Reporting").
5. **Frankenstein Dashboards:**
   Adding a new metric every time a manager asks a one-off question, until the dashboard has 40 charts.
   *Correction:* Audit dashboards quarterly and delete any metric that hasn't driven a decision in 3 months.

---

## Case Application & Discussion Questions

### 1. Designing the Layout
Sketch (on paper) a Tactical WSSI Dashboard for the "Hardgoods" category. Follow the Z-pattern. Place your most critical summary metric in the top left, and your actionable SKU-level table in the bottom right. What are the 4 charts you choose to include in the middle?

### 2. Calculating True ROS for the Dashboard
A Aura Global Retail store was open for 30 days in November. A decorative vase sold 120 units total. However, the WMS shows it was out of stock for 10 days during the month. 
Calculate the Naive ROS and the True ROS. If you want to order 4 weeks (28 days) of cover, what is the difference in the order quantity between the two methods?

### 3. The Data Story (SCR)
You notice on your operational dashboard that the new "Festive Table Runner" has a WOC of 2, but the target is 8. The vendor is running 3 weeks late on delivery. Write a 3-sentence SCR (Situation, Complication, Resolution) update to send to David.

### 4. Dashboard Critique
A junior planner presents a new Strategic Dashboard to Sarah. It contains 15 pie charts showing sales mix for every sub-category, updates every 5 minutes in real-time, and uses bright red and green for every slice of the pie. Identify 3 specific flaws in this design based on the module's teachings, and suggest corrections.

---

## Connection to Next Module

In Semester 6, you have learned how to analyze historical data, forecast demand, and build the dashboards that track your decisions. But data alone cannot account for the human element of retail—the promotions, the marketing calendar, and the sudden shift in consumer trends.

In **Module 7.1: Category Strategy**, we will take the baseline data you've mastered and learn how to deliberately manipulate the sales curve to clear old stock and drive seasonal peaks.

**Next Module:** [Module 7.1: Category Strategy](Module-7.1_Category-Strategy.md)

---

## Key Takeaways

1. **Dashboards are decision engines.** A dashboard that fails the 3-second rule is just a data dump.
2. **Tell the SCR story.** Use Situation, Complication, and Resolution to frame your data for leadership.
3. **Use the Z-pattern.** Organize dashboards logically to guide the user from high-level KPIs down to actionable details.
4. **Always use True ROS.** A dashboard that triggers replenishment off Naive ROS will cause chronic stockouts.
5. **Beware the Frankenstein Dashboard.** Edit ruthlessly. If a chart does not drive a decision, remove it.
