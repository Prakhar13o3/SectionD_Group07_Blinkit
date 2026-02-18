## Project Overview

This project transforms raw retail data from Blinkit into a strategic decision-making tool. By analyzing 8,500+ items across various outlet tiers and sizes, the study identifies key revenue drivers, optimizes digital shelf space (visibility), and evaluates the impact of outlet maturity on total sales.

---

## Data Dictionary

- Item_Fat_Content: Level of fat (Standardized: Low Fat, Regular)
- Item_Identifier: Unique ID assigned to each product
- Item_Type: Category of the product (e.g., Snacks, Fruits)
- Outlet_Establishment_Year: The year the store was first opened
- Outlet_Identifier: Unique ID for the specific store location
- Outlet_Location_Type: City classification (Tier 1, Tier 2, Tier 3)
- Outlet_Size: Ground area covered by the store (Small, Medium, High)
- Outlet_Type: Format of the store (Grocery Store, Supermarket)
- Item_Visibility: Percentage of total display area allocated to the product
- Item_Weight: Physical weight of the product
- Sales: Total revenue generated (Item_Outlet_Sales)
- Rating: Average customer satisfaction score
- Outlet_Age: Calculated column representing years of operation since establishment
- Visibility Efficiency: Calculated metric representing the ratio of Sales to Visibility

---

## Data Cleaning & Transformation

### Standardization of Fat Content Labels

Inconsistent naming conventions for Item_Fat_Content were unified. Labels such as low fat and LF were converted to Low Fat, while reg was converted to Regular to ensure accurate grouping during analysis.

### Handling Missing Values (Item Weight)

Null values in the Item_Weight column were identified and imputed using the average weight of products within the same category to maintain data integrity for weight-based trends.

### Treating Zero Values in Visibility

The Item_Visibility column contained several zero values, which is logically impossible for a product on sale. These were replaced with the median visibility of their respective Item_Type to prevent skewing the efficiency analysis.

### Engineering the Outlet Age Column

A new column was created by subtracting the Outlet_Establishment_Year from the current reporting year (2026). This enables tracking of revenue growth based on store maturity rather than calendar years.

### Adding the Visibility Efficiency Metric

A custom calculated column was created by dividing Total Sales by Item_Visibility.

Purpose:  
This metric identifies high-efficiency drivers — products that generate significant revenue even with low shelf or app visibility. It supports decisions around digital shelf optimization.

### Accuracy & Deduplication

The dataset was audited for duplicate entries using the Item_Identifier and Outlet_Identifier combination.  
Zero duplicates were found, confirming the uniqueness of transaction records.

---

## Key Insights & Statistics

### Revenue & Scale Overview

Total Revenue: ₹1,201,681 (Approx. ₹12 Lakhs)  
Total Volume: 8,523 items sold across all outlet types  
Average Rating: 3.96/5  

---

### The Winning Store Profile (The Sweet Spot)

Tier 3 locations are the most profitable, generating ₹472k in sales and outperforming Tier 1 locations by approximately 40%.

Medium-sized outlets are the most efficient, generating ₹507k in revenue and outperforming both small and high-sized formats.

Conclusion:  
The highest ROI is achieved by deploying medium-sized outlets in Tier 3 cities.

---

### Product Performance Leaders

Top Categories:

- Fruits & Vegetables (₹176k)  
- Snack Foods (₹174k)  

Niche Opportunity:

Starchy Foods has the highest average sales per item (₹142.38), indicating a premium customer base despite lower volume.

---

### The Visibility Paradox

Grocery Stores have the highest average item visibility (0.108) but the lowest total sales.

Takeaway:  
Increasing visibility alone does not compensate for limited inventory and lower footfall in smaller store formats.

---

### Shelf Space Efficiency

High-Efficiency Winners:

Categories such as Meat and Others generate the most revenue relative to their visibility (Efficiency Score greater than 40). These products perform strongly without heavy promotion.

Inefficient Placements:

Seafood and Breakfast items occupy significant digital real estate but generate the lowest return per visibility point (Efficiency Score below 30).

---

### Historical Growth Trends

Peak Maturity:

Stores established in 2018 are the highest performers, generating ₹204k in sales.

Concern Area:

Stores established in 2011 significantly underperform at ₹78k, indicating the need for operational review of older store models.

---

### Consumer Behavior

There is no significant difference in average sales between:

Low Fat items: ₹140.83  
Regular items: ₹141.28  

This suggests that fat content is not a primary purchasing factor for Blinkit customers.

---

## Dashboard Summaries

### Dashboard 1: Executive Sales Overview

Purpose:  
Designed as the primary landing page for CEOs and Managers to monitor overall business health.

Key Focus:

- Total Revenue (₹1.2M)  
- Average Ratings  
- Total Items Sold  

Functionality:

Includes a sales breakdown by Outlet Type, highlighting Supermarket Type 1 as the dominant revenue channel at approximately 65%. This dashboard presents the big-picture performance view for 2026.

---

### Dashboard 2: Product & Inventory Insights

Purpose:  
Designed for Inventory Managers and Category Leads.

Key Focus:

- Revenue across 16 product categories  
- Fat content comparison (Low Fat vs Regular)  
- Average sales per category  

Functionality:

Identifies Fruits & Vegetables and Snacks as category leaders, highlights Starchy Foods as a high-value low-volume segment, and flags Seafood as underperforming.

---

### Dashboard 3: Location & Logistics Strategy

Purpose:  
Designed for Operations and Expansion teams.

Key Focus:

- Relationship between Outlet Size, Location Tier, and Store Age  
- Store maturity performance analysis  

Functionality:

Highlights the optimal expansion strategy of medium-sized outlets in Tier 3 cities, compares historical store cohorts, and demonstrates that Tier 3 cities outperform Tier 1 by nearly 40% in revenue efficiency.

