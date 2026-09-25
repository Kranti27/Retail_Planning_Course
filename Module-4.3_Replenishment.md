# Module 4.3: Replenishment — Keeping Stores Fed

> *"Allocation is a guess. Replenishment is the truth. The single biggest driver of full-price sales is a highly responsive replenishment engine that feeds the fast-selling stores exactly what they need, exactly when they need it, without starving the warehouse."*

**Semester:** 4 — The Store  
**Prerequisites:** Module 4.1 (Store Grading), Module 4.2 (Allocation), Module 3.3 (Availability)  
**Estimated Study Time:** 6–7 hours  
**Level:** Core — this is the execution engine of inventory management.

---

## Executive Summary & Core Dilemma

**How do you build a mathematical engine that automatically pulls the right stock from the warehouse to the stores based on actual selling velocity, balancing the risk of stockouts against the cost of overstocking?**

In Module 4.2, we *pushed* the initial allocation to stores based on grades and estimates. Now, the stores are open, the products are selling, and the estimates are irrelevant. The customer is voting with their wallet. Replenishment is the process of *pulling* stock from the warehouse (or vendors) to replace what was sold, guided by the rate of sale (ROS) and the target service level. As an MIS and Allocation specialist, this is your domain.

---

## What Replenishment Is (First Principles)

### Push vs. Pull Systems

| Characteristic | Allocation (Push) | Replenishment (Pull) |
|----------------|-------------------|----------------------|
| **Trigger** | Stock arrives at warehouse | Stock sells at the store |
| **Data Basis** | Historical estimates, Store Grades | Actual current Rate of Sale (ROS) |
| **Direction** | Central planning decides where it goes | Store demand pulls it from the center |
| **Risk** | High (guessing where demand will be) | Low (reacting to proven demand) |
| **Objective** | Distribute initial presentation | Maximize availability, prevent stockouts |

If you allocated 10 units of a vase to Store A and 10 to Store B, and A sells 8 in the first week while B sells 0, Replenishment ensures Store A gets 8 more immediately, while Store B gets none. 

### The Core Replenishment Equation

The fundamental goal of replenishment is to bring a store's inventory position back up to a predefined **Model Stock** (or **Target Stock Level**).

**Replenishment Quantity = Model Stock - Current Inventory Position**

Where:
**Current Inventory Position = Stock on Hand (SOH) + Stock in Transit (SIT)**

*Example:* 
- A store's Model Stock for a specific cushion is 15 units.
- They have 4 units on the shelf (SOH).
- There is a box of 6 units currently on a truck heading to them (SIT).
- Current Inventory Position = 4 + 6 = 10 units.
- Replenishment Quantity = 15 - 10 = **5 units**. 

The entire complexity of replenishment lies in calculating the **Model Stock**.

---

## Calculating Model Stock (The Dynamic Target)

Model stock cannot be static. If a product's sales suddenly double because of a festival, a static model stock will guarantee stockouts. Model stock must breathe with demand.

### The Components of Model Stock

**Model Stock = max(Display Minimum, Lead Time Demand + Safety Stock)**

Let's break this down for a Aura Global Retail store in Bangalore.

**1. Lead Time Demand (LTD)**
How much will the store sell *while waiting* for the truck to arrive?
**LTD = Average Daily ROS × Lead Time (Days)**
- If the store sells 2 units/day, and it takes 7 days for the DC to pick, pack, and ship to Bangalore:
- LTD = 2 × 7 = **14 units**.

**2. Safety Stock (SS)**
The buffer against variability (from Module 3.3). What if they suddenly sell 4 a day? What if the truck takes 10 days instead of 7?
- Let's say statistical safety stock for 95% service level = **8 units**.

**3. Display Minimum / Presentation Stock (PS)**
The physical constraint (from Module 4.4). The shelf looks empty if there are fewer than 4 units on it, regardless of sales. Display Minimum acts as a FLOOR.
- PS = **4 units**.

**Total Model Stock = max(4, 14 + 8) = max(4, 22) = 22 units.**

*(Note: If this were a very slow-selling item where LTD + SS = 2, the Model Stock would be max(4, 2) = 4 units to maintain visual presentation).*

Whenever the store's inventory position falls below the Model Stock, the system generates an order to top it back up.

---

## Methods of Replenishment

### Method 1: Min-Max Replenishment (Simple)

Best for: Basic, non-seasonal items (e.g., standard white bedsheets).

- **Min (Reorder Point):** The trigger level. When stock hits this number, order more.
  - $\text{Min} = \max(\text{Display Minimum}, \text{Lead Time Demand} + \text{Safety Stock})$
- **Max (Target Stock):** The ceiling. Order enough to reach this level.
  - $\text{Max} = \text{Min} + \text{Economic Order Quantity (or Pack Size)}$

*Example:* White Bedsheet (Pack size = 10). Min = 12. Max = 32. 
Stock hits 11. System orders 20 units (2 packs) to bring it back to 31 (close to max).

### Method 2: Dynamic Weeks of Cover (WOC) Replenishment (Advanced)

Best for: Seasonal/Fashion items (e.g., festive cushion covers).

Instead of fixed units, the target is defined in TIME. 
- "Keep 4 weeks of cover in the store at all times."
- Target Stock = $\text{Average Weekly ROS} \times 4$.

If ROS is 5 units/week in Week 1, Target Stock = 20.
If ROS jumps to 15 units/week in Week 4 (Diwali approaching), Target Stock dynamically adjusts to 60.

This is what David uses to manage the bi-annual seasonal shifts.

---

## The Rate of Sale (ROS) Calculation Dilemma

The entire replenishment engine relies on an accurate ROS. But calculating ROS is notoriously tricky.

### Problem 1: Stockout Distortion
If a store sold 10 units in the last 4 weeks, ROS = 2.5/week. 
But what if the store was *out of stock* for 2 of those 4 weeks? 
They actually sold 10 units in 2 weeks. True ROS = 5.0/week.
**Rule:** Always calculate ROS based on *days in stock*, not total calendar days.

### Problem 2: The Time Window
- Use 1-week ROS? Too volatile. One big customer purchase skews the data.
- Use 12-week ROS? Too slow. It won't catch a sudden seasonal spike.
**Best Practice:** A weighted 4-week average. 
- (Most Recent Week × 40%) + (Week-2 × 30%) + (Week-3 × 20%) + (Week-4 × 10%).

### Problem 3: The "Zero Sales" Trap
A new product is launched. A C-grade store doesn't sell a single unit in the first 3 weeks. ROS = 0.
If ROS = 0, LTD+SS = 0.
But because Model Stock = max(Display Minimum, LTD+SS), the store will maintain the Display Minimum. When a customer finally buys the only display unit in Week 4, the system replenishes it back to the floor level.

---

## Warehouse Hold Strategy: The Replenishment Fuel

You cannot replenish if the warehouse is empty. 

### The 70/30 Split
When 1,000 units of a new product arrive from the vendor:
- Do NOT allocate 1,000 units to the stores (100% Push).
- Allocate 700 units based on Grade estimates (70% Push).
- Hold 300 units in the DC (30% Hold).

**Why? The Pareto Principle of Store Performance.**
Stores will not sell the product evenly. 20% of the stores will account for 80% of the sales. 
If you pushed 100% of the stock on Day 1, the fast stores would sell out and stay empty, while the slow stores sit on dead stock. 
By holding 30% back, you use the replenishment engine to feed the 300 units *only* to the stores that are actually selling them.

**This is how Sarah achieved "sell-through increased by 5 percentage points".** He stopped pushing stock to dead locations and started holding it back to feed the winners.

---

## Case Study: Aura Global Retail Replenishment Mathematics

**Scenario:** Managing a top-selling Ceramic Dinner Set.
- Store: Delhi Flagship (Grade A+)
- Vendor Pack Size: 4 sets per carton
- DC to Store Lead Time: 5 days
- Review Frequency: Weekly (7 days)
- Total Lead + Review Time = 12 days (1.7 weeks)

**Data (End of Week):**
- Weighted Avg Weekly ROS: 18 units
- Current SOH: 12 units
- SIT: 0 units
- Display Minimum: 6 units

**Step 1: Calculate Target Stock**
- Lead Time Demand = 18 units/week × 1.7 weeks = 30.6 units
- Safety Stock (95% SL, calculated previously) = 10 units
- Model Stock = max(6, 30.6 + 10) = max(6, 40.6) = 40.6 (round to **41**).

**Step 2: Calculate Net Requirement**
- Requirement = Target (41) - Current Position (12 SOH + 0 SIT) = **29 units**.

**Step 3: Apply Pack Size Constraints**
- Requirement is 29. Pack size is 4.
- 29 / 4 = 7.25 cartons.
- Do we round up or down? For an A+ store with high velocity, round up to prevent stockouts.
- Order = 8 cartons = **32 units**.

The system generates a pick ticket for 32 units to be shipped from the DC to the Delhi store.

---

## Executive Perspectives

### How David Operates on Replenishment
David doesn't look at individual store-SKU calculations (there are tens of thousands of them). He manages the *parameters*.
- "Diwali is in 4 weeks. Go into the system and increase the WOC target for all Festive Hardgoods from 4 weeks to 8 weeks."
- "The warehouse is running out of space. Reduce the Safety Stock Z-score on all C-Class items to lean out the replenishment flow."

### How Sarah Views Replenishment
Sarah looks at the financial outcome.
- **Fill Rate:** Of the 10,000 units the replenishment system requested from the warehouse this week, how many did the warehouse actually have in stock to send? If the DC Fill Rate drops below 85%, Sarah knows the initial buy was too small or the vendor deliveries are late. 
- **Lost Sales:** The ultimate metric of a failing replenishment system (Module 3.3).

---

## Strategic Trade-Offs & Risk Matrices

