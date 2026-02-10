# 📊 Amazon Sales Analysis (Python | Pandas | EDA)

## 📌 Project Overview

This project analyzes Amazon sales data to uncover **revenue drivers, demand patterns, and growth opportunities** across **time, geography, and product categories**.
The focus is on **data cleaning, KPI creation, and business insights**, not just visualization.

---

## 🎯 Business Objective

To answer:

* How is revenue trending over time?
* Which categories and states drive most sales?
* Where are the biggest growth and risk areas?

---

## 🗂️ Dataset

* **Source:** Amazon Sales Report
* **Rows:** ~129,000 order-line records
* **Granularity:** Order-line level (multiple rows per order)
* **Time Period:** March–June 2022

### Key Columns

* `Order ID`, `Date`, `Qty`, `revenue`
* `Category`, `SKU`, `Style`
* `ship_state`
* `is_valid_sale`, `B2B`

---

## 🧹 Data Cleaning & Preparation

Key issues addressed:

* Cancelled orders and zero-quantity rows
* Inconsistent state names (`RAJASTHAN`, `RJ`, `rajasthan`)
* Missing and inconsistent categorical values
* Incorrect KPI calculations due to order-line granularity

### Cleaning Actions

* Created `is_valid_sale` to isolate completed sales
* Standardized Indian state names into a clean `ship_state` column
* Rebuilt date features (`order_month`, `order_year`)
* Removed intermediate helper columns after validation

📌 Result: **Analysis-ready dataset with preserved business logic**

---

## 📐 KPIs Defined (Sales Only)

| Metric                    | Value   |
| ------------------------- | ------- |
| Total Revenue             | ₹78.6M  |
| Total Orders              | 120,378 |
| Total Quantity Sold       | 116,649 |
| Average Order Value (AOV) | ₹652.88 |
| Avg Items per Order       | 1.08    |

🔍 *Important Fix:*
Average items per order was initially incorrect (<1) due to order-line granularity.
This was corrected by aggregating quantity at the **order level**.

---

## 📈 Time-Based Analysis

* Revenue peaked in **April** and declined through **June**
* Decline driven by **lower order volume**, not lower AOV
* AOV increased in May and June → shift toward higher-value purchases

**Charts Created**

* Monthly Revenue (Line & Bar)
* Monthly Orders
* Monthly AOV
* Month-over-Month Revenue Growth

---

## 🧵 Category Analysis

Top revenue contributors:

* **Set** (~50%)
* **Kurta**
* **Western Dress**

📌 Insight:

> Top 3 categories contribute ~93% of total revenue, indicating strong category concentration.

---

## 🗺️ Geographic Analysis

### Top Revenue States

* Maharashtra (17.2%)
* Karnataka (13.5%)
* Telangana
* Uttar Pradesh
* Tamil Nadu

➡️ **Top 5 states contribute ~56% of revenue**

### High-AOV, Low-Volume States

* Ladakh
* Nagaland
* Lakshadweep

📌 Insight:

> Large states drive scale, while smaller states exhibit premium purchasing behavior.

---

## 💡 Key Insights

* Revenue is highly concentrated across a few categories and states
* Order volume declined, but AOV increased over time
* Strong dependency on Tier-1 states poses moderate concentration risk
* Long-tail categories contribute minimal revenue

---

## 📊 Business Recommendations

* Increase basket size via bundling and cross-selling
* Focus marketing spend on high-performing categories (Set, Kurta)
* Expand mid-tier states to reduce geographic dependency
* Rationalize or reposition low-performing categories

---

## 🛠️ Tools & Skills Used

* Python
* Pandas
* Matplotlib
* Exploratory Data Analysis (EDA)
* Data Cleaning & Validation
* KPI Design
* Business Insight & Storytelling

---

## 🚀 How to Run This Project

```bash
pip install pandas matplotlib
```

```python
import pandas as pd
import matplotlib.pyplot as plt
```

Open the notebook and run cells sequentially.

---

## 📌 Resume Bullet (Example)

> Analyzed 129K+ Amazon sales records using Python to identify revenue drivers by time, category, and geography; built KPIs, cleaned messy address data, and delivered actionable business insights.

---

## 📎 Next Improvements

* Power BI / Tableau dashboard
* SKU-level 80/20 (Pareto) analysis
* B2B vs B2C comparison
* Profitability analysis (if cost data available)

---

### ⭐ If you like this project

Feel free to ⭐ the repo or fork it!

Just tell me the next number 👌
