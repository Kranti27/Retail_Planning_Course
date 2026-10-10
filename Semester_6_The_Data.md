# Module 6.1: Planning Analytics — From Data to Decisions

**Semester:** 6 — The Data  
**Prerequisites:** Module 5.4 (Supply Chain Integration)  
**Estimated Study Time:** 6-7 hours  
**Level:** Core

![The Data](assets/Retail%20Data%20to%20Decisions%20Roadmap.png)

---

## 1. Executive Brief & Operating Dilemma

**Date:** October 12, 2028  
**Context:** Aura Global Retail CEO Monday Trade Meeting.  
**The Dilemma:** The junior analyst proudly presented a beautiful, 40-tab dashboard summarizing 250,000 rows of POS data. They concluded their 15-minute presentation by announcing: "Total sales in the Home category dropped by 15% last week." 

The CEO looked at the analyst and asked: *"Why did they drop, and what exactly are you doing about it today?"* 
The analyst froze. They had built a rear-view mirror. They knew exactly what happened, but they had no idea why, and no recommendation for action. Data without a prescriptive action is just corporate trivia. A planner's job is not to build reports; it is to consume raw data, synthesize it into an insight, and trigger a physical action in the supply chain that protects or generates margin.

---

## 2. Competency Targets (Bloom's Taxonomy)

Upon completing this module, you will be able to:
1. **Diagnose** the root cause of sales anomalies by moving from Descriptive to Diagnostic analytics.
2. **Formulate** prescriptive data queries that intersect Product, Location, Time, and Metric.
3. **Architect** Market Basket Analysis logic (Support, Confidence, Lift).
4. **Synthesize** a Sell-Through vs. Cover Matrix to trigger automated inventory actions.

---

## 3. Theoretical Architecture & Mathematical Formulation

### 3.1 The Analytics Maturity Hierarchy
1. **Descriptive:** What happened? (e.g., Sales dropped 15%).
2. **Diagnostic:** Why did it happen? (e.g., 20 Grade A stores stocked out of our top 5 SKUs).
3. **Predictive:** What will happen? (e.g., At current ROS, 10 more stores will stock out by Friday).
4. **Prescriptive:** What should we do? (e.g., Execute a 500-unit cross-dock push from the DC immediately).

### 3.2 Market Basket Analysis (Lift)
`Lift = Confidence(Item A -> Item B) / Support(Item B)`
If Lift > 1, the items are positively correlated. If Lift = 2.5, a customer buying Item A is 2.5x more likely to buy Item B. You must physically allocate and merchandise these items together.

### 3.3 Data Normalization
You cannot feed an algorithm raw data. If sales spiked 400% in Week 42 because of a 50% discount flash sale, you must mathematically flatten (normalize) that spike back to the baseline average before using Week 42 data to predict Week 44 demand.

---

## 4. Authentic Industry Data Artifacts & Exhibits

### Exhibit A: The Diagnostic Action Matrix
*How planners categorize 10,000 SKUs instantly.*

| Quadrant | Financial Profile | Sell-Through % | Weeks of Cover (WOC) | The Prescriptive Action |
|---|---|---|---|---|
| **Q1: The Winners** | High Velocity, Starving | > 65% | < 4 Weeks | **Chase.** Expedite POs. Increase price if inelastic. Air-freight if margin allows. |
| **Q2: The Cash Cows**| Healthy, Sustained | > 40% | 8 - 12 Weeks | **Maintain.** Run standard automated replenishment. |
| **Q3: The Toxic Dogs**| Dead Capital | < 15% | > 20 Weeks | **Liquidate.** Stop replenishment immediately. Execute deep markdowns or RTV. |
| **Q4: The Phantoms** | Failed Tests | < 10% | < 4 Weeks | **Exit.** Do not reorder. Sell out and drop from assortment. |

*Conclusion: Analytics must instantly map every SKU into one of these four buckets and output a daily exception report telling the planner exactly which lever to pull.*

---