### Trade-Off 1: Pack Size vs. Freight Cost
Shipping loose units (breaking cartons) means you can send exactly 29 units instead of 32. This keeps inventory perfectly lean. However, warehouse labor costs double when they have to break boxes and count loose items, and damages increase in transit. **Decision:** For low-value items, ship full cartons. For high-value items (e.g., $15,000furniture), break the carton.

### Trade-Off 2: Review Frequency vs. Logistics Cost
If you run the replenishment system daily, stores get stock exactly when they need it, allowing them to operate on very lean inventory. But shipping trucks to stores daily destroys your freight budget. If you run it weekly, freight is cheap, but stores need to hold 7 extra days of safety stock. **Decision:** A+ stores get 2-3 deliveries a week. C stores get 1 delivery every two weeks.

---

## Strategic & Operational Pitfalls

1. **Replenishing to a static space limit indefinitely:** A seasonal item has a POG capacity of 10 units. It sells out in a day. The system replenishes 10 units. It sells out again. The system is blindly feeding a fixed physical space rather than recognizing a breakout hit. The planner needs to intervene, expand the physical space allocation (Module 4.4), and let the system pull 50 units.
2. **Ignoring Stock in Transit (SIT):** If Target is 20, SOH is 5, and SIT is 15. If the system ignores SIT, it will order 15 *more* units. The store ends up with 35 units. This creates a "bullwhip effect" of massive overstocking.
3. **Zero-sum warehouse grabbing:** If the DC has 10 units left, and Store A needs 8 while Store B needs 8. A naive system fulfills Store A completely (leaving 2), and starves Store B. An intelligent system fair-shares the scarce inventory (giving 5 to A and 5 to B) based on their relative ROS.

---

## Case Application & Discussion Questions

1. **The Model Stock Calculation (30 minutes):** Product: Brass Diya (Pack Size: 12). Store: Mumbai Colaba. Avg Daily ROS: 5 units. Lead Time: 4 days. Review Cycle: 7 days. Safety Stock: 15 units. Display Min: 10 units. Current SOH: 22 units. SIT: 12 units.
   - Calculate Lead Time Demand (including review cycle).
   - Calculate the unconstrained Model Stock using max(Display, LTD+SS).
   - Calculate the Net Requirement.
   - Calculate the Final Order Quantity (applying pack size rounding logic).
2. **Correcting the ROS (20 minutes):** Product Z sold the following quantities over the last 4 weeks: W1: 40 units (in stock 7 days), W2: 12 units (in stock 2 days, then stocked out), W3: 0 units (out of stock all 7 days), W4: 35 units (arrived Tuesday, in stock 5 days).
   - Calculate the naive 4-week Average Weekly ROS (Total sales / 4 weeks). 
   - Calculate the True Average Weekly ROS (Sales per in-stock day × 7).
   - What is the percentage difference? If you used the naive ROS for replenishment, what would happen?
3. **The 70/30 Hold Strategy (20 minutes):** You buy 2,500 units of a new bed cover. Option 1: Push 100% to stores. (Freight cost $10/unit once). Option 2: Push 70% (1,750 units), Hold 30% (750 units) in DC. Later, replenish the 750 units. (Initial freight $10/unit, secondary pick/pack/freight $25/unit). Financially, Option 2 costs extra in logistics. If the bed cover retails for $2,499with a 60% gross margin, how many extra full-price sales does Option 2 need to generate to justify the extra logistics cost? 
4. **Dashboard Logic (30 minutes):** As the MIS lead, design an "Out of Stock (OOS) Root Cause" dashboard. When a store hits zero stock on a core item, the dashboard should automatically categorize the failure into one of these buckets:
   - Under-forecasted (ROS spiked suddenly)
   - Warehouse Stockout (DC had zero stock to send)
   - Vendor Delay (PO is late)
   - Transit Delay (SIT > Lead Time)
   Write the logical if/then statements for how the data would classify an OOS event into these 4 buckets.

---

## Connection to Next Module

We have covered how to group stores (4.1), how to push the initial stock (4.2), and how to pull replenishment stock (4.3). But all of these mathematical models hit a hard, physical wall: **The Store Fixture**. Module 4.4 explores Space Planning and Planogramming—the final constraint where financial math meets physical wood and glass.

**Next Module:** [Module 4.4: Space Planning & Planogramming](Module-4.4_Space-Planning-and-Planogramming.md)

---

## Key Takeaways

1. **Allocation is a guess; Replenishment is the truth.** Always hold ~30% of inventory in the DC to fuel the replenishment engine based on actual sales.
2. **Model Stock = max(Display Minimum, Lead Time Demand + Safety Stock).** It must breathe dynamically with the Rate of Sale, but never fall below the visual floor.
3. **Calculate ROS on In-Stock Days only.** Including stockout days mathematically guarantees a downward spiral of under-replenishment.
4. **Include Stock In Transit (SIT).** Ignoring SIT leads to double-ordering and bloated store inventory.
5. **Pack sizes dictate the final math.** A perfectly calculated requirement of 17 units means nothing if the vendor pack size is 24. Know when to round up (A stores) and round down (C stores).
