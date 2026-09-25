# Module 4.2: Allocation — First Distribution of Stock

> *"Allocation is where the rubber meets the road. It doesn't matter how beautiful the assortment plan is or how accurate the open-to-buy is; if the right product isn't in the right store on launch day, you will lose the sale and the margin."*

**Semester:** 4 — The Store  
**Prerequisites:** Module 4.1 (Store Grading & Clustering), Module 3.3 (Availability & Service Level)  
**Estimated Study Time:** 6-7 hours  
**Level:** Core  

---

## Executive Summary & Core Dilemma

**How do we mathematically decide exactly how many units of a new product to send to each individual store before we have any actual sales history for that specific item?**

---

## What Allocation Is (First Principles Definition)

At its most fundamental level, **Allocation** is the initial, calculated distribution of inventory from the central warehouse (or Distribution Center, DC) to the store network. It is the "push" of stock that happens before the item has started selling in the stores. 

In retail planning, inventory movement to stores is broadly categorized into two mechanics: **Push** and **Pull**. 

- **Allocation (Push):** The planner analyzes data, assumptions, and physical constraints to proactively push inventory out to stores. The stores do not ask for it; the planner decides what they will receive. This happens for new season launches, initial stock-ups of new styles, or promotional drops.
- **Replenishment (Pull):** Once an item is on the shelf and starts selling, actual consumer demand "pulls" replacement inventory from the warehouse to the store. This is a reaction to sales history (covered in detail in Module 4.3).

**The Core Goal:** The objective of allocation is to maximize full-price sell-through and overall margin by putting the right quantity of inventory in the right stores at the moment of launch. If you allocate too much to a low-performing store, capital is trapped and markdown risk increases. If you allocate too little to a high-performing store, you suffer immediate out-of-stocks and lost sales. 

In the context of Aura Global Retail's Home & Lifestyle category, allocation means ensuring that when a new collection of Hand-block Printed Bedcovers arrives at the warehouse, the correct mix of quantities and sizes is sent to the flagship store in Delhi versus a smaller boutique in an airport terminal.

---

## Why This Exists (The Problem It Solves)

When Sarah, VP of Merchandising for Hardgoods (managing a $100 Million business), signs off on a new collection of brass diyas and terracotta lamps for the Diwali season, he buys the inventory at an aggregate, chain-wide level based on the Open-to-Buy (OTB). 

However, inventory cannot be sold in aggregate. It must be physically present in a specific location where a customer can touch, feel, and buy it. 

The problem allocation solves is **Spatial Disaggregation of Risk**.
When 10,000 units of a new brass diya arrive at the warehouse, the risk is concentrated but manageable. The moment you distribute those 10,000 units across 250 stores, you are fragmenting your risk into 250 micro-bets. Allocation exists to calculate those micro-bets intelligently rather than randomly, balancing mathematical demand forecasts with physical retail realities like shelf space and vendor packaging.

Without a structured allocation methodology, retailers suffer from:
1. **The Phantom Out-of-Stock:** The company as a whole has 500 units in stock, but the top 50 stores have 0, while the bottom 150 stores have 3 units each that aren't selling.
2. **Visual Merchandising Failure:** Stores receive 1 unit of a product, making the display look impoverished and signaling low value to the customer.
3. **Logistics Bleed:** Shipping inefficient micro-quantities that incur high freight costs and require breaking factory-sealed cartons at the DC, increasing labor costs and damages.

---

## How It Connects to the Retail System

As we learned in **Module 0.1 (The Retail Value Chain)**, inventory flows through a sequential pipeline. Allocation sits perfectly at the intersection of Buying and Selling.

1. **Strategic Planning & OTB:** Dictates how much capital we have to buy the total category.
2. **Assortment Planning:** Dictates the breadth of styles and total units purchased.
3. **Store Grading (Module 4.1):** Gives us the mathematical weighting of each store's potential volume for a specific category.
4. **Allocation (This Module):** Uses the store grades to physically distribute the units purchased in Assortment Planning.
5. **Replenishment (Module 4.3):** Takes over after allocation, reading point-of-sale data to refill what was sold.

