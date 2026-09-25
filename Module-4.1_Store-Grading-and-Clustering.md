# Module 4.1: Store Grading & Clustering — Not All Stores Are Equal

> *"If you send the exact same assortment in the exact same quantities to a 10,000 sqft flagship in Manhattan and a 1,500 sqft boutique in a Tier-3 town, you will fail twice. You will starve the flagship of revenue and choke the boutique with dead stock. Treating unequal stores equally is the fastest way to destroy margin."*

**Semester:** 4 — The Store  
**Prerequisites:** Module 1.2 (Assortment Planning), Module 3.1 (Inventory Health)  
**Estimated Study Time:** 6–7 hours  
**Level:** Core — foundational for all allocation and replenishment

---

## Executive Summary & Core Dilemma

**How do you mathematically categorize a diverse network of stores so that you can allocate the right assortment width and depth to each, maximizing network-wide GMROI without managing 200 stores individually?**

When you build the ISQ plan (Module 1.4), you don't plan for "the company." You plan for the stores. But managing a network of 100, 200, or 350 stores individually is impossible for a human planner. Store grading and clustering compress that complexity into manageable buckets. Since your role heavily involves allocation and replenishment, this is your operating matrix.

---

## What Store Grading and Clustering Are (First Principles)

### Grading vs. Clustering: The Two Dimensions

Store analysis always operates on two axes: **Volume (Grade)** and **Profile (Cluster)**.

1. **Store Grading (The Y-Axis):** Grouping stores by their *sales volume capacity*. Grades answer the question: **"How MUCH stock should this store get?"**
   - Typically A, B, C, D grades.
   - Determines the **Depth** of inventory.

2. **Store Clustering (The X-Axis):** Grouping stores by their *customer behavior or format*. Clusters answer the question: **"WHAT KIND of stock should this store get?"**
   - Typically based on geography, climate, format (mall vs. high street), or customer demographics.
   - Determines the **Width** (Assortment) of inventory.

### The Power of the Matrix

When you cross Grades and Clusters, you create your **Store Matrix**. 

If Aura Global Retail has 300 stores, you cannot build 300 different assortment plans. But if you have 4 Grades (A, B, C, D) and 3 Clusters (Metro, Tier-2, Tourist), you only need to build **12 Assortment Profiles**. 

This is the secret to scaling retail planning: you manage the 12 profiles, and the system maps those 12 profiles to the 300 stores.

---

## Store Grading: The Volume Dimension

### The Mathematics of Grading

Store grading is usually done using a **Pareto (80/20) approach** or **Decile analysis** on historical sales. 

**Step 1: Rank stores by historical 12-month sales.**

| Rank | Store | Annual Sales ($ Cr) | Cumulative Sales ($ Cr) | Cumulative % |
|------|-------|-------------------|-----------------------|--------------|
| 1 | Mumbai Flagship | 12.5 | 12.5 | 5% |
| 2 | Delhi Select City | 11.2 | 23.7 | 9.5% |
| ... | ... | ... | ... | ... |
| 50 | Pune KP | 4.1 | 150.0 | 60% |
| ... | ... | ... | ... | ... |
| 250 | Small Town Store | 0.8 | 250.0 | 100% |

**Step 2: Assign Grades based on contribution thresholds.**

| Grade | Contribution Target | # of Stores | Avg Store Sales ($ Cr) | Characteristics |
|-------|---------------------|-------------|----------------------|-----------------|
| **A+ / Platinum** | Top 20% of Revenue | 15 stores (6%) | 8.5 | High capacity, flagship status, trend-setters |
| **A / Gold** | Next 30% of Revenue | 45 stores (18%) | 5.2 | Strong mall anchors, high traffic |
| **B / Silver** | Next 35% of Revenue | 90 stores (36%) | 3.1 | Core network, steady performers |
| **C / Bronze** | Bottom 15% of Revenue | 100 stores (40%) | 1.1 | Small footprint, limited capacity, basic focus |

**Notice the imbalance:** 6% of the stores (A+) generate 20% of the revenue. 40% of the stores (C) generate only 15% of the revenue. 

### Why Grading Matters for Allocation

