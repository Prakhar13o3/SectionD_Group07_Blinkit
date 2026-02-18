##  Project Overview
This project transforms raw retail data from Blinkit into a strategic decision-making tool. By analyzing 8,500+ items across various outlet tiers and sizes, the study identifies key revenue drivers, optimizes digital shelf space (visibility), and evaluates the impact of outlet maturity on total sales.

## Data Dictionary
1. Item_Fat_Content: Level of fat (Standardized: Low Fat, Regular).
2. Item_Identifier: Unique ID assigned to each product.
3. Item_Type: Category of the product (e.g., Snacks, Fruits).
4. Outlet_Establishment_Year: The year the store was first opened.
5. Outlet_Identifier: Unique ID for the specific store location.
6. Outlet_Location_Type: City classification (Tier 1, Tier 2, Tier 3).
7. Outlet_Size: Ground area covered by the store (Small, Medium, High).
8. Outlet_Type: Format of the store (Grocery Store, Supermarket).
9. Item_Visibility: % of total display area allocated to the product.
10. Item_Weight: Physical weight of the product.
11. Sales: Total revenue generated (Item_Outlet_Sales).
12. Rating: Average customer satisfaction score.
13. Outlet_Age: [Calculated Column] Years of operation since establishment.
14. Visibility Efficiency: [Calculated Metric] Ratio of Sales to Visibility

## Data Cleaning & Transformation

1. Standardization of Fat Content Labels: Inconsistent naming conventions for Item_Fat_Content were unified. Labels like low fat and LF were converted to Low Fat, while reg was converted to Regular to ensure accurate grouping during analysis.

2. Handling Missing Values (Item Weight): Null values in the Item_Weight column were identified. These were imputed using the average weight of products within the same category to maintain data integrity for weight-based trends.

3. Treating Zero Values in Visibility: The Item_Visibility column contained several 0 values, which is logically impossible for a product on sale. These were replaced with the Median visibility of their respective Item_Type to prevent skewing the efficiency analysis.

4. Engineering the "Outlet Age" Column: A new column was created by subtracting the Outlet_Establishment_Year from the current reporting year (2026). This allows the business to track revenue growth based on store maturity rather than just calendar dates.

5. Adding the "Visibility Efficiency" Metric: A custom calculated column was added by dividing Total Sales by Item_Visibility.

Why: This was done to identify "High-Efficiency Drivers"—products that generate significant revenue even with low shelf/app visibility. This helps the marketing team decide which products deserve more digital real estate and which are currently wasting space.

6. Accuracy & Deduplication: The dataset was audited for duplicate entries based on the Item_Identifier and Outlet_Identifier combination. 0 duplicates were found, confirming the uniqueness of the transaction records.

Key Insights & Statistics

1. Revenue & Scale Overview

Total Revenue: ₹1,201,681 (Approx. ₹12 Lakhs).

Total Volume: 8,523 items sold across all outlet types.

Customer Health: The average rating is a stable 3.96/5, reflecting consistent service and product quality across the board.

2. The Winning Store Profile (The "Sweet Spot")

Top Performance: Tier 3 locations are the most profitable, generating ₹472k in sales (outperforming Tier 1 by ~40%).

Operational Efficiency: Medium-sized outlets are the most efficient, generating ₹507k in revenue, proving more effective than "High" or "Small" sized formats.

Conclusion: The highest ROI is achieved by deploying Medium-sized outlets in Tier 3 cities.

3. Product Performance Leaders

Top Categories: Fruits & Vegetables (₹176k) and Snack Foods (₹174k) are the primary revenue drivers.

Niche Opportunity: Starchy Foods has the highest average sales per item (₹142.38), suggesting a premium customer base despite lower total volume.

4. The Visibility Paradox

Insight: Grocery Stores have the highest average item visibility (0.108) but the lowest total sales.

Takeaway: Simply increasing product visibility on the app or shelf does not compensate for the limited inventory and lower footfall of smaller store formats.

5. Shelf Space Efficiency

High-Efficiency Winners: Categories like Meat and Others generate the most revenue relative to their visibility (Efficiency Score >40). These are "natural sellers" that thrive without heavy promotion.

Inefficient Placements: Seafood and Breakfast items occupy significant digital real estate but yield the lowest return per visibility point (Efficiency Score <30).

6. Historical Growth Trends

Peak Maturity: Stores established in 2018 are the highest performers (₹204k), nearly doubling the average of other historical cohorts.

Concern Area: Stores established in 2011 are significantly underperforming (₹78k), indicating a need for an operational audit of older store models.

7. Consumer Behavior

Health Labels: There is no significant difference in sales between Low Fat (₹140.83) and Regular (₹141.28) items. This suggests that fat content is not a primary decision-making factor for the average Blinkit customer.

Dashboard Summaries
Dashboard 1: Executive Sales Overview

Purpose: This is the primary landing page designed for high-level stakeholders (CEOs/Managers) to monitor the overall health of the business.

Key Focus: It tracks core KPIs such as Total Revenue (₹1.2M), Average Ratings, and the total count of items sold.

Functionality: It features a breakdown of sales by Outlet Type, allowing users to see at a glance that Supermarket Type 1 is the dominant revenue channel (65%). It provides the "Big Picture" of the company’s performance in 2026.

Dashboard 2: Product & Inventory Insights

Purpose: This dashboard focuses on "What" is being sold and "How" it is perceived by customers. It is designed for Inventory Managers and Category Leads.

Key Focus: It analyzes revenue across 16 product categories, identifying "Fruits & Vegetables" and "Snacks" as the market leaders.

Functionality: It includes a deep dive into Item Fat Content (Low Fat vs. Regular) and Average Sales per Category. This view helps identify high-value/low-volume items like "Starchy Foods" and allows for a review of underperforming categories like "Seafood."

Dashboard 3: Location & Logistics Strategy

Purpose: This view focuses on the "Where" and "When" of sales. It is designed for Operations and Expansion teams to plan future growth.

Key Focus: It explores the relationship between Outlet Size, Location Tier, and Store Age.

Functionality: It highlights the "Sweet Spot" (Medium-sized outlets in Tier 3 locations) and uses historical data to compare the success of the 2018 store cohort against older models. It allows the team to see that Tier 3 cities are currently outperforming Tier 1 by nearly 40% in revenue efficiency.