Allocation is the ultimate stress test of your Assortment Plan. If you find yourself struggling to allocate a product effectively (e.g., you don't have enough units to give every target store a meaningful display), it usually means the Assortment Plan was flawed—you bought too much breadth (too many styles) and not enough depth (too few units per style).

---

## The Allocation Equation

To remove emotion and guesswork from the initial push, planners use the Allocation Equation. This formula calculates the exact number of units to send to a specific store for a specific SKU.

**Initial Allocation = (Target WOC × Expected Weekly ROS) + Display Quantity**

Let's define each component:

### A. Expected Weekly ROS (Rate of Sale)
How many units of this specific item do we expect this specific store to sell per week? 
Since this is a new item with no history, we estimate this by taking the **Chain Average ROS** for a similar item and applying the **Store Grade Index** (from Module 4.1).

**Expected Weekly ROS = Chain Average ROS × Store Grade Index**

### B. Target WOC (Weeks of Cover)
How many weeks of forward sales do we want to provide in the initial push? If the DC lead time (time taken to pick, pack, and ship to the store) is 2 weeks, you might want to send 4 weeks of cover so the store doesn't run out before the first replenishment shipment arrives.

### C. Display Quantity (Presentation Minimum)
The absolute minimum physical units required on the shelf or table to make the product look appealing to the customer, regardless of how fast it sells. A bedcover might only sell 1 unit every 2 weeks, but a store needs at least 2 on the shelf to create a visual block.

### Worked Example: The Wooden Salad Bowl Launch
Aura Global Retail is launching a new Acacia Wood Salad Bowl (Retail Price: $1,500). 
- **Chain-wide expected sales rate:** 2 units per store, per week.
- **Target WOC for launch:** 4 weeks (to allow time for sales to register and replenishment to kick in).
- **Display Quantity:** 3 units (Visual Merchandising requires a stack of 3 bowls on the nesting tables).

Let's calculate the allocation for two different stores:

**Store A: Indiranagar, Bangalore (Grade A+, Category Index: 1.5)**
1. **Expected Weekly ROS:** 2 units × 1.5 (Index) = 3 units/week
2. **Sales Cover Requirement:** 3 units/week × 4 WOC = 12 units
3. **Display Quantity:** 3 units
4. **Initial Allocation:** 12 + 3 = 15 units

**Store B: Tier-2 Mall, Mysore (Grade C, Category Index: 0.5)**
1. **Expected Weekly ROS:** 2 units × 0.5 (Index) = 1 unit/week
2. **Sales Cover Requirement:** 1 unit/week × 4 WOC = 4 units
3. **Display Quantity:** 3 units
4. **Initial Allocation:** 4 + 3 = 7 units

Notice the mathematical elegance here. Store A receives 15 units, giving it enough stock to fuel its high sales velocity. Store B receives 7 units—it only mathematically needs 4 units to cover a month of sales, but the display minimum of 3 acts as an additive baseline to ensure the store doesn't look empty.

---

## Display Minimums (The Visual Constraint)

In retail, physics often trumps mathematics. A planner looking strictly at a spreadsheet might conclude that a Grade D store selling 0.5 units a week only needs 1 unit in stock for the month. But retail is theater. If a customer walks into a Aura Global Retail store and sees one solitary, lonely ceramic mug sitting on a massive wooden shelf, they perceive it as leftover stock, defective, or undesirable.

This is the conflict between **Visual Merchandising (needs full shelves)** and **Inventory Efficiency (needs lean stock)**.

Display minimums dictate the absolute floor for an allocation. If the display minimum is higher than what you can afford to allocate, you should not allocate the product to that store at all. 

### Worked Example: The Floor Lamp Dilemma
You are allocating a new Brass Floor Lamp ($8,000retail). 
You have 100 units in the warehouse. You have 80 stores.
The VM guideline states that Floor Lamps must be displayed in pairs (Display Quantity = 2). 

If you try to allocate to all 80 stores:
- To meet the display minimum: 80 stores × 2 units = 160 units required
- You only have 100 units. 

If you simply send 1 unit to all 80 stores, you violate the VM guideline. The stores look terrible, and the product won't sell. 
Instead, you must restrict the allocation to fewer stores to maintain the display integrity. You allocate 2 units to your Top 50 stores (using exactly 100 units). The bottom 30 stores receive nothing. This protects Aura Global Retail presentation and concentrates stock where it has the highest probability of selling.

---

## Depth vs. Breadth in Allocation

The Floor Lamp dilemma introduces one of the most critical decisions a planner makes: Depth versus Breadth. 

- **Breadth:** Sending a product to as many stores as possible (e.g., all 250 Aura Global Retail stores).
- **Depth:** Sending a larger quantity of a product to a smaller subset of stores.

### The "Peanut Butter" Mistake
A common error among junior planners is "spreading peanut butter too thin." They want every store to have the new product to keep all Store Managers happy. So, if they have 300 units of a cushion cover and 150 stores, they allocate 2 units to every store. 

Why is this disastrous?
1. **Immediate Stockouts in Top Stores:** A Grade A store will sell those 2 units on the first weekend. They are now out of stock for 2 weeks until replenishment kicks in. You lost massive sales upside.
2. **Trapped Capital in Bottom Stores:** A Grade D store might take 4 months to sell those 2 units. That inventory is gathering dust.
3. **High Logistics Cost:** Shipping 2 units to 150 locations is highly inefficient and expensive.

### Minimum Viable Depth (MVD)
Planners must establish a Minimum Viable Depth (MVD). This is the minimum allocation quantity that justifies sending the product to a store, factoring in freight costs, DC processing, and display integrity. 

If a store's calculated allocation (Sales Cover + Display) falls below the MVD, they do not receive the item.

### Worked Example: Ceramic Dinner Plates
You have 1,500 units of a new Ceramic Dinner Plate ($20 retail).
You want to allocate them. The MVD is 12 units (because dinner plates are usually bought in sets of 4 or 6; having fewer than 12 units risks an immediate broken assortment).

| Store Grade | Store Count | Calc. Allocation per Store | Meets MVD (12)? | Decision | Total Units Allocated |
|---|---|---|---|---|---|
| A | 20 | 36 units | Yes | Allocate 36 | 20 × 36 = 720 |
| B | 40 | 24 units | Yes | Allocate 24 | 40 × 24 = 960 |
| C | 60 | 10 units | No | Do Not Allocate | 0 |
| D | 30 | 4 units | No | Do Not Allocate | 0 |
| **Total** | | | | | **1,680 units required** |

Wait, we need 1,680 units but only have 1,500! 
You cannot reduce Grade C and D, because they are already at 0. You must trim the allocation from Grade A and B. 
Instead of sending 24 units to Grade B stores, you might send 19 units (20 × 36 = 720; 1500 - 720 = 780 remaining. 780 / 40 stores = 19.5 units).
You ensure Depth in the best stores, even at the cost of zero Breadth in the bottom 90 stores.

---

## Pre-pack / Carton Optimization

In theoretical retail, you can allocate exactly 7 units to a store. In physical retail, products arrive from vendors in specific carton configurations, known as Pre-packs, Master Cartons, or Inner Packs.

Assume our new Brass Diyas are shipped from the artisan in Moradabad in a **Master Carton of 24 units**, containing 4 **Inner Packs of 6 units** each.

When a store needs 7 units based on our Allocation Equation, the DC faces a choice:
1. **Break down an Inner Pack:** Open the box of 6, take out 1 unit to add to another box of 6, creating a custom shipment of 7. 
2. **Round Down to the Inner Pack:** Send 6 units.
3. **Round Up to the nearest Inner Pack:** Send 12 units (2 inner packs).

**The Margin Impact of Breaking Cartons:**
Every time the warehouse opens a factory-sealed carton to pick "eaches" (individual units), costs skyrocket. 
- Labor costs increase (picking 1 unit takes almost as much time as picking a full box).
- Packaging costs increase (you need a new secondary box).
- Breakage risk increases (factory packing is designed for transport; custom DC packing often isn't as secure, especially for fragile Hardgoods).

**The Planner's Rule:** Always round to the nearest Inner Pack (or Master Carton) for the initial allocation, unless it's an extremely high-value, slow-moving item (like a $25,000rug). 

### Worked Example: Rounding Logic
Item: Scented Candles. Inner Pack Size: 6 units. Master Carton: 24 units.

| Store | Calculated Allocation | Rounding Rule | Actual Allocated Qty | Justification |
|---|---|---|---|---|
| Delhi Flagship | 28 units | Round up to nearest Inner Pack | 30 units (5 inner packs) | Avoid breaking an inner pack; high volume store can absorb the extra 2 units. |
| Cochin Airport | 8 units | Round down to nearest Inner Pack | 6 units (1 inner pack) | Sending 12 would overstock them by 50%. Safer to round down for a smaller store. |
| Mumbai Colaba | 23 units | Round up to Master Carton | 24 units (1 Master Carton) | Shipping an intact Master Carton is the cheapest, safest freight method. |

Mastering carton optimization separates novice planners from true professionals. You aren't just moving numbers on a screen; you are directing physical labor and freight economics in a warehouse 500 kilometers away.

---

## New Product Allocation vs. Continuity Allocation

How do you estimate the `Chain Average ROS` for a product that has never existed before? You use **Proxy SKUs** or **Like-for-Like (LFL)** matching.

When allocating a completely new item, the planner identifies a historical item that shares similar attributes:
- Same sub-category (e.g., Table Linen - Placemats)
- Same price tier (e.g., $35 - $50)
- Same seasonality (e.g., launched in Autumn/Winter)
- Similar aesthetic (e.g., geometric print vs floral print)

You pull the historical launch data for the Proxy SKU and use its first 4 weeks of ROS as the baseline for the new item.

**Continuity Allocation:** For items that are always in stock (core staples like basic white bedsheets), allocation is less about "pushing" a launch and more about "resetting" store inventory levels based on updated store grades for the new financial half-year. We rely heavily on actual store-level history for continuity items.

---

## Size Curve / Variant Curve Allocation

Not all variants sell equally in all locations. In Home & Lifestyle, "size" often refers to dimensions (e.g., Bedcovers: Single, Double, King, Super King) or colors. 

You cannot apply a flat chain-wide ratio (e.g., 20% Single, 40% Double, 40% King) to every store. You must allocate based on **Cluster-Specific Variant Curves**.

Urban, high-income Tier-1 stores (Delhi, Mumbai, Bangalore) typically index much higher on King and Super King sizes because apartments are larger and primary bedrooms feature larger beds. Tier-2 and Tier-3 cities often index heavily on Double and Single sizes.

### Worked Example: The Bedcover Allocation
You are allocating 100 units of a new block-printed bedcover to Store A (Mumbai) and Store B (Lucknow). 

**Chain Average Size Curve:** 20% Single, 40% Double, 40% King.
**Mumbai Size Curve:** 10% Single, 30% Double, 60% King.
**Lucknow Size Curve:** 30% Single, 50% Double, 20% King.

If you allocate 100 units to each store using the Chain Average, Mumbai will stock out of King sizes immediately, and Lucknow will have unsold King sizes gathering dust for months.

By allocating against the Cluster Curve:
- **Mumbai receives:** 10 Single, 30 Double, 60 King.
- **Lucknow receives:** 30 Single, 50 Double, 20 King.

This maximizes yield by aligning the physical inventory with the local demographic reality.

---

## Executive Perspectives

### How David Operates on Allocation
David reviews the allocation plans on Tuesday mornings before transmitting them to the DC for Wednesday picking. He is looking for execution anomalies:
- *"Are we breaking too many cartons? Our DC labor budget is already stretched this month."*
- *"Did we maintain the Display Minimums for the new Diwali glassware drop? I don't want angry calls from the Visual Merchandising head when stores look empty."*
- *"Are we starving the top 10 stores to feed the bottom 50? Sort the allocation spreadsheet descending by quantity; if a Grade C store is getting more than a Grade A store, something is broken in the formulas."*

### How Sarah Thinks About Allocation
Sarah views allocation as the realization of his strategy. He looks at the macro-level distribution:
- *"We invested heavily in premium $15,000brassware this season to elevate Aura Global Retail perception. Did the allocation team concentrate this in our 30 flagship premium stores, or did they accidentally scatter it across 150 tier-3 stores where it will intimidate the customer?"*
- *"We bought 50,000 units of the entry price-point tea mugs to drive volume and footfall. Have these been pushed broad and deep to ensure we hit our $2 Million sales target for this event?"*

---

## Strategic Trade-Offs & Risk Matrices

### Warehouse Hold vs. Store Push
When 1,000 units of a new product arrive, you face a strategic choice: Do you push all 1,000 units to the stores immediately, or do you hold some back?

**Scenario A: 100% Push (The "Empty the DC" Approach)**
- **Pros:** Maximum visual impact in stores. Logistics efficiency (ship it once and be done). Frees up space in the warehouse.
- **Cons:** If you allocated incorrectly, you are trapped. If Store A sells out and Store B sells nothing, you cannot easily move stock from B to A (Inter-Store Transfers are expensive and slow). You must resort to markdowns in Store B.

**Scenario B: 70% Push / 30% Warehouse Hold (The "Read and React" Approach)**
- **Pros:** You push enough to launch the product (700 units). You hold 300 units in reserve. After 2 weeks, you analyze actual sales. You discover Store C is selling it three times faster than expected. You use the 30% hold to aggressively replenish Store C, maximizing full-price sales.
- **Cons:** Requires a second wave of logistics costs. Can result in warehouse dead-stock if the product flops everywhere and you are left holding 30% that no store wants.

**The Decision Framework:**
- **Fashion/Trend/High-Uncertainty items:** Hold 20-30% back to react to actual demand.
- **Basic/Core/High-Volume items:** Push 90-100%. You know they will sell eventually; minimize freight touches.
- **Imported/Long-Lead-Time items:** Hold back to protect against supply chain shocks.

---

## Strategic & Operational Pitfalls

1. **Allocating Strictly on Total Store Volume:** Giving a store a huge allocation of expensive dinnerware just because it has high total sales, ignoring that the store's sales are heavily skewed towards cheap apparel, not Hardgoods. You must allocate using *Category-Specific* store grades.
2. **Ignoring Display Minimums for Breadth:** Sending 1 unit to every store to make everyone happy, resulting in poor visual presentation and zero sales velocity.
3. **Blindly Breaking Cartons:** Using exact mathematical formulas that result in sending 11 units, forcing the DC to break a carton of 12. This destroys warehouse efficiency.
4. **Pushing 100% of Unproven Trends:** Allocating every single unit of a highly experimental new design on Day 1, leaving no reserve to chase the stores where the trend actually resonates.
5. **Averaging the Size Curve:** Applying a flat national size curve (e.g., 30/40/30) to all clusters, ignoring the vast differences in consumer demographics between a metro flagship and a tier-3 highway stop.

---

## Case Application & Discussion Questions

1. **The Allocation Equation:** You are launching a new Teapot (Retail $1,200). Chain Average Expected ROS is 1.5 units/week. Target WOC is 6 weeks. Display Minimum is 2 units. Calculate the Initial Allocation for:
   - Store A (Grade A, Index 1.8)
   - Store B (Grade C, Index 0.6)
2. **The Carton Math:** A new set of Coasters comes in Master Cartons of 48, with Inner Packs of 12. Your calculation says Store X needs 29 units. Store Y needs 10 units. Store Z needs 44 units. Using standard rounding rules (round to nearest inner pack/carton to protect margins), what exact quantities do you send to each store? Justify your decision.
3. **Depth vs Breadth Capital Allocation:** You have $50,000 worth of a new premium hand-painted vase (Cost per unit: $2,000). You have 250 units total. You have 50 Grade A stores and 100 Grade B stores. Display minimum is 4 units (MVD). Can you allocate this to all Grade A and B stores? If not, how do you adjust your strategy? Show the math.
4. **The Hold-Back Strategy:** You receive a shipment of 5,000 units of a highly experimental seasonal cushion cover. Based on the Decision Framework, how many units do you push immediately, and how many do you hold in the warehouse? What specific data will you look at in Week 3 to decide where to send the held-back inventory?

---

## Connection to Next Module

Allocation gets the stock onto the shelf for opening day. But what happens on Monday morning after a busy weekend when the shelves are half-empty? 

We cannot run manual allocation equations every day. We need a system that reads what was sold and automatically replaces it. We need to transition from the **Push** of Allocation to the **Pull** of Replenishment. 

**Next Module:** [Module 4.3: Replenishment](Module-4.3_Replenishment.md)

---

## Key Takeaways

1. **Allocation is the spatial disaggregation of risk.** It distributes a centralized purchase into hundreds of localized bets.
2. **Use the Allocation Equation:** (Target WOC × Expected Weekly ROS) + Display Quantity.
3. **Display Minimums trump math.** If you cannot allocate enough units to meet the physical display requirement, do not allocate it to that store.
4. **Protect Depth over Breadth.** "Spreading peanut butter" guarantees stockouts in top stores and dead stock in bottom stores.
5. **Optimize Cartons.** Never break factory packs unless absolutely necessary. Rounding to the nearest inner pack preserves margins by reducing DC labor.
6. **Use Proxy SKUs for launches.** Model new product ROS based on similar historical items.
7. **Hold back on uncertainty.** Retain 20-30% of fashion/trend items at the warehouse to "read and react" to actual localized demand.
