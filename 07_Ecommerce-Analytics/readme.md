# 🛒 Ecommerce Analytics Dashboard

![Dashboard Preview](Screenshots/2.%20Executive%20Overview.png)

<p align="center">
  <img src="https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black">
  <img src="https://img.shields.io/badge/DAX-Advanced-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Transactions-1,000-success?style=for-the-badge">
  <img src="https://img.shields.io/badge/Report%20Pages-6-purple?style=for-the-badge">
</p>

> **Self-Made Project** | Portfolio Project  
> A 6-page interactive Power BI dashboard analyzing 1,000 ecommerce transactions across Jan 2024 – Dec 2025, covering revenue, profit, customer behaviour, returns, and marketing performance using DAX, Power Query, and field parameters.

---

## 📌 Project Overview

An end-to-end ecommerce analytics project exploring profitability, customer retention, return orders, and marketing effectiveness through six interactive Power BI dashboard pages.

## ❓ Business Questions Answered

| # | Business Question |
|:--:|---|
| 1 | Which categories and products drive revenue vs. profit, and where do discounts cause losses? |
| 2 | Who are the highest-value customers, and how much revenue comes from repeat buyers? |
| 3 | What drives returns, and which categories or shipping modes impact profitability? |
| 4 | Which marketing channels perform best, and how does seasonality influence sales? |

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Interactive dashboard, DAX, data modeling, and field parameters |
| **Power Query** | Data transformation and formatting |
| **DAX** | 20+ measures and calculated columns |
| **Microsoft Excel** | Raw dataset source |

---

## 📊 Dashboard Pages

### 🏠 Page 1 — Home
![Home](Screenshots/1.%20Home.png)

Navigation landing page linking to all five report pages.

### 📈 Page 2 — Executive Overview
![Executive Overview](Screenshots/2.%20Executive%20Overview.png)

| KPI | Value |
|---|---:|
| Total Revenue | 236.76K |
| Total Profit | 66.19K |
| Total Orders | 1,000 |
| Total Customers | 326 |
| Profit Margin | 27.96% |
| Return Rate | 8.20% |

**Visuals:** Monthly revenue/profit trends, category and country revenue, regional performance, and country/city table.

### 💰 Page 3 — Revenue & Profit Analysis
![Revenue & Profit](Screenshots/3.%20Revenue%20&%20Profit%20Analysis.png)

**Additional KPIs:** Total Cost (170.57K) · Average Selling Price (169.78)

**Visuals:** Revenue ↔ Profit toggle, profit by sub-category, category, and payment method, top/bottom 5 products, and profit by discount bucket.

### 👥 Page 4 — Customer Analysis
![Customer Analysis](Screenshots/4.%20Customer%20Analysis.png)

| KPI | Value |
|---|---:|
| Revenue per Customer | 726.27 |
| Orders per Customer | 3.07 |
| Repeat Customers | 275 of 326 (84%) |
| Repeat Customer Revenue | 225K (95.2%) |
| One-Time Customers | 51 |

**Visuals:** Payment methods, customer types, customer segments, average order value, and top customers.

### 🔄 Page 5 — Return Orders Insight
![Return Orders](Screenshots/5.%20Return%20Orders.png)

| KPI | Value |
|---|---:|
| Total Return Orders | 82 |
| Return Rate | 8.20% |
| Lost Revenue | 18.37K |
| Lost Profit | 5.12K |

**Visuals:** Return rate by category and shipping mode, profit loss analysis, monthly returns, and shipping performance.

### 📣 Page 6 — Marketing & Seasonal Analysis
![Marketing & Seasonal](Screenshots/6.%20Marketing%20&%20Seasonal%20Insights.png)

| KPI | Value |
|---|---|
| Top Marketing Channel | Organic Search |
| Top Sales Month | December |

**Visuals:** Channel revenue/profit, average order value, weekday vs. weekend sales, quarterly trends, and customer count.

---


## 🧮 DAX Measures & Calculated Columns

### Key Measures

| Measure | Description |
|---|---|
| `Total Revenue` | Sum of net revenue |
| `Total Profit` | Sum of profit |
| `Total Cost` | Unit cost × quantity |
| `Total Orders` | Distinct count of order IDs |
| `Total Customers` | Distinct count of customer IDs |
| `Average Order Value` | Revenue / Orders |
| `Profit Margin %` | Profit / Revenue × 100 |
| `Avg Selling Price` | Revenue / Quantity |
| `Return Rate %` | Return Orders / Total Orders × 100 |
| `Profit Lost to Returns` | Profit associated with returned orders |
| `Net Profit Excl Returns` | Total Profit − Profit Lost |
| `Revenue from Repeat Customers %` | Repeat Revenue / Total Revenue |
| `Revenue per Customer` | Revenue / Customers |
| `Orders per Customer` | Orders / Customers |
| `Loss Making Orders Count` | Orders with profit < 0 |
| `Loss Making Orders %` | Loss Orders / Total Orders |
| `Avg Discount on Loss Orders` | Average discount on loss-making orders |

### Calculated Columns

| Column | Logic |
|---|---|
| `Discount Bucket` | 0–5%, 5–10%, 10–15%, 15–20%, 20%+ |
| `Customer Type` | Repeat vs. One-time |
| `Customer Order Count` | Orders per customer |

### Field Parameters
- **Revenue ↔ Profit Toggle:** Dynamically switches visuals between revenue and profit.

---

## 📁 Project Structure

```text
Ecommerce-Analytics-Dashboard/
│
├── README.md
├── raw-data/
│   ├── ecommerce data.xlsx
│   └── README.md
├── powerbi/
│   ├── Ecommerce Analytics.pbix
│   └── README.md
└── Screenshots/
    ├── Home.png
    ├── Executive Overview.png
    ├── Revenue Profit.png
    ├── Customer Analysis.png
    ├── Return Orders.png
    ├── Marketing Seasonal.png
    └── README.md
```

---

## 🎯 Skills Demonstrated

| Skill | Application |
|---|---|
| **DAX** | KPIs, return analysis, customer segmentation, discount impact |
| **Power Query** | Data transformation and formatting |
| **Data Modeling** | Fact table and dimension relationships |
| **Field Parameters** | Dynamic Revenue ↔ Profit toggle |
| **Business Analysis** | Profitability, retention, returns, and marketing |
| **Dashboard Design** | Six-page navigation, slicers, KPI cards, and conditional formatting |



## 👤 Author

**Dishant Bhere**  
*Data Analyst | SQL · Power BI · Tableau · Excel · Python*

