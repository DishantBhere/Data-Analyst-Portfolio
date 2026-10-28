# 🚗 BMW Sales Analytics Dashboard

![Landing Page](Screenshots/1.%20Home.png)

<p align="center">
  <img src="https://img.shields.io/badge/Tableau-Dashboard-E97627?style=for-the-badge&logo=tableau&logoColor=white" alt="Tableau">
  <img src="https://img.shields.io/badge/PowerPoint-Custom%20Design-B7472A?style=for-the-badge&logo=microsoftpowerpoint&logoColor=white" alt="PowerPoint">
  <img src="https://img.shields.io/badge/Models-6-1C69D3?style=for-the-badge" alt="6 Models">
  <img src="https://img.shields.io/badge/Records-200-2ECC71?style=for-the-badge" alt="200 Records">
</p>

> A 7-page professional Tableau dashboard analyzing BMW sales across 6 models and 4 regions. Features custom PowerPoint-designed backgrounds, a premium BMW dark blue theme, and interactive metric and dimension selectors.

**📊 200 Records · 🚘 1,974 Units Sold · 💰 $117.28M Revenue**

---

## 📌 Project Overview

An interactive BMW sales analytics project exploring model performance, regional sales, revenue, and profitability through seven dashboard pages.

**Key business questions answered:**
- Which BMW model generates the most revenue and profit?
- How do the four regions compare in sales and profitability?
- Which model has the highest profit margin?
- What is the relationship between units sold and profit?
- How are prices and unit volumes distributed?

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| **Tableau Desktop** | Interactive dashboards, parameters, calculated fields, and visualizations |
| **Microsoft PowerPoint** | Custom backgrounds with a premium BMW dark blue theme |

---

## 📊 Dashboard Pages

### 🏠 Page 1 — Landing / Home
![Home](Screenshots/1.%20Home.png)

BMW branding, six navigation cards, dataset summary, and key business KPIs.

### 📈 Page 2 — Executive Overview
![Overview](Screenshots/2.%20Overview.png)

Five KPIs, revenue by model and region, sales trends, and interactive filters.

### 🚘 Page 3 — Model Analysis
![Model](Screenshots/3.%20Model.png)

Model-wise units sold, revenue, profit, average price, and performance KPIs.

### 🗺️ Page 4 — Region Analysis
![Region](Screenshots/4.%20Region.png)

Regional units, revenue, profit, and model-wise comparisons.

### 💰 Page 5 — Revenue & Profit
![Revenue](Screenshots/5.%20Revenue%20&%20Profit.png)

Revenue versus profit, total cost, profit margins, and profit distribution by model and region.

### 📉 Page 6 — Time Analysis
![Time](Screenshots/6.%20Time%20Analysis.png)

Price and unit distributions, histograms, and a profit-versus-units scatter plot.

### ⚡ Page 7 — Quick Analysis
![Quick](Screenshots/7.&20Quick%20Analysis.png)

Dynamic analysis using metric and dimension selectors, a KPI card, and a distribution donut chart.

---

## 🔑 Key Business Insights

### 📊 Overall KPIs

| Metric | Value |
|---|---:|
| Total Revenue | $117,285,097 |
| Total Cost | $84,406,943 |
| Total Profit | $32,878,154 |
| Units Sold | 1,974 |
| Average Price per Car | $59,361 |
| Profit Margin | 28.03% |
| Average Profit per Record | $164,391 |
| Total Records | 200 |

### 🚘 Model Performance

| Model | Units | Revenue | Profit | Margin |
|---|---:|---:|---:|---:|
| BMW X3 | 421 | $25.27M | $7.16M | 28.34% |
| BMW 7 Series | 364 | $22.52M | $6.37M | 28.28% |
| BMW X1 | 385 | $22.51M | $6.76M | **30.02%** |
| BMW 3 Series | 355 | $21.37M | $5.89M | 27.55% |
| BMW 5 Series | 236 | $13.91M | $3.47M | 24.93% |
| BMW X5 | 213 | $11.71M | $3.24M | 27.64% |

- **BMW X3:** Highest revenue and unit sales.
- **BMW X1:** Highest profit margin at 30.02%.
- **BMW 5 Series:** Lowest profit margin at 24.93%.
- **BMW 7 Series:** Highest average price at $62,533.

### 🗺️ Regional Performance

