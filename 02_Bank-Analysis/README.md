<div align="center">

# 🏦 Bank Loan Analysis

### End-to-End Advanced SQL Analysis · 20+ Queries · Stored Procedures · Views · Window Functions

![MySQL](https://img.shields.io/badge/MySQL%20Workbench-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Queries](https://img.shields.io/badge/Queries-20+-blue?style=for-the-badge)
![Stored Procedures](https://img.shields.io/badge/Stored%20Procedures-4-success?style=for-the-badge)
![Views](https://img.shields.io/badge/Views-StateRanking-orange?style=for-the-badge)

<br>

![SQL Queries Preview](Screenshots/BA4.png)

<br>

> *A comprehensive bank loan analysis using advanced SQL — covering 20+ queries across EDA, customer profiling, financial risk assessment, stored procedures, views, and window functions on a real-world lending dataset.*

</div>

---

## 📑 Table of Contents

- [📌 Project Overview](#-project-overview)
- [🛠️ Tools Used](#️-tools-used)
- [🖼️ SQL Query Screenshots](#️-sql-query-screenshots)
- [💡 Key Business Insights](#-key-business-insights)
- [📂 Project Structure](#-project-structure)
- [🗃️ Dataset](#️-dataset)
- [👤 Author](#-author)

---

## 📌 Project Overview

This project performs an **end-to-end SQL analysis** on a bank lending dataset (`finance1` + `finance2`) to understand loan performance, customer risk profiles, default patterns, and business insights across **US states, loan grades, and purposes**.

### 🎯 Key Business Questions Answered

| # | Question |
|---|----------|
| 1️⃣ | What is the overall **loan portfolio composition** and **default rate**? |
| 2️⃣ | Which **states and loan grades** carry the highest financial risk? |
| 3️⃣ | How do **verified vs non-verified** customers compare in loan behavior? |
| 4️⃣ | What are the **top loan purposes** and their funded amounts? |
| 5️⃣ | Which customers have the highest **Debt-to-Income (DTI)** ratio? |

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| ![MySQL](https://img.shields.io/badge/MySQL%20Workbench-4479A1?style=flat-square&logo=mysql&logoColor=white) | All analysis — EDA, financial analysis, stored procedures, views, window functions |

---

## 🖼️ SQL Query Screenshots

| Query Set | Preview |
|-----------|---------|
| 🔍 **Basic EDA — 10 queries** | ![EDA](Screenshots/BA4.png) |
| 💳 **Customer & Financial Analysis** | ![Financial](Screenshots/BA5.png) |
| 📈 **Business Insight queries** | ![Business](Screenshots/BA6.png) |
| ⚙️ **Stored Procedures — Loan Profile + Grade Analysis** | ![SP1](Screenshots/BA1.png) |
| 🧠 **Master Stored Procedure — 4 result tables in 1 CALL** | ![SP2](Screenshots/BA2.png) |
| 🏆 **StateRanking VIEW with DENSE_RANK** | ![View](Screenshots/BA3.png) |

---

## 💡 Key Business Insights

### 🔍 Basic EDA Findings

- 📦 Total loans, unique customers, and distinct states extracted in single queries
- 🗺️ `GROUP_CONCAT(DISTINCT addr_state)` used to get all state names + count in one query
- 🏷️ Loans broken down by **grade** (A–G) and **purpose** (debt consolidation, credit card, home improvement etc.)
- 🥇 Top 10 states by total loan amount identified
- 📊 Avg loan amount and avg interest rate calculated across the portfolio

---

### 💳 Customer & Financial Analysis

- ⚠️ **Loan default rate** calculated per state using `SUM(CASE WHEN loan_status='Charged Off')` / COUNT(*)
- 🏅 **Grade-wise avg loan amount** — higher grades (A, B) tend to have lower avg loan amounts
- 🏠 **Income by home ownership** — RENT vs MORTGAGE vs OWN comparison
- 💹 **Grade-wise interest rates** — using `REPLACE(int_rate,'%','')` to convert string % to numeric for AVG calculation

---

### 📈 Business Insights

- 🎯 **Top purposes by funded amount** — debt consolidation dominates
- ✅ **Verified vs Non-Verified customers** — comparison of avg loan, avg income, count
- 🚨 **Highest DTI customers** — top 10 riskiest customers identified
- ⚖️ **Fully Paid vs Charged Off** — side-by-side comparison of avg loan, avg income, avg DTI
- 🗺️ **State-wise avg income** — geographic income distribution
- 📅 **Monthly installment trends** by issue date

---

### 🏆 StateRanking VIEW Output

| Risk Rank | State | Default Rate |
|:---------:|:-----:|-------------:|
| 🥇 1 | **NE** | **60.00%** |
| 🥈 2 | **NV** | **21.73%** |
| 🥉 3 | **AK / SD** | **18.75%** |
| 9 | **CA** | **15.85%** *(7,099 total loans)* |

---

### ⚙️ Stored Procedures

| Procedure | What It Does |
|:----------|:-------------|
| **`Loan_Profile(p_id INT)`** | Full loan profile for any customer by ID (JOIN finance1 + finance2) |
| **`GradeAnalysis(p_grade VARCHAR)`** | Returns loans count, avg loan, avg income, avg interest rate for any grade |
| **`Loan_Status(a VARCHAR)`** | State-wise breakdown for any loan status (Fully Paid / Charged Off / Current) |
| **`MASTER_SP(p_state VARCHAR)`** | Returns **4 result tables in a single CALL**: State KPI, Grade Distribution, Top 5 Purposes, Loan Status Summary |

---

## 📂 Project Structure

```
07_Bank-Analysis/
│
├── README.md                      ← You are here
│
├── raw-data/
│   └── README.md
│
├── sql/
│   ├── Bank_Analysis.sql          ← All 20+ queries
│   └── README.md
│
└── Screenshots/
    ├── BA1.png                    ← Stored Procedures: Loan_Profile + GradeAnalysis
    ├── BA2.png                    ← Master SP: 4 result tables in one CALL
    ├── BA3.png                    ← StateRanking VIEW with DENSE_RANK output
    ├── BA4.png                    ← Basic EDA — 10 queries
    ├── BA5.png                    ← Customer & Financial Analysis
    └── BA6.png                    ← Business Insight queries
```

---

## 🗃️ Dataset

| Field | Details |
|:------|:--------|
| **Source** | Bank Loan / Lending Club Dataset |
| **Tables** | `finance1` (loan info), `finance2` (financial details) |
| **Join Key** | `finance1.id = finance2.id` |
| **Key Fields** | id, member_id, loan_amnt, funded_amnt, int_rate, installment, grade, sub_grade, emp_title, emp_length, home_ownership, annual_inc, verification_status, issue_d, loan_status, purpose, addr_state, dti |

---

## 👤 Author

<div align="center">

### **Dishant Bhere**

**Data Analyst**

![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=flat-square&logo=tableau&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat-square&logo=microsoftexcel&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)

⭐ *If you found this useful, consider giving the repo a star!*

</div>
