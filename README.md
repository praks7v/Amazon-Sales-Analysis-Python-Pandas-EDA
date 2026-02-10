# 📊 E-Commerce Business Performance Analysis

## 1. Business Context

This project analyzes transactional sales data from an e-commerce business to evaluate **overall business performance** and identify **key revenue drivers**.  
The analysis is conducted from the perspective of a **Data Analyst supporting business stakeholders**, with a focus on translating raw data into actionable insights.

The dataset reflects real-world e-commerce complexity, including order-line level granularity, multiple order statuses, and operational attributes such as fulfillment and shipping methods.

---

## 2. Objective

The objectives of this analysis are to:

- Assess overall revenue and order performance
- Understand sales trends and seasonality over time
- Identify high-performing products and categories
- Evaluate fulfillment and operational dependencies
- Provide data-driven business recommendations

---

## 3. Dataset Overview

- **Source:** E-commerce sales transaction data
- **Records:** ~129,000 order-line records
- **Granularity:** Product-level line items (multiple rows per order)
- **Time Period:** March–June 2022
- **Key Fields:**
  - Order ID
  - Order Date
  - Product SKU & Category
  - Quantity
  - Revenue (Amount)
  - Order Status
  - Fulfilment Method
  - Shipping Location

Each row represents a **single product sold within an order**, requiring careful aggregation for order-level KPIs.

---

## 4. Tools & Technologies

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Jupyter Notebook  

---

## 5. Data Quality & Preparation

Several data quality challenges were addressed prior to analysis:

- Removed irrelevant and empty columns
- Converted date fields to datetime format
- Filtered out cancelled and non-revenue transactions
- Validated quantity and revenue values
- Standardized categorical fields for consistent grouping

Only **valid sales transactions** were retained to ensure accurate performance measurement.

---

## 6. Feature Engineering

To support business analysis, the following features were created:

- **order_date** – standardized datetime column  
- **order_month** – month-level aggregation for trend analysis  
- **order_year** – year-based comparison  
- **revenue** – standardized numeric revenue field  
- **is_valid_sale** – flag identifying completed sales  

These features enable reliable KPI calculation, time-series analysis, and downstream reporting.

---

## 7. Exploratory Data Analysis (EDA)

The EDA focused on four key areas:

### 7.1 Business KPI Overview
- Total Revenue  
- Total Orders  
- Total Quantity Sold  
- Average Order Value (AOV)  
- Average Items per Order  

These KPIs establish a baseline understanding of overall business performance.

---

### 7.2 Revenue & Order Trends
- Monthly revenue trends
- Monthly order volume
- Monthly AOV trends

This analysis helps identify whether growth is driven by **order volume** or **customer spend**.

---

### 7.3 Product & Category Performance
- Revenue contribution by category
- Top-performing products by revenue and quantity
- Revenue concentration analysis to identify dependency risks

---

### 7.4 Fulfilment & Operational Insights
- Revenue by fulfilment method
- Dependency on shipping service levels
- Operational concentration risks

---

## 8. Key Insights (Summary)

- Revenue performance is primarily driven by changes in order volume rather than AOV
- A small subset of products and categories contributes a significant share of total revenue
- Sales fulfillment is concentrated through limited operational channels, creating efficiency but potential risk

---

## 9. Business Recommendations

Based on the analysis:

- Focus pricing, inventory, and marketing decisions on high-revenue categories
- Implement strategies to increase average order value through bundling or cross-selling
- Monitor and diversify fulfillment operations to reduce dependency risks
- Regularly track product performance to identify declining or emerging trends

---

## 10. Limitations & Assumptions

- Customer-level lifetime value and retention analysis were limited due to anonymized data
- Profitability analysis was constrained by incomplete cost information
- Geographic insights are based on shipping location, which may not reflect customer origin

---

## 11. Next Steps

Potential extensions of this project include:

- Customer cohort and retention analysis using SQL
- Product profitability analysis by integrating cost and expense data
- Executive dashboard development using Power BI
- Deeper geographic and operational efficiency analysis

---

