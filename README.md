## Shop Performance Case Study

An end-to-end data analysis project examining ** sales performance, customer behaviour, promotional effectiveness, product performance, and transaction outcomes** using Python, Pandas, Plotly Express, and Databricks.

## Project Overview

This project presents a complete data-analysis workflow applied to transactional retail data. The analysis covers **data profiling, data cleaning, anomaly detection, relational data integration, feature engineering, business metric development, and exploratory data visualisation**.

The objective is to transform raw transactional data into actionable insights that can support decisions around **revenue growth, customer retention, product performance, promotions, and operational efficiency**.

---

## Methodology

### Step 1: Exploratory Data Analysis & Profiling

The initial analysis assessed the structure and quality of the core datasets:

* `orders_df`
* `customers_df`
* `products_df`
* `payments_df`

The datasets were profiled to identify:

* Missing values
* Duplicate records
* Inconsistent categorical values
* Potential anomalies in numerical fields
* Referential integrity issues

### Step 2: Data Cleaning & Quality Improvements

Several data-quality issues were addressed before analysis:

* **Missing Values:** Missing numerical values were handled using appropriate imputation methods, while unrecorded payment methods were classified as `Unknown`.
* **Duplicates:** 120 duplicate order records were identified and removed to prevent distortion of revenue and transaction metrics.
* **Anomalies:** Negative quantity records were reviewed and excluded where they represented returns or erroneous transactions.
* **Referential Integrity:** Orphaned `CustomerID` records that could not be matched to the customer table were identified and addressed.
* **Text Standardisation:** Inconsistent city names and formatting were standardised u
### Step 3: Relational Data Integration

The datasets were merged sequentially to create analysis-ready tables while maintaining relational integrity:

1. `orders_df` — Base transaction table
2. `products_df` — Product names, categories and unit prices
3. `customers_df` — Customer cities, segments and demographic information
4. `payments_df` — Payment methods, statuses and payment dates

This integration enabled analysis across **transactions, products, customers, and payment behaviour**.

### Step 4: Feature Engineering & Business Logic

Additional analytical variables were created to support the business questions:

* **Temporal Features:** Extracted `Year`, `Month`, and `YearMonth` from `OrderDate` to analyse revenue trends over time.

* **Revenue:** Calculated revenue using:

  **Revenue = Quantity × Unit Price × (1 − Discount)**

* **Revenue Eligibility:** Revenue analysis was restricted to completed transactions, while all transaction statuses were retained when analysing cancellations, returns, and payment outcomes.

* **Customer & Product Metrics:** Developed aggregated measures including total revenue, order counts, average order value, and units sold.

---

## Key Insights

### 1. Product & Category Performance

**Electronics** emerged as the strongest revenue-generating category, highlighting its importance to overall shop performance.

### 2. Geographic Performance

Major markets such as **Tehran and Mashhad** contributed strongly to overall sales, indicating opportunities to focus marketing, logistics, and customer-retention efforts in high-performing locations.

### 3. Promotional Effectiveness

Transactions with **zero discount** generated the highest aggregate revenue. This suggests that broad discounting should be evaluated carefully to determine whether additional sales volume justifies the associated reduction in revenue per transaction.

### 4. Customer Segmentation

**Regular customers** represented the largest share of revenue among the analysed customer segments, highlighting the importance of retention strategies and opportunities to develop high-value customers into VIP segments.

### 5. Transaction & Payment Performance

Transaction-status analysis was used to evaluate completed, cancelled, and returned orders across different payment methods and identify potential areas for improving transaction conversion.

---

## Strategic Recommendations

Based on the findings from the analysis, the following recommendations are proposed:

### 1. Optimise Promotional Strategies

Avoid relying on broad discounting across the product range. Instead, use **targeted promotions** for underperforming products or categories where discounts can stimulate demand without unnecessarily reducing revenue on products that already perform strongly.

### 2. Prioritise High-Performing Categories

Electronics is a major revenue contributor. Maintaining **adequate inventory, product availability, and targeted marketing** in this category could help protect and grow overall revenue.

### 3. Strengthen High-Value Markets

High-performing cities such as Tehran and Mashhad should receive focused attention through **localised marketing, improved fulfilment, and customer-retention initiatives**, while lower-performing markets can be assessed for growth opportunities.

### 4. Develop Customer Loyalty

With Regular customers contributing substantially to revenue, a **tiered loyalty programme** could be used to improve retention and encourage movement toward higher-value VIP segments.

### 5. Monitor Transaction Outcomes

Continue monitoring cancelled, returned, and unsuccessful transactions by payment method to identify potential friction points and opportunities to improve the overall customer purchasing experience.

---

## Technology Stack

| Technology                | Purpose                                        |
| ------------------------- | ---------------------------------------------- |
| **Python**                | Data analysis and processing                   |
| **Pandas**                | Data cleaning, transformation and aggregation  |
| **Plotly Express**        | Interactive data visualisations                |
| **Databricks**            | Cloud-based analytics and notebook environment |

---

##  Project Outcome

The project demonstrates an end-to-end approach to **data cleaning, analysis, visualisation, and business interpretation**. The final outputs translate transactional data into practical insights that can support decisions around **revenue optimisation, customer retention, product strategy, promotional effectiveness, and operational performance**.