If you have a new premium Silk Cushion Cover and you buy 500 units, how do you distribute them?
- **Without Grading (Democratic allocation):** 500 units / 250 stores = 2 units per store. 
  - *Result:* The Mumbai flagship sells its 2 units on Monday morning and stocks out. The small-town store sits on its 2 units for a year.
- **With Grading (Strategic allocation):** 
  - Give to A+ stores: 15 stores × 12 units = 180 units.
  - Give to A stores: 45 stores × 5 units = 225 units.
  - Give to B stores: 90 stores × 1 unit = 90 units.
  - Give to C stores: 0 units. (Assortment truncated).
  - *Result:* Deep inventory where it sells fast; no dead inventory where it doesn't.

### Dynamic Grading: The Category Nuance

A store's grade is rarely identical across all categories. 

A massive flagship in a corporate IT park might be an **A-grade** store for Men's Formal Wear, but a **C-grade** store for Home & Lifestyle because office workers don't buy heavy ceramics on their lunch break.

**Always grade stores at the Category (or Sub-Category) level, not just the total store level.**

*Worked Example: Aura Global Retail Store 'X'*
- Total Store Revenue Grade: **A**
- Apparel Category Grade: **A+**
- Personal Care Category Grade: **B**
- Hardgoods Category Grade: **C** (due to space constraints or customer profile)

If you allocate Hardgoods to this store assuming it's an 'A' grade, you will bloat it with dead inventory.

---

## Store Clustering: The Profile Dimension

### Defining Clusters

While grades tell you the *volume*, clusters tell you the *mix*. Clusters group stores that exhibit similar selling patterns, regardless of their total size.

Common clustering methodologies:

1. **Climate / Seasonality Clusters:**
   - *Winter/Cold:* High demand for quilts, heavy throws.
   - *Tropical/Warm:* High demand for light cottons, sheer curtains.
2. **Demographic / Location Clusters:**
   - *Urban/Metro:* Contemporary styles, modern silhouettes, premium pricing.
   - *Tier-2/Traditional:* Classic styles, bright colors, value pricing.
   - *Tourist/Airport:* Small, easily packable items, gifting focused.
3. **Format/Size Clusters:**
   - *Large Format (5,000+ sqft):* Full home setups, large furniture.
   - *Express Format (< 1,500 sqft):* Soft furnishings only, no bulky items.

### The Math of Clustering (Category Mix Analysis)

To prove a cluster exists, you look at the **Sales Mix** variance.

Let's analyze two "A-Grade" stores with identical total revenue ($5 Million) for the Home category:

| Sub-Category | Store 1 (Urban Mall) Mix % | Store 2 (Tier-2 High St) Mix % | Network Average |
|--------------|---------------------------|--------------------------------|-----------------|
| Bed Linen | 25% | 40% | 35% |
| Tableware/Ceramics | 35% | 15% | 20% |
| Decorative Accents | 25% | 15% | 20% |
| Furniture (Small) | 15% | 30% | 25% |
| **Total** | **100%** | **100%** | **100%** |

*Insight:* Despite having the same total volume, their profiles are vastly different. Store 1 heavily indexes on Ceramics and Decorative items (urban lifestyle, gifting). Store 2 heavily indexes on practical Bed Linen and Furniture. 

If you use the Network Average to assortment both stores, you will under-stock Ceramics in Store 1 and over-stock it in Store 2. 

### K-Means Clustering (Advanced Planner Concept)

In modern retail, planners use statistical clustering algorithms like K-Means to group stores based on multi-dimensional data rather than gut instinct.

#### 1. Feature Selection
You select numeric variables that define store performance and customer behavior. Examples:
- Total Sales Volume
- Average Selling Price (ASP)
- Category Sales Mix %
- Store Square Footage
- Full-Price Sell-Through %

#### 2. Normalization
Because these features have different units (e.g., Sales in0,000,000 vs. ASP in thousands vs. SqFt in thousands), you must normalize them, typically using Z-scores. This ensures that a metric like Total Sales doesn't dominate a percentage metric like Sell-Through.
**Z = (Value - Mean) / Standard Deviation**

#### 3. The Elbow Method (Choosing K)
How many clusters (K) should you have? The algorithm is run for K=1, 2, 3, 4, etc. You plot the Sum of Squared Errors (SSE) for each K. The SSE drops rapidly as you add clusters, but eventually, the drop slows down, forming an "elbow" shape on the graph. The elbow point represents the optimal balance between precision (more clusters) and simplicity (fewer clusters). In retail, K is usually 4 to 8.

