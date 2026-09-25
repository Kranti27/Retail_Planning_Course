# Module 6.3: Planning Systems & Platforms — Beyond Excel

> *"Excel is a brilliant sandbox, but a terrible factory. When you are managing 50,000 SKUs across 300 stores with daily replenishment cycles, relying on a spreadsheet is retail suicide. Systems don't replace planners; they execute the planner's strategy at a scale human math cannot achieve."*

**Semester:** 6 — The Data  
**Prerequisites:** Module 6.2 (Excel Mastery)  
**Estimated Study Time:** 2-3 hours  
**Level:** Core

---

## Executive Summary & Core Dilemma

**When does Excel break, and how do enterprise-grade planning platforms (like SAP, Blue Yonder, or Increff) actually work to manage the retail supply chain at scale?**

As a retail planner, you spend a lot of time in Excel (Module 6.2). But Aura Global Retail does not run its core operations off a laptop spreadsheet. The company uses massive enterprise systems to track inventory, process sales, and generate replenishment orders. Understanding how these systems connect, where data originates, and how to manipulate their parameters is what separates an analyst from a systems architect.

---

## The Limits of Excel (First Principles)

Why do we need enterprise planning systems? 
1. **Concurrency:** Only one person can edit an Excel file safely. A retail system needs to be updated simultaneously by 300 cashiers, 50 warehouse workers, and 20 planners.
2. **Data Volume:** Excel caps at 1.04 million rows. A daily SKU-Store sales feed for Aura Global Retail will exceed that limit in a matter of weeks.
3. **Auditability:** If a junior planner accidentally deletes a row in an allocation spreadsheet, there is no log of who did it or when. Millions of Rupees could be misallocated invisibly.
4. **Integration:** Excel does not natively trigger a warehouse robot to pick a box, nor does it automatically generate a PDF Purchase Order and email it to a vendor.

Excel is for *modeling* (What-If scenarios). Enterprise systems are for *execution* (making it happen).

---

## The Tech Stack: How the Systems Talk

A modern retail tech stack is not one piece of software. It is a linked chain of specialized systems.

### 1. The ERP (Enterprise Resource Planning)
- **Examples:** SAP, Oracle, Microsoft Dynamics.
- **The Role:** The central source of truth for the company's money and inventory.
- **What it does:** It holds the Master Data (Vendor names, SKU numbers, Store addresses). It tracks the financial ledger (Accounts Payable to vendors). It records the absolute physical location of every piece of inventory.

### 2. The POS (Point of Sale)
- **The Role:** The cash register software in the stores.
- **What it does:** It captures the exact moment a customer buys an item, updates the store inventory locally, and sends a transaction record back to the ERP (usually in a nightly batch run or real-time API).

### 3. The WMS (Warehouse Management System)
- **The Role:** The brain of the Distribution Center.
- **What it does:** When the ERP says "Send 50 units of Cushion A to Store X," the WMS figures out exactly which shelf Cushion A is on, directs a worker to pick it, prints the shipping label, and updates the ERP when the truck leaves.

### 4. The Planning Platform (The Planner's Engine)
- **Examples:** Blue Yonder, Increff, o9 Solutions, Oracle Retail.
- **The Role:** This is where *you* live. 
- **What it does:** It pulls historical sales from the POS, pulls current stock levels from the ERP, and applies your mathematical algorithms (Safety Stock, WOC, Service Levels) to generate future purchase orders or daily replenishment recommendations. 

---

## How Planners Interact with Systems

You do not write code for these systems. You manipulate their **Parameters**. 

In Module 4.3 (Replenishment), we discussed the Model Stock formula:
`Model Stock = Lead Time Demand + Safety Stock + Display Minimum`

In an Excel sheet, you type that formula. In an enterprise system like Blue Yonder or Increff, the system already knows the formula. Your job is to tell the system what variables to use.

**Parameter Management Examples:**
- **Lead Time Parameter:** The system currently assumes Vendor A takes 30 days to deliver. You know there is a port strike. You go into the system and change the Lead Time parameter for Vendor A to 45 days. The system instantly recalculates the Lead Time Demand for all 5,000 SKUs from Vendor A and generates larger POs to cover the gap.
- **Display Minimum Parameter:** VM changes the store layout. They say tables can only hold 2 units now, not 4. You mass-update the Display Minimum parameter from 4 to 2 for the 'Decor' sub-category. The system immediately reduces the replenishment trigger levels, leaning out the store inventory.
- **Store Grade Parameter:** A new mall opens next to Store Z, doubling its footfall. You change Store Z's grade in the system from 'C' to 'A'. The system automatically starts pushing deeper allocations of premium assortment to Store Z.

The system is a high-performance race car. The planner is the driver turning the dials.

---

## The Challenge of "Garbage In, Garbage Out" (GIGO)

Enterprise systems are ruthlessly mathematical. They do exactly what the data tells them to do, without human common sense. 

### The Master Data Nightmare
If a data entry clerk creates a new SKU in the ERP and accidentally enters the Cost Price as $50 instead of $5, the ERP accepts it. 
When the Planning System reads that data, it sees a $50 cost item being sold at a $10 Retail Price. 
The system calculates a massive negative margin and automatically blocks all replenishment orders to "protect profitability."
The stores stock out of a best-seller because of one zero typed incorrectly. 

**The Planner's Rule:** 90% of system errors are actually Master Data errors. Always check the raw inputs (Cost, MRP, Pack Size, Lead Time) before blaming the algorithm.

### The Pack Size Disaster
If a vendor changes their carton size from 12 units to 24 units, but no one updates the Master Data in the ERP...
Your allocation system calculates a store needs 15 units. It rounds up to the nearest carton (Module 4.2). It thinks a carton is 12. So it orders 2 cartons (24 units). 
But the WMS physically ships 2 of the *new* cartons (48 units). 
The store is massively overstocked, all because a parameter was out of sync with reality.