## 5. Cross-Functional Tension & Alignment Playbook

### The War Over Data Purity
| Function | Incentive | The Dangerous Bias | The Executive Mitigation |
|---|---|---|---|
| **Finance** | Audited Precision. | **The Paralysis by Perfection.** Refusing to release sales data until it is 100% reconciled on Wednesday, leaving Planners flying blind on Monday and Tuesday. | Build dual-stream data. Planners use 80% accurate raw POS data on Monday morning for inventory moves. Finance uses 100% accurate data on Wednesday for P&L reporting. Speed beats perfection in supply chain execution. |
| **Merchandising**| Optimism. | **The Promo Amnesia.** Looking at a massive sales spike and demanding higher OTB budgets, conveniently forgetting the spike was driven by a margin-destroying 50% off sale. | Always mandate "Normalized ROS" alongside Raw ROS in all allocation dashboards. |

---

## 6. Step-by-Step Operational Modeling Lab

**The Scenario:** Identifying Phantom Zeros
A C-Grade store shows 0 sales for a core bedsheet for 14 days. The naive replenishment system sees "Zero Demand" and stops ordering the product. 

**The Execution (Data Cleaning):**
You must filter out *Phantom Zeros* (0 sales because of 0 stock) from *True Zeros* (0 sales because customers didn't want it). 
```sql
SELECT Store_ID, SKU_ID, Sales_Units
FROM POS_Data
WHERE NOT (Sales_Units = 0 AND Closing_Stock = 0)
```
By implementing this exact WHERE clause in your data pipeline, you ensure that the Rate of Sale denominator only counts days where the product was physically available to be sold, preventing the replenishment algorithm from spiraling into starvation mode.

---

## 7. Post-Mortem: How Retailers Fail

### Autopsy: The 40-Tab Spreadsheet
A planning department built an incredibly complex descriptive dashboard. It had 40 tabs, tracked 150 different metrics, and took two junior analysts 12 hours every Monday to update and format. 
Because it took so long to build, the planners had zero time left in the week to actually analyze it or make decisions. They were data janitors, not supply chain operators. 
When a major trend shifted, the dashboard beautifully recorded the failure, but no one acted on it. 
**The Lesson:** If an MIS report does not trigger a decision within 5 minutes of opening it, delete it. 

---

## 8. Executive Practicum & C-Suite Memo

### The Simulation
You are the Director of Planning. The CEO is furious that the weekly trade meetings are just a recitation of past sales numbers. The CEO mandates that starting next week, the MIS must be "action-oriented." 

**Your Task:** Write a BLUF memo to the Planning and Data teams mandating the shift from Descriptive to Prescriptive Analytics.

### Grading Rubric
- **Fail:** Adds a "Comments" column to the existing 40-tab dashboard.
- **Pass:** Reduces the dashboard to 5 tabs, but keeps it backward-looking.
- **Executive Grade:** Mandates the destruction of the 40-tab dashboard. Institutes a 1-page "Exception Dashboard" built around the Diagnostic Action Matrix (Exhibit A). Mathematically proves that by only looking at the top 5% of Winners (to chase) and the bottom 10% of Toxic Dogs (to mark down), the planning team will recover 15 hours a week of analytical time and generate $2 Million in margin recovery that was previously buried in the noise.

---

**Next Module:** [Module 6.2: Excel Mastery](Module-6.2_Excel-Mastery.md)


---

# Module 6.2: Excel Mastery for Planning

**Semester:** 6 — The Data  
**Prerequisites:** Module 6.1 (Planning Analytics)  
**Estimated Study Time:** 6-7 hours  
**Level:** Core

---

## 1. Executive Brief & Operating Dilemma

**Date:** November 4, 2028  
**Context:** Aura Global Retail OTB Model Audit.  
**The Dilemma:** A junior planner built a massive Allocation model in Excel. To calculate the baseline stock requirement, they wrote a formula like this: `=SUM(A1:A10) * 1.05`. 

The `1.05` was a hardcoded 5% growth target mandated by the CEO. 
Six months later, the CEO updated the growth target to 8%. The planning team updated all their dashboards, but they forgot about the hidden `1.05` buried deep inside the junior planner's 50,000-row Allocation model. 
For an entire year, the company systematically under-allocated stock by 3%, creating chronic stockouts across the network, costing millions in lost sales. 
Standard Excel usage is dangerous. Planners must use Excel as an Integrated Development Environment (IDE) built on strict architectural principles of variable separation and dynamic referencing.

---

## 2. Competency Targets (Bloom's Taxonomy)

Upon completing this module, you will be able to:
1. **Deconstruct** the 3-Layer Spreadsheet Architecture (Input/Engine/Output).
2. **Formulate** dynamic data pipelines using Power Query and Structured Tables.
3. **Architect** resilient logic using INDEX/MATCH, XLOOKUP, and Dynamic Arrays.
4. **Synthesize** Goal Seek scenarios to optimize markdown depth against margin floors.

---

## 3. Theoretical Architecture & Mathematical Formulation

### 3.1 The 3-Layer IDE Architecture
- **Layer 1: Input (The Database).** Raw data. Zero calculations. Tabular format. 
- **Layer 2: Calc (The Engine).** Where SUMIFS, XLOOKUP, and logic live. Helper columns abound. 
- **Layer 3: Output (The Dashboard).** Executive summaries, Pivot Tables, Conditional Formatting. No complex formulas.

### 3.2 The Death of VLOOKUP
VLOOKUP relies on a hardcoded column index number. If a column is added to the raw data, it silently returns the wrong data. 
*Always use:* `INDEX(Return_Range, MATCH(Lookup_Value, Lookup_Range, 0))` or `XLOOKUP`.

### 3.3 Dynamic Arrays
Use `=FILTER()` and `=UNIQUE()` to instantly segment data without writing 50-line nested IF statements. 

---

## 4. Authentic Industry Data Artifacts & Exhibits

### Exhibit A: The Power Query Pipeline (Unpivoting)
*How to transform messy ERP exports into modeled data.*

**The Raw Export (Pivot Format - Useless for Planning):**
| SKU | Store | Jan_Sales | Feb_Sales | Mar_Sales |
|---|---|---|---|---|
| CUSH-01 | MUM-01 | 150 | 120 | 180 |

**The Power Query Execution:**
1. Connect Excel to the raw CSV folder. 
2. Select the Date columns. Execute "Unpivot Columns". 
3. Output to the Data Model.

**The Transformed Output (Tabular Format - Ready for SUMIFS):**
| SKU | Store | Month | Sales_Qty |
|---|---|---|---|
| CUSH-01 | MUM-01 | Jan_Sales | 150 |
| CUSH-01 | MUM-01 | Feb_Sales | 120 |
| CUSH-01 | MUM-01 | Mar_Sales | 180 |

*Conclusion: Power Query automates this transformation every Monday morning, saving the planner 5 hours of manual data cleaning per week.*

---

## 5. Cross-Functional Tension & Alignment Playbook

### The War Over the Spreadsheet
| Function | Incentive | The Dangerous Bias | The Executive Mitigation |
|---|---|---|---|
| **Merchandising (Execs)** | Speed of reading. | **The 40-Column Blob.** Complaining that the planner's calculation sheet is "too confusing to read." | Strictly enforce the 3-Layer Architecture. Ban executives from looking at the Calc tab. Give them a pristine, 1-page Output Dashboard. |
| **Junior Analysts** | Aesthetics. | **The Merged Cell Catastrophe.** Using 'Merge & Center' to make titles look pretty across columns. | Ban Merged Cells entirely. They instantly break the ability to sort, filter, or drag formulas in a 10,000-row sheet. Use 'Center Across Selection' instead. |

---

## 6. Step-by-Step Operational Modeling Lab

**The Scenario:** Goal Seek for Markdown Optimization
You have a toxic SKU. Current Margin is 60%. You have 1,000 units. You need to clear them. The CFO mandates that the final blended category margin cannot drop below 45%. 
What is the exact maximum discount percentage you can offer on this SKU?

**The Execution (Goal Seek):**
- *Set Cell:* [Cell containing the Projected Final Margin Formula]
- *To Value:* 0.45 (45%)
- *By Changing Cell:* [Cell containing the Discount % input]
*The Goal Seek engine runs thousands of iterations in a second and hardcodes the exact discount (e.g., 27.4%) that clears the stock while perfectly hitting the CFO's margin floor.*

---

## 7. Post-Mortem: How Retailers Fail

### Autopsy: The Hardcoding Sin
A multi-million dollar OTB model crashed the company's Q3 inventory position. 
The post-mortem revealed that a planner had calculated the margin percentage for Store A (50%) and Store B (40%), and then wrote `=AVERAGE(50%, 40%)` to get the total company margin (45%). 
This is mathematically illegal. Store A did $1 Million in sales; Store B did $10,000 in sales. The true weighted margin was 49.9%. 
**The Lesson:** Never average an average. Always calculate aggregate metrics from raw underlying Rupees (Total Profit / Total Sales).

---

## 8. Executive Practicum & C-Suite Memo

### The Simulation
You are the Director of Planning. You have audited the department's Excel files and found rampant use of VLOOKUPs, hardcoded variables inside formulas, and analysts spending 20 hours a week manually copy-pasting data from ERP exports into spreadsheets.

**Your Task:** Write a BLUF memo to the Planning Department mandating a complete overhaul of their Excel architecture.

### Grading Rubric
- **Fail:** Suggests an "Excel Training Course" but institutes no hard structural rules.
- **Pass:** Bans VLOOKUP and Merged Cells, but ignores the manual data entry problem.
- **Executive Grade:** Mandates the immediate adoption of the 3-Layer IDE Architecture. Bans hardcoded variables inside formulas (all variables must live in designated, color-coded 'Input' cells). Mandates the use of Power Query to automate all ERP data extraction, mathematically proving that this will save 2,000 man-hours annually. States that any spreadsheet submitted with a Merged Cell or a VLOOKUP will be immediately rejected without review.

---

**Next Module:** [Module 6.3: Planning Systems](Module-6.3_Planning-Systems.md)


---

# Module 6.3: Planning Systems & Platforms — Beyond Excel

**Semester:** 6 — The Data  
**Prerequisites:** Module 6.2 (Excel Mastery)  
**Estimated Study Time:** 2-3 hours  
**Level:** Core

---

## 1. Executive Brief & Operating Dilemma

**Date:** December 1, 2028  
**Context:** Aura Global Retail Holiday Allocation Crisis.  
**The Dilemma:** The new AI-driven allocation system went live in October. By December, 150 stores were reporting massive overstocks of a seasonal decorative cushion, with units spilling out of the backrooms. 

The VP of Merchandising blamed the system, calling the AI "broken." 
The systems architect audited the logs. The system had correctly calculated that each store needed 2 cartons to meet demand. However, a data entry clerk had incorrectly keyed the Master Data Pack Size in the ERP as "24 units" instead of "12 units." 
The system ordered 2 cartons. The Warehouse Management System (WMS) shipped 2 of the 24-packs. Every store received exactly double the inventory they needed. 
The algorithm was mathematically perfect; the master data was garbage. Systems do not replace planners; they execute the planner's parameters at a scale human math cannot achieve.

---

## 2. Competency Targets (Bloom's Taxonomy)

Upon completing this module, you will be able to:
1. **Evaluate** the flow of data through the retail tech stack (POS -> ERP -> WMS -> Engine).
2. **Architect** parameter overrides to manipulate algorithmic outputs.
3. **Synthesize** Master Data audits to prevent "Garbage In, Garbage Out" (GIGO).
4. **Deconstruct** the difference between modeling (Excel) and execution (Enterprise Systems).

---

## 3. Theoretical Architecture & Mathematical Formulation

### 3.1 The Enterprise Tech Stack
- **POS (Point of Sale):** Captures the transaction.
- **ERP (Enterprise Resource Planning):** The financial ledger and master data repository (e.g., SAP).
- **WMS (Warehouse Management System):** The physical execution engine (picking, packing, shipping).
- **Planning Engine (e.g., Blue Yonder, Increff):** The brain. It pulls from POS and ERP, runs the replenishment math, and sends orders to the WMS.

### 3.2 Parameter Management vs. Coding
Planners do not code algorithms. The system already knows the formula `Model Stock = Lead Time Demand + Safety Stock + Display Minimum`.
A planner's job is to manage the **Parameters**. If a port strike occurs, the planner changes the "Lead Time" parameter from 30 days to 45 days. The system instantly recalculates millions of POs to cover the gap.

---

## 4. Authentic Industry Data Artifacts & Exhibits

### Exhibit A: The Master Data GIGO Audit
*Why the system refused to allocate the best-selling vase.*

| SKU | ERP Field | Value in System | The Reality | The Algorithmic Consequence |
|---|---|---|---|---|
| 9901 | Cost Price | $50.00 | $5.00 | System calculates negative margin and auto-blocks all POs to "protect profitability." |
| 9901 | Status | Discontinued | Active Replenishment | System ignores POS demand entirely. |
| 9901 | Carton Qty | 0 | 12 | System tries to divide allocation by 0, errors out, and skips the SKU in the nightly batch run. |

*Conclusion: 90% of "system errors" are actually Master Data typos. Planners must audit the ERP inputs before blaming the allocation engine.*

---

## 5. Cross-Functional Tension & Alignment Playbook

### The War Over "Black Box" AI
| Function | Incentive | The Dangerous Bias | The Executive Mitigation |
|---|---|---|---|
| **IT / Data Science** | Algorithmic Superiority. | **The Black Box Defender.** Deploying neural networks that output perfect allocation quantities, but cannot explain *why* to a human. | Mandate transparent "Explainability Logs" for all AI models. If a planner cannot explain the math to a buyer, they cannot defend the markdown risk. |
| **Old-School Planners** | Control. | **The Manual Override.** Distrusting the system and manually changing 500 PO quantities based on "gut feel." | Lock system override privileges. Force planners to change the underlying parameter (e.g., Target WOC) instead of manually overriding the final output quantity. |

---

## 6. Step-by-Step Operational Modeling Lab

**The Scenario:** Parameter Manipulation
You manage the Core Bedding category. A massive supply chain disruption occurs, delaying all inbound sea-freight by 3 weeks. 

**The Execution:**
Instead of manually increasing 5,000 Purchase Orders in Excel (which takes a week), you enter the Planning System's Parameter Dashboard. 
1. Select Category: Core Bedding.
2. Select Parameter: Lead Time (Days).
3. Update Value: `Current (60) + 21 = 81 Days`.
*Result: The nightly batch run triggers. The algorithm calculates 21 days of extra Lead Time Demand for every SKU, instantly generating emergency bridge POs to cover the gap.*

---

## 7. Post-Mortem: How Retailers Fail

### Autopsy: The Customization Trap
A major retailer bought an off-the-shelf tier-1 ERP system. Instead of changing their messy, legacy business processes to match the software, they spent $10 Million customizing the software to match their legacy processes. 
Two years later, the software vendor released a critical security update. The retailer couldn't install it because their heavy customizations broke upon updating. They became trapped on an outdated, unsupported version of the ERP, paralyzing their supply chain evolution for a decade.
**The Lesson:** Standardize your business to fit the software; do not customize the software to fit your business.

---

## 8. Executive Practicum & C-Suite Memo

### The Simulation
You are the Director of Planning. The company is evaluating a new Allocation Engine. The vendor is pushing a highly advanced "Black Box" Machine Learning model that claims a 99% accuracy rate but offers zero visibility into how it calculates the replenishment quantity. 

**Your Task:** Write a BLUF memo to the Chief Operating Officer (COO) rejecting the Black Box model and demanding a transparent, parameter-driven system.

### Grading Rubric
- **Fail:** Accepts the Black Box model based purely on the 99% accuracy claim.
- **Pass:** Rejects the model, but relies on emotional arguments about "losing control."
- **Executive Grade:** Rejects the Black Box model using operational logic. Proves that when (not if) a massive anomaly occurs (e.g., a global pandemic, a viral TikTok trend), a Black Box model cannot be manually untangled, whereas a transparent system allows planners to immediately isolate and adjust specific parameters (Lead Time, Service Level). States that without explainable math, the Merchandising team will refuse to accept accountability for markdowns generated by the system.

---

**Next Module:** [Module 6.4: Dashboards & Data Storytelling](Module-6.4_Dashboards-and-Data-Storytelling.md)


---

# Module 6.4: Dashboards & Data Storytelling

**Semester:** 6 — The Data  
**Prerequisites:** Module 6.1 (Analytics), Module 6.2 (Excel), Module 6.3 (Systems)  
**Estimated Study Time:** 4-6 hours  
**Level:** Core

---

## 1. Executive Brief & Operating Dilemma

**Date:** January 15, 2029  
**Context:** Aura Global Retail Q4 Review.  
**The Dilemma:** A junior planner emailed the VP of Merchandising to warn her about a massive inventory problem. The email contained a 15-MB Excel attachment, three pie charts showing regional sales, and the sentence: "Please see attached for Q4 Hardgoods performance metrics."

The VP opened the file, saw 150 columns of unformatted data, closed it, and ignored it. 
Two weeks later, the company suffered a $500,000 markdown hit on unsold festive inventory. The junior planner said, "I warned you in the dashboard!" The VP replied, "A dashboard that doesn't tell me what to do is just a digital museum of past mistakes." 
Your job isn't to report the news; your job is to change the weather. Data without a narrative is just noise.

---

## 2. Competency Targets (Bloom's Taxonomy)

Upon completing this module, you will be able to:
1. **Architect** MIS dashboards strictly adhering to the 3-Second Rule and the Z-Pattern.
2. **Formulate** True ROS logic inside operational dashboards to prevent chronic under-stocking.
3. **Synthesize** raw data into the Situation-Complication-Resolution (SCR) storytelling framework.
4. **Evaluate** the trade-offs between Real-Time intraday data vs. T-1 Batch processing.

---

## 3. Theoretical Architecture & Mathematical Formulation

### 3.1 The 3-Second Rule
A user must look at a dashboard and within 3 seconds understand:
1. What is going right?
2. What is going wrong (variance to plan)?
3. What is the immediate required action?

### 3.2 True ROS Calculation (The Dashboard Engine)
Never use Naive ROS (`Total Sales / Total Days`) in a dashboard. It assumes the item was available to sell every day.
**True ROS = `Total Sales / Days In Stock (DIS)`**
If an item sold 60 units in 30 days, but was stocked out for 15 days, its Naive ROS is 2, but its True ROS is 4. Dashboards running Naive ROS will mathematically starve your stores.

### 3.3 The SCR Data Storytelling Framework
- **Situation:** The baseline, objective fact (Where are we?).
- **Complication:** The variance, threat, or anomaly (Why is the baseline at risk?).
- **Resolution:** The prescriptive action (What are we doing about it right now?).

---

## 4. Authentic Industry Data Artifacts & Exhibits

### Exhibit A: The Tactical Z-Pattern Dashboard Layout
*How to organize information visually for executives.*

| Position | Content | Purpose |
|---|---|---|
| **Top-Left** | Massive Red/Green KPI (e.g., $ Margin Variance) | The Hook. Instantly establishes if we are winning or losing. |
| **Top-Right**| Context Metrics (e.g., Target vs Actual YoY) | Grounding. Provides the scale of the variance. |
| **Middle** | Visual Chart (e.g., Sell-Through vs WOC Scatter Plot) | Diagnosis. Highlights the specific anomalies (the Toxic Dogs). |
| **Bottom** | Actionable Exception Table | Execution. "Here are the 15 exact SKUs causing the variance, click here to execute a Markdown." |

*Conclusion: Never put a massive, unformatted data table at the top of a screen.*

---

## 5. Cross-Functional Tension & Alignment Playbook

### The War Over Real-Time Data
| Function | Incentive | The Dangerous Bias | The Executive Mitigation |
|---|---|---|---|
| **Merchandising**| FOMO (Fear of Missing Out). | **The Intraday Obsession.** Demanding true real-time, minute-by-minute sales dashboards on their phones. | Remind them that retail supply chains move in days, not minutes. You cannot physically move a pallet of sofas from New York to London in 30 minutes. |
| **IT / Tech** | Cost Control. | **The Batch Defender.** Pushing back on real-time dashboards because continuous compute queries cost $50,000/month. | Compromise on T-1 (Yesterday's close of business) batch processing. It is mathematically sufficient for 95% of strategic and tactical retail decisions. |

---

## 6. Step-by-Step Operational Modeling Lab

**The Scenario:** Translating a Data Dump into an SCR Narrative.
*The Raw Data:* "Week 42 total sales $1M. Plan was $1.1M. Furniture is -20%. Decor is +5%. We have 500 sofas sitting at the port waiting for customs. Promotions start next week."

**The Execution (SCR Storytelling):**
- **Situation:** "Total business missed the Week 42 plan by $100k, driven entirely by a 20% deficit in the Furniture category."
- **Complication:** "This deficit is caused by a customs delay trapping 500 core sofas at the port, creating a massive out-of-stock risk ahead of next week's promotional launch."
- **Resolution:** "We have re-allocated the remaining DC buffer stock exclusively to Grade A stores to protect the promotional optics, and authorized a $5,000 expediting fee to clear customs by Thursday."
*Notice how the SCR framework immediately answers the executive's implicit question: "Do I need to worry, and what are you doing about it?"*

---

## 7. Post-Mortem: How Retailers Fail

### Autopsy: The Frankenstein Dashboard
A Planning Director wanted a single "God Dashboard." Every time a buyer or store manager asked a one-off analytical question, the Director told the BI team to add a new chart to the dashboard. 
After two years, the dashboard had 45 charts, 18 filters, and 6 layers of drill-downs. It took 10 minutes to load. 
Because it was so visually overwhelming, the planners stopped using it entirely and went back to downloading raw CSVs into Excel. 
**The Lesson:** Dashboards suffer from scope creep. Audit them quarterly. If a specific chart has not triggered a physical supply chain decision in 90 days, delete it. 

---

## 8. Executive Practicum & C-Suite Memo

### The Simulation
You are the Director of Planning. You just received an email from a junior analyst regarding a highly anticipated seasonal product launch. The email simply states: *"Sales for the new velvet quilts are 40% below forecast. See attached dashboard for details."* 

**Your Task:** Write a BLUF reply to the junior analyst, formally reprimanding the format of their communication, and explicitly instructing them on how to rewrite it using the SCR framework before you forward it to the CEO.

### Grading Rubric
- **Fail:** Opens the dashboard and tries to figure out the problem themselves.
- **Pass:** Tells the analyst to provide more detail, but does not enforce a strict communication structure.
- **Executive Grade:** Refuses to open the dashboard. Rejects the email. Instructs the analyst that they are never to report a baseline "Situation" (sales are down) without simultaneously providing the "Complication" (why) and the "Resolution" (the mathematical markdown or RTV action required to fix it). Demands a 3-sentence SCR rewrite within 15 minutes, enforcing the rule that analysts are paid to make decisions, not just report the news.

---

**Next Module:** [Module 7.1: Category Strategy (Next Semester)](Module-7.1_Category-Strategy.md)


---