#### 4. Interpretation
Once the algorithm groups the stores, the planner must name and interpret the clusters. 
- *Cluster 1:* High ASP, High Square Footage, High Fashion Mix. → **"Premium Large Format"**
- *Cluster 2:* Low ASP, High Basics Mix, High Volume. → **"Value Core"**
The algorithm does the math; the planner builds the strategy around it.

---

## Building the Assortment Matrix

### Intersecting Grades and Clusters

Once you have your Grades and Clusters, you build the matrix. Let's assume 3 Grades (A, B, C) and 2 Clusters (Metro, Tier-2) for simplicity. 

You have 6 Assortment Profiles:
1. A-Metro
2. A-Tier2
3. B-Metro
4. B-Tier2
5. C-Metro
6. C-Tier2

### The Width & Depth Rules by Profile

**Width (Option Count) relates to the Grade AND Cluster.**
**Depth (Units per Option) relates to the Grade.**

| Profile | Assortment Width | Option Focus | Initial Allocation Depth |
|---------|-----------------|--------------|-------------------------|
| **A-Metro** | 100% of Range (200 opts) | Heavy on Premium/Fashion | 12 units / option |
| **A-Tier2** | 80% of Range (160 opts) | Heavy on Core/Classic | 15 units / option |
| **B-Metro** | 70% of Range (140 opts) | Balanced Core/Fashion | 6 units / option |
| **B-Tier2** | 60% of Range (120 opts) | Core dominant | 8 units / option |
| **C-Metro** | 40% of Range (80 opts) | Best sellers only | 3 units / option |
| **C-Tier2** | 30% of Range (60 opts) | Entry price points only | 4 units / option |

*(Note: Tier-2 stores often have higher depth per option because they carry fewer total options but have strong store loyalty and steady traffic for basics.)*

### Assortment Truncation (The Cut-Off Line)

When building an assortment plan (Module 1.2), you rank your options. 
- Option Rank 1-60 (The Basics): Go to ALL stores (A, B, C).
- Option Rank 61-140 (The Core Seasonals): Go to A and B stores only.
- Option Rank 141-200 (The Fashion/Premium): Go to A-Metro stores only.

**This is Assortment Truncation.** It protects C stores from slow-moving fashion items that will eventually require heavy markdowns. 

---

## Applying Grading to Space and Capacity

### The Physical Constraint

Grades are not just about sales volume; they reflect physical space. A 'C' store physically cannot hold 200 options. 

*Worked Example:*
- Option requires 2 facings × 3 units deep = 6 units minimum display.
- Store 'C' has 3 fixtures for the category. Each fixture holds 15 options.
- Max capacity = 45 options.
- If you push 80 options to this store (ignoring the capacity limit), the store staff will keep 35 options in the backroom. They will never see the floor. They will age. They will be marked down. 

**Rule:** A store's Assortment Width (number of options) must NEVER exceed its Fixture Capacity. Grading forces this discipline. (This will be covered deeply in Module 4.4).

---

## Executive Perspectives

### How David Uses Grading

For David, grading is the daily allocation engine. When a shipment of new bedsheets arrives at the warehouse, David doesn't look at 200 stores. He looks at the matrix.
- "Send the King Size 400-TC Premium sets to A-Metro and A-Tourist."
- "Send the standard Double Size printed sets across all A, B, and C Tier-2 stores."
Grading turns a 2-day manual allocation nightmare into a 1-hour systematic push.

### How Sarah Views the Matrix

Sarah looks at the matrix strategically for the OTB (Module 1.3).
- "Our A-Metro stores are generating 40% of revenue but holding 50% of the inventory. We need to lean them out."
- "We are opening 10 new C-tier stores this year. I need to increase the buy quantity of my Option Rank 1-60 (Basics) to feed these new stores, but I don't need to increase the buy of my Fashion options."
The matrix dictates the shape of the buy.

---

## Strategic Trade-Offs & Risk Matrices