---

## Modern Planning: Increff and the Theory of Constraints

Many modern Indian retailers utilize platforms like Increff, which are built heavily on the Theory of Constraints and localized algorithms.

### How Systems Like Increff Think:
1. **True ROS over Naive ROS:** As discussed in Module 6.1, Increff actively filters out "Zero Sales" days that were caused by stockouts, ensuring the system doesn't artificially lower the demand forecast.
2. **Attribute-Based Forecasting:** If a new Red Cotton Kurta is launched, the system doesn't just look for a proxy SKU manually. It automatically looks at historical sales of all things "Red", all things "Cotton", and all things "Kurta", blending those attributes to create a highly accurate day-one forecast.
3. **The Single View of Inventory:** These systems integrate E-commerce and physical stores. If a warehouse has 10 units left, the system decides mathematically whether those 10 units are better placed on the website or shipped to the Delhi flagship store, based on real-time margin yields.

---

## Executive Perspectives

### How David Uses the System (Tactical)
David, Director of Planning, uses the system for **Exception Management**. He logs in and looks at the "Alerts" dashboard. 
- *Alert:* "SKU 9982 requires a WOC of 4, but current DC stock can only provide 2 WOC across the network."
David investigates, realizes the vendor shipment is delayed, and manually overrides the allocation logic to prioritize Grade A stores only, cutting off the C stores entirely to preserve the limited stock.

### How Sarah Uses the System (Strategic)
Sarah, VP of Merchandising, uses the system for **Scenario Modeling**.
- *"What if we increase our target service level on the Core Assortment from 95% to 98%? System, run a simulation."*
The system processes the request against 2 years of historical variance and replies: *"Achieving 98% service level will require $4.2 Million in additional Safety Stock investment across the chain."*
Sarah then decides if the extra sales are worth the $4.2 Million capital tie-up (Module 3.3).

---

## Strategic Trade-Offs & Risk Matrices

### Customization vs. Standardization
When a retailer buys SAP, they often want to customize it to fit their unique, quirky business processes. 
**The Risk:** Heavy customization costs millions of dollars, takes years, and breaks every time the software needs an update. 
**Best Practice:** Change your business processes to match the standard software (Standardization) rather than rewriting the software to match your business.

### Black Box vs. Transparent Math
Some advanced AI planning systems are "Black Boxes." The system says "Send 14 units to Store X," but it cannot explain *why* it chose 14. 
Planners hate this, because if the 14 units don't sell, Sarah blames the planner, and the planner can only say "the AI told me to." 
Retailers must balance the superior accuracy of machine learning models against the planner's need for transparent, explainable math (like the formulas taught in this university).

---

## Strategic & Operational Pitfalls

1. **"The System is Broken":** 99% of the time, the system is executing its math perfectly based on flawed parameters (bad ROS, wrong lead time, incorrect master data). Check your inputs.
2. **Manual Overrides as a Habit:** A planner doesn't trust the system's replenishment recommendation of 10 units, so they manually type in 30 units. They do this for 500 SKUs. They have just destroyed the value of a multi-million dollar software platform and reintroduced human emotional bias into the supply chain.
3. **Ignoring the System Updates:** The software pushes an update that changes how Safety Stock is calculated. The planner doesn't read the release notes, and suddenly their inventory levels spike 20%. Planners must stay educated on their tools.

---

## Case Application & Discussion Questions

### 1. Tracing the Data Flow (20 minutes)
Draw a flowchart of what happens in the tech stack when a customer buys a $30 ceramic vase at a Aura Global Retail store in Mumbai.
Include the POS, ERP, WMS, and Planning Platform. What data moves where, and what system triggers the replenishment order for a replacement vase?

### 2. Master Data Audit (30 minutes)
The system is refusing to allocate a fast-selling cushion cover. 
Given this mock Master Data snapshot, spot the three errors that are causing the system's math to break:
- MRP: $15 - Cost: $16 - Vendor Pack Size: 0
- Status: Discontinued
- Store Display Minimum: 12

### 3. Parameter Adjustment Strategy (20 minutes)
A massive supply chain crisis delays all sea-freight imports by 3 weeks. 
You use an automated replenishment system. 
Which specific parameter (e.g., Target WOC, Display Min, Lead Time, Store Grade) must you go into the system and change immediately? If you change it from 60 days to 81 days, what will the system automatically do to your pending Purchase Orders?

---

## Connection to Next Module

We now understand the data (6.1), how to manipulate it manually in Excel (6.2), and how enterprise systems execute it at scale (6.3). 
But how do we present this massive, complex, algorithmic reality to stakeholders who don't have time to read spreadsheets or system logs? 
In **Module 6.4: Dashboards & Data Storytelling**, we learn the final analytical skill: summarizing chaos into clean, visual, actionable dashboards that force executives to make the right decisions.

**Next Module:** [Module 6.4: Dashboards & Data Storytelling](Module-6.4_Dashboards-and-Data-Storytelling.md)

---

## Key Takeaways

1. **Excel is for modeling; Systems are for execution.** Excel cannot manage concurrent usage, scale, or direct integration with warehouse logistics.
2. **Planners manage parameters, not code.** Your job is to set the dials (Lead Time, Display Min, Service Level) and let the system run the math.
3. **GIGO (Garbage In, Garbage Out).** An enterprise system is only as smart as its Master Data. Fix the inputs before you blame the algorithm.
4. **Manage by exception.** Trust the system to handle the 90% of routine replenishment, so you can spend your time manually managing the 10% of critical exceptions and anomalies.
