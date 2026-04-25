# 📦 Amazon Sales Performance Analysis (2022–2023)

---

## 📌 Overview

This project presents an end-to-end analysis of Amazon's sales performance data spanning **2022 to 2023**. Using Python for data cleaning and exploratory data analysis (EDA), alongside an interactive Power BI dashboard, this project uncovers trends in revenue, customer behavior, regional distribution, and product performance to support data-driven business decisions.

**Key Metrics at a Glance:**

| Metric | Value |
|---|---|
| Total Revenue | $32.87M |
| Total Orders | 50K |
| Average Order Value (AOV) | $657.33 |
| Avg Monthly Growth | -0.05% |
| Revenue YTD | $16.48M |

---

## 🗂️ Background

E-commerce platforms like Amazon generate vast amounts of transactional data on a daily basis. Understanding sales patterns, customer preferences, and payment behavior is critical for strategic planning and performance optimization.

This analysis is based on the `amazon_sales_dataset.csv`, which contains order-level data including:
- **Order date** — timestamp of each transaction
- **Product category** — type of product sold (Beauty, Books, Fashion, Home & Kitchen, Electronics, Sports)
- **Customer region** — geographic region of the buyer (Asia, Europe, Middle East, North America)
- **Payment method** — mode of payment used (Wallet, UPI, Cash on Delivery, Credit Card, Debit Card)
- **Price & Discounted Price** — original and final selling price
- **Total Revenue** — revenue generated per order

The dataset covers **2 fiscal years (2022–2023)** and includes **50,000 transactions** across multiple regions and product categories.

---

## 🔍 Exploratory Data Analysis (EDA)

The EDA pipeline was implemented in Python using `pandas`, `numpy`, `matplotlib`, and `seaborn`.

### A. Data Cleaning

Before analysis, the following cleaning steps were performed:

- **Duplicate Check** — Scanned and removed any duplicate rows to ensure data integrity.
- **Missing Value Handling** — Verified that all columns had no null/missing values.
- **Data Type Correction** — Converted the `order_date` column from `object` to `datetime` format for time-series analysis.

### B. Feature Engineering

New features were derived from existing columns to enrich the analysis:

- **Temporal Features** — Extracted `year`, `month`, and `day_name` from `order_date` to enable time-based aggregations.
- **Discount Amount** — Computed as `price - discounted_price` to quantify the discount given per order.

### C. EDA & Visualizations

**1. Variable Correlation Analysis**
A heatmap of the correlation matrix across all numerical features was generated to identify relationships between variables such as price, quantity, discount, and total revenue.
![Variable Correlation Analysis](images/Variable%20Correlation%20Analysis.png)

**2. Revenue by Product Category**
A horizontal bar chart visualized total revenue per product category, revealing which categories drive the most sales.
![Revenue by Product Category](images/Revenue%20by%20Product%20Category.png)

**3. Sales Trend Over Time**
A monthly time-series line chart tracked revenue fluctuations from January 2022 to December 2023, highlighting seasonal peaks and troughs.
![Sales Trend Over Time](images/Sales%20Trend%20Over%20Time.png)

**4. Customer Shopping Activity by Day of Week**
A count plot analyzed transaction frequency across each day of the week to identify peak shopping days.
![Customer Shopping Activity by Day of Week](images/Customer%20Shopping%20Activity%20by%20Day%20of%20Week.png)

---
## 📊 Dashboard Overview

![Dashboard](images/dashboard.png)

---

## 💡 Key Business Insights

### 1. 📅 Revenue Trend is Relatively Stable, but Growth is Stagnant
Monthly revenue hovers around **~$1M** throughout both years, with an average monthly growth rate of **-0.05%**. This flat trend suggests the business has reached a plateau and requires growth-oriented strategies to drive meaningful revenue increases.

### 2. 🛍️ Product Categories are Nearly Equally Distributed
All six product categories — **Beauty, Books, Fashion, Home & Kitchen, Electronics, and Sports** — contribute similarly to total revenue, ranging from **$5.4M to $5.6M**. This indicates a well-diversified product portfolio with no single dominant category.

### 3. 🌍 Revenue is Balanced Across Regions
All four regions — **Middle East ($8.3M), North America ($8.3M), Asia ($8.2M), and Europe ($8.1M)** — contribute almost equally to total revenue. This reflects strong global reach with consistent market penetration across geographies.

### 4. 💳 Payment Methods are Evenly Split
No single payment method dominates: **Wallet (20.32%), Credit Card (20.02%), Debit Card (19.92%), Cash on Delivery (19.90%), and UPI (19.84%)** are all nearly equally preferred. This suggests customers have diverse payment preferences, and supporting all channels is critical to avoid losing sales.

### 5. 📉 Notable Revenue Dip in February 2023
A visible dip in revenue occurred in **February 2023**, which may correlate with seasonal factors, lower promotional activity, or supply chain disruptions. This warrants further investigation.

---

## ✅ Conclusion

The Amazon Sales Performance analysis reveals a **stable but stagnant business** with strong diversification across products, regions, and payment methods. While the balanced distribution across dimensions is a sign of resilience, the near-zero monthly growth rate signals an urgent need for strategic interventions.

**Recommended next steps:**
- Launch **targeted promotions** during low-revenue months (e.g., February) to smooth out seasonal dips.
- Investigate high-performing subcategories within each product group to identify growth drivers.
- Consider region-specific campaigns — while revenue is balanced, growth opportunities may exist in underpenetrated markets.
- Leverage the diversity of payment methods as a competitive advantage in marketing campaigns.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python (pandas, numpy) | Data cleaning & feature engineering |
| Matplotlib & Seaborn | EDA visualizations |
| Power BI | Interactive sales dashboard |
| Jupyter Notebook | Analysis environment |

---

## 📁 Project Structure

```
amazon_sales_performance/
│
├── data/
│   └── amazon_sales_dataset.csv
│
├── notebooks/
│   └── data_cleaning_and_eda.ipynb
│
├── dashboard/
│   └── amazon_sales_performance.pbix
│
└── README.md
```

---

> **Author:** *Muh. Salim Maulana*
> **Last Updated:** April 2026
