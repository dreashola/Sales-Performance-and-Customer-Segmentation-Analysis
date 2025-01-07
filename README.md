# Sales Performance and Customer Segmentation Analysis
![Introduction](images/Customer-Segmentation.jpg)
## Objective
This analysis evaluates sales performance and customer segmentation using data-driven methodologies to inform personalized engagement strategies. It includes a detailed RFM (Recency, Frequency, Monetary) analysis and the development of an interactive Power BI dashboard with drill-down capabilities for actionable insights.

![Introduction](images/overview.png)
---

## Data Sources
The dataset for this analysis was sourced from [Kaggle](https://www.kaggle.com/datasets/gopikamahadevan/global-superstore?select=GlobalSuperstore.csv) and includes the following attributes:

- **Order Details:** Order ID, Order Date, Ship Date, Ship Mode, Order Priority.
- **Customer Details:** Customer ID, Customer Name, Segment.
- **Geographical Details:** City, State, Country, Postal Code, Market, Region.
- **Product Details:** Product ID, Category, Sub-Category, Product Name.
- **Sales Metrics:** Sales, Quantity, Discount, Profit, Shipping Cost.

The data was transformed into a relational data model adhering to third normal form (3NF) standards, with interconnected tables for customers, products, stores, and orders, enabling efficient analysis.

![](images/trans2.png)

---

## Data Preparation
- **Standardized Regional Classifications:** Consolidated North, South, Central, West, and East regions into "Other" where necessary.
- **Unique Identifiers:**
  - City-State-Country IDs for accurate store tracking.
  - Product IDs for name, category, and sub-category attributes.
  - Customer IDs for consistent linkage across tables.
- **Key Relationships:**
  - Linked orders to customer, store, date, and product tables.
- **Data Enhancements:**
  - Extracted product attributes (e.g., size, color) into separate columns.
  - Built a comprehensive date table in Power Query for temporal analysis.
  - Standardized column formatting for clarity and consistency.
- **Custom Columns Added:**
  - **Discount (Lost Revenue):** Quantified revenue impact of discounts.
  - **Fulfillment Duration:** Measured time between order placement and shipment.

![](images/trans.png)

---

## Data Transformation
- **Measures Developed:**
  - Ranking products and sub-categories by sales and profit margins.
- **Hierarchies for Drill-Down Analysis:**
  - Time: Year → Quarter → Month → Date.
  - Location: Country → State → City.
  - Product: Category → Sub-category → Product.
- **Defined KPIs:**
  - Total Sales
  - Average Order Value
  - Average Shipping Cost
  - Sales and Profit Growth (MoM, YoY)
  - Profit Margins
  - Customer Metrics (e.g., Orders per Customer, Retention Rates).


![](images/measures.png)
---

## RFM Analysis in Detail
RFM analysis assigns scores ranging from **1 to 4** for each dimension:

- **Recency (R):** How recently a customer made a purchase.
- **Frequency (F):** How often a customer makes purchases.
- **Monetary (M):** Total spending by the customer.

### RFM Customer Segments
| **Segment**           | **Scores**               | **Description**                                                             | **Action**                                                                 |
|------------------------|--------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|
| **Champions**          | 444, 443, 434, 433      | Highly engaged, frequent buyers with recent, high-value transactions.      | Reward loyalty with exclusive offers, VIP programs, and early access.      |
| **Loyal Customers**    | 442, 441, 432, 431, etc. | Consistent buyers with strong purchase histories and good recency.         | Encourage referrals and maintain engagement with personalized offers.       |
| **Potential Loyalists**| 344, 343, 334, 333, etc. | Promising recent buyers with moderate frequency and value.                  | Nurture with targeted promotions and loyalty programs.                     |
| **New Customers**      | 411, 412, 421, 422      | Recently acquired, low-value buyers.                                       | Onboard with welcome discounts and product recommendations.                |
| **Promising**          | 314, 313, 312, etc.     | Moderate recency and spending, potential for growth.                       | Provide personalized offers and engaging campaigns.                        |
| **Needs Attention**    | 321, 322, 231, etc.     | Moderate engagement and declining activity.                                | Use reminders, retargeting strategies, and limited-time offers.            |
| **About to Sleep**     | 224, 223, 214, etc.     | Low recency, moderate value, and low frequency.                            | Launch re-engagement campaigns with win-back offers.                       |
| **At Risk**            | 144, 143, 134, etc.     | Previously valuable customers showing disengagement.                       | Conduct surveys to identify pain points; offer tailored re-engagement deals.|
| **Can’t Lose Them**    | 114, 113, 124, etc.     | High-value customers on the verge of churn.                                | Assign account managers and provide premium services.                      |
| **Lost**               | 111, 112, 121, etc.     | Least engaged, lowest-value customers.                                     | Focus resources on other segments after win-back attempts.                 |

![](images/segment.png)
---

## Key Insights and Recommendations
1. **Discount Impact:** Discounts significantly influence revenue and profitability, requiring careful optimization.
2. **Segment Opportunities:**
   - Retain Champions and Loyal Customers through rewards and engagement programs.
   - Nurture Potential Loyalists and Promising customers with targeted campaigns.
   - Mitigate churn risks for At Risk and Lost customers with re-engagement efforts.
3. **Category Performance:** Furniture and office supplies show untapped profit potential.
4. **Shipping Optimization:** Standard shipping dominance suggests cost-cutting opportunities.

---

## Interactive Dashboards
Developed Power BI dashboards to present actionable insights:
- **Landing Page:** Central navigation hub.
- **Sales Overview:** Revenue, profit, and growth trends.
- **Product Analysis:** Performance by category, sub-category, and individual products.
- **Customer Overview:** Segment-wise performance, including sales and regional distribution.
- **Segment Analysis:** Drill-through capabilities for segmentation KPIs and group behaviors.

![](images/product.png)
---

## Conclusion and Next Steps
The analysis demonstrates the value of data-driven strategies for optimizing customer engagement and sales. 

### Next Steps:
1. Evaluate discount strategies to maximize profitability.
2. Target Promising and At Risk customers with tailored campaigns.
3. Refine pricing and shipping policies for underperforming categories.
4. Leverage seasonal trends for marketing and inventory planning.
5. Conduct churn analysis to proactively address disengagement risks.
---


## Click **[here](https://app.powerbi.com/view?r=eyJrIjoiNDZhY2RmZjctOWMzZC00ZjI1LWE1N2QtMzljMzc3ZTQxNmEwIiwidCI6ImRhZjMyMGRmLTc4ODMtNDA0Ny1hZWVjLTAxNTliMjRkZGFmZSIsImMiOjZ9&pageName=5f5b498ee27a5b4bf9ca)** to view the interactive dashboard

## Other images
![](images/customerdrill.png)

![](images/customer.png)

![](images/productdrill.png)

![](images/sales2.png)

![](images/sales3.png)

![](images/salesfilter.png)

![](images/salesmenu.png)