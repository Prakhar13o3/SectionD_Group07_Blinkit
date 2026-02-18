Project Workflow: Blinkit Data Analysis (Logs)

              Step 1: Data Cleaning (The Foundation)

Standardized Labels: Fixed Item Fat Content (e.g., changed "low fat" to "Low Fat").

Imputed Missing Values: Filled gaps in Item Weight.

Advanced Imputation: Replaced 0% Item Visibility with the Median of each Item Type to avoid outlier skewing (Mean was up to 43% higher).

Checking Duplicates: Confirmed zero duplicate records.

              Step 2: Feature Engineering

Added Outlet Age: Calculated store age from the establishment year to better visualize performance trends based on "Store Maturity."

              Step 3: Pivot Table Development

Segmented Data: Created specific pivot tables for Sales by Tier, Size, Outlet Type, and Product Category.

Calculated KPIs: Established core metrics including Total Revenue, Average Sales per Item, and Top-Performing Outlet IDs.

              Step 4: Dashboard Construction

Modular Design: Built 3 separate dashboards to maintain clarity and prevent data overload.

Visual Strategy: Used a "Hero Chart" (Stacked Bar) to identify Tier 3 as the primary revenue driver and Area Charts to track maturity trends.

              Step 5: Interactivity & Final Insights

Dynamic UI: Integrated Slicers to allow users to filter data by item type or location.







            Sales Performance Executive Summary 
1. High-Level Performance
Total Revenue: ₹1,201,681 (approx. ₹12 Lakhs) across 8,523 items sold.

Customer Satisfaction: The average rating stands at 3.96/5, indicating strong brand health.

Primary Channel: Supermarket Type 1 is the core revenue driver, accounting for ~65% of total sales.

2. Outlet & Location Strategy
Top Store Type: Supermarket Type 1 (₹787k) is the dominant sales channel.

Tier Success: Tier 3 locations are the most lucrative (₹472k), outperforming Tier 1 by roughly 40%.

Size Efficiency: Medium-sized outlets are the most efficient operational model (₹507k) compared to "High" sized outlets (₹249k).

The "Sweet Spot": The most profitable combination is a Medium-sized outlet in a Tier 3 location.

3. Product Portfolio
Top Sellers: Fruits & Vegetables (₹176k) and Snack Foods (₹174k) lead the categories.

Underperformers: Seafood (₹8k) and Breakfast (₹16k) have the lowest sales volume.

Consumer Preference: Negligible difference between "Low Fat" (₹140.83) and "Regular" (₹141.28) items, suggesting fat content does not drive purchase decisions.

4. Digital Shelf Productivity (Efficiency Index)
High-Efficiency Winners: Others and Meat generate the highest revenue relative to their visibility (Efficiency Score >40). These "Natural Drivers" sell well without heavy promotion.

Inefficient Placements: Breakfast and Seafood occupy significant screen space but yield the lowest return per visibility point (Efficiency Score <30).

5. Action Plan
Expansion: Prioritize future store openings in Tier 3 using the Medium-sized model.

Inventory Focus: Increase stock levels for high-velocity categories like Fruits, Veggies, and Snacks.

Operational Audit: Investigate the 2011 cohort (₹78k) to identify bottlenecks compared to the high-performing 2018 cohort.

Digital Real Estate: Reallocate app visibility from low-efficiency categories to high-efficiency drivers (Meat/Snacks).

6. Historical Performance
Peak Year: Stores established in 2018 are the highest performers (₹204k), nearly double the average of other years (~₹130k).

Concern Area: Stores established in 2011 are significantly underperforming (₹78k).

Trend Insight: Sales stability from 2014–2017 suggests a consistent operational model, but the 2018 outlier warrants a deep dive to replicate its success.

7. Operational Insights
The Visibility Paradox: Grocery Stores have the highest "Average Item Visibility" (0.108) yet the lowest sales, proving that visibility cannot compensate for smaller inventory and lower footfall.

Consistency: Average ratings are remarkably consistent across all store types (~3.96/5).

Key Takeaway: Revenue disparity is driven by availability and store size, not poor service or product quality.

8. Hidden Opportunities
High Value, Low Volume: Starchy Foods has one of the highest Average Sales per item (₹142.38) but very low total sales (₹21k).

Strategy: Expanding the stock or marketing for Starchy Foods represents a high-margin growth opportunity.

Category Review: Unless supply chain costs are minimal, the Seafood category (₹8k) may not justify its shelf space.