### Trade-Off 1: Complexity vs. Precision
Having 25 cluster profiles gives you incredible precision to match local tastes. But managing 25 assortment matrices is a logistical nightmare for planners, buyers, and supply chain. Having 2 profiles is easy, but highly imprecise. **The Sweet Spot: 6 to 12 total profiles.**

### Trade-Off 2: Aspiration vs. Reality
Aura Global Retail team wants the 'C' stores to carry the $5,000premium vase to elevate Aura Global Retail image (Aspiration). The planner knows the C store will sell zero vases and mark it down to $1,500after 8 months (Reality). **Resolution:** Allocate 1 unit as a "display only" prop, not as a selling SKU, funded by a marketing budget, not the OTB.

---

## Strategic & Operational Pitfalls

1. **Static Grading:** Grading stores once a year and forgetting it. If a 'B' store undergoes a renovation and footfall doubles, it needs to be dynamically upgraded to an 'A' grade immediately, or it will starve for stock.
2. **Total Store vs. Category Grading:** As mentioned, assuming a store that is 'A' for Apparel is 'A' for Home. Always grade at the Category level.
3. **Over-Assorting C Stores:** The most common margin destroyer. C stores have low traffic. Giving them a wide variety of options guarantees low sell-through across the board. C stores need narrow width (few options) and decent depth of the absolute best-sellers.
4. **Ignoring the "Halo Effect" of Flagships:** A+ Flagship stores sometimes have a lower GMROI than B stores because they carry the slow-moving, highly expensive "showpiece" items that define Aura Global Retail. Punishing an A+ store for this by cutting its assortment ruins Aura Global Retail halo. Understand the *role* of the grade.

---

## Case Application & Discussion Questions

1. **Calculate Store Grades (30 minutes):** You have 10 stores with the following annual Hardgoods revenue (in $00,000):
   S1: 120, S2: 15, S3: 85, S4: 210, S5: 45, S6: 30, S7: 195, S8: 60, S9: 150, S10: 25.
   Total Revenue: $9,350,000.
   - Rank them.
   - Group them into A (Top 40% of revenue), B (Next 40%), C (Bottom 20%).
   - How many stores fall into each bucket? What is the average revenue per store in each bucket?
2. **Category Mix Variance (20 minutes):** Store X and Store Y both do $1,000,000 in total Home sales.
   - Store X mix: Bed (20%), Bath (20%), Decor (50%), Dining (10%).
   - Store Y mix: Bed (50%), Bath (30%), Decor (10%), Dining (10%).
   If you launch a new premium Decor line, which store gets it? If you launch a value Bed linen line, which store gets it? Define the clusters for X and Y.
3. **Assortment Truncation (30 minutes):** You are buying 50 options of Cushions. 
   Your matrix has A stores (20 stores), B stores (50 stores), C stores (100 stores).
   - Options 1-10 (Core) go to A, B, C. 
   - Options 11-35 (Fashion) go to A, B.
   - Options 36-50 (Premium) go to A only.
   If all options require a minimum presentation depth of 6 units per store, how many total units of Option 5 (Core) must you buy? How many total units of Option 40 (Premium)?
4. **Dashboard Integration (20 minutes):** In your MIS role, design a simple weekly report that flags if a store's performance is deviating significantly from its assigned Grade (e.g., a 'C' store that is suddenly selling like a 'B' store). What specific metrics would trigger the flag?

---

## Connection to Next Module

Now that you have grouped your stores mathematically by Grade (volume) and Cluster (profile), you can execute the first major supply chain action: **Allocation**. Module 4.2 will teach you the exact math of how to push that first wave of inventory to the stores based on the matrix you just built. 

**Next Module:** [Module 4.2: Allocation](Module-4.2_Allocation.md)

---

## Key Takeaways

1. **Treating unequal stores equally destroys margin.** Democratic allocation guarantees stockouts in top stores and markdowns in bottom stores.
2. **Grade = Volume (Depth). Cluster = Profile (Width).** The intersection creates your Assortment Matrix.
3. **Grade at the Category level.** A flagship for Apparel is not automatically a flagship for Home.
4. **Assortment Truncation protects margin.** C stores should carry a fraction of the options that A stores carry, focused entirely on core best-sellers.
5. **Manage the matrix, not the stores.** Scale your planning capability by managing 12 profiles instead of 300 individual locations.