| Region | Units | Revenue | Profit |
|---|---:|---:|---:|
| North | 560 | $33.76M | $9.00M |
| West | 482 | $30.49M | $8.33M |
| South | 474 | $27.57M | $8.07M |
| East | 458 | $25.46M | $7.48M |

- **North:** Leads in units, revenue, and profit.
- **East:** Lowest regional sales and profit, indicating a potential growth opportunity.
- **Regional distribution:** Sales are spread relatively evenly across the four regions.

### 🏆 Top 10 Records by Profit

| Rank | Model | Region | Units | Price | Profit |
|---:|---|---|---:|---:|---:|
| 1 | BMW 7 Series | West | 19 | $85,766 | $640,571 |
| 2 | BMW X1 | South | 18 | $89,383 | $589,493 |
| 3 | BMW 7 Series | East | 16 | $82,796 | $529,035 |
| 4 | BMW X1 | East | 17 | $76,540 | $499,812 |
| 5 | BMW 7 Series | North | 17 | $72,675 | $482,195 |
| 6 | BMW X1 | North | 18 | $76,975 | $448,446 |
| 7 | BMW X3 | South | 13 | $87,010 | $443,564 |
| 8 | BMW X3 | West | 18 | $63,307 | $433,665 |
| 9 | BMW X3 | West | 16 | $89,150 | $407,925 |
| 10 | BMW X3 | South | 19 | $58,312 | $400,227 |

### 📈 Distribution Insights

- **Price range:** $30,009–$89,581.
- **Units per record:** 1–19, averaging 9.87.
- **Profit vs. units:** Positive relationship between units sold and profit.
- **Highest-profit record:** $640,571 from a BMW 7 Series record in the West.
- **Time analysis:** No time-based fields are available in the dataset.

---

## 🧮 Calculated Fields Used

| Field | Purpose |
|---|---|
| `Revenue` | `[Price] * [Units Sold]` |
| `Total Cost` | `[Cost] * [Units Sold]` |
| `Profit Margin %` | `SUM([Profit]) / SUM([Revenue]) * 100` |
| `Avg Revenue per Car` | `SUM([Revenue]) / SUM([Units Sold])` |
| `Price Range` | Budget / Mid-Range / Premium / Luxury |
| `Unit Range` | Low / Medium / High / Very High |
| `Profit Tier` | Low / Medium / High / Top |
| `Row Number` | `INDEX()` |
| `Selected Metric Value` | Dynamic calculation using the metric parameter |
| `Selected Dimension` | Dynamic calculation using the dimension parameter |

---

## 📁 Project Structure

```text
13_BMW-Sales-Analytics/
│
├── README.md
│
├── data/
│   ├── bmw_sales_dataset.xlsx
│   └── README.md
│
├── tableau/
│   ├── tableau_link.txt
│   └── README.md
│
├── background/
│   ├── BMW_Dashboard_Background_1668x861.pptx
│   └── README.md
│
└── Screenshots/
    ├── BMW_Home.png
    ├── BMW_Overview.png
    ├── BMW_Model.png
    ├── BMW_Region.png
    ├── BMW_Revenue.png
    ├── BMW_Time.png
    ├── BMW_Quick.png
    └── README.md
```

---

## 📂 Dataset

| Property | Value |
|---|---|
| **Source** | BMW Sales Dataset |
| **File** | `bmw_sales_dataset.xlsx` |
| **Records** | 200 |
| **Columns** | 6 |
| **Models** | BMW X1, X3, X5, 3 Series, 5 Series, 7 Series |
| **Regions** | North, South, East, West |
| **Price Range** | $30,009–$89,581 |
| **Units Range** | 1–19 per record |

---

## 🎨 Design Details

| Element | Specification |
|---|---|
| Theme | BMW Premium Dark Blue |
| Design Tool | Microsoft PowerPoint |
| Dashboard Size | 1668 × 861 px |
| BMW Blue | `#1C69D3` |
| Navy Background | `#0A1929` |
| Profit | `#2ECC71` |
| Cost | `#E74C3C` |
| Text | `#FFFFFF` |
| Sidebar | `#0F3460` |

---

## 🌐 Live Dashboard

🔗 [**View BMW Sales Analytics on Tableau Public**](https://public.tableau.com/app/profile//viz/BMWSalesAnalytics_17828850435440/HOME)

---

## 👤 Author

**Dishant Bhere**  
*Data Analyst | SQL · Power BI · Tableau · Excel · Python*
