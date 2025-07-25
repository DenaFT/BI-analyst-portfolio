# 📊 Superstore Profitability Dashboard — Tableau Data Visualization Project

## 🏬 Project Overview
**Sprint 4 — Data Visualization with Tableau**  
**Program:** TripleTen Business Intelligence Analyst Bootcamp  
**Project Type:** Tableau Dashboard + Strategic Analysis  
**Prepared by:** Dena Taylor  
**Date:** August 2024

As a consultant hired by a struggling retail chain, **Superstore**, I was tasked with identifying areas of profit, loss, and customer/product inefficiencies using interactive dashboards built in **Tableau**. The objective was to uncover actionable business insights to help save the company from bankruptcy.


## 🧠 Business Challenges Addressed

1. Identify the biggest **profit and loss centers** across products, regions, and shipping methods.
2. Recommend **products and subcategories** to eliminate or invest in.
3. Determine if **advertising by state and season** is a profitable strategy.
4. Investigate **returned items** and the impact of high return rates on profitability.

---

## 🧾 Dataset: Superstore

The project used two key datasets:

- `Orders`: Transactional data, including product info, pricing, region, and profit.
- `Returns`: Dataset indicating returned items.

These tables were joined using a **LEFT JOIN** on `Order ID`.

---

## 📊 Part 1: Profits & Losses

### 🔹 Key Visualizations:
- Profit by **Sub-Category + Region**
- Profit by **Shipping Mode + Product ID**
- Product-Level Profitability

### ✅ Insights:
- **Biggest Profit Centers**: Technology products in the West and Chairs in the Central region.
- **Biggest Loss-Makers**: Bookcases and Tables had consistently negative margins.
- 📉 **Products to Stop Selling**: Identified SKUs with high volume and low-to-negative profitability.
- 🎯 **Focus Subcategories**: Accessories, Phones, and Binders showed the highest profit potential.
- ❌ **Remove Subcategories**: Tables, Supplies, and Bookcases.

---

## 💰 Part 2: Advertising Opportunities

### 🔍 Objective:
Determine where and when to advertise, using **average profit per unit** by **State + Month**.

### 📍 Top State-Month Combos:
- **California — December**
- **New York — November**
- **Texas — March**

Used **Return on Ad Spend (ROAS)** logic to define ad budget:
> If profit = \$10, then ad spend ≤ \$2 (1/5 of profit)

### 💡 Insight:
Seasonal advertising in high-performing states can yield excellent returns with minimal risk.

---

## 🔁 Part 3: Returned Items Analysis

### 🔄 Data Preparation:
- Created a **calculated field**: `Returned_flag`  
  - `Yes` = 1  
  - `null` = 0

### 🔍 Visualizations:
1. **Top Returned Products**: Highlighted products with the highest return rates.
2. **High-Risk Customers**: Identified users frequently returning items.
3. **Avg. Profit vs. Return Rate by Category**:
   - Helped balance profitability against operational risk.

### ⚠️ Insight:
Some product categories (e.g., Machines) have high profits **and** high return rates — suggesting a need for quality control or adjusted return policies.

---

## 📦 Deliverables

- ✅ Tableau Public Dashboard
- ✅ `README.md` (project summary & insights)
- ✅ Tableau Workbook (Packaged `.twbx`)
- ✅ PDF report (project documentation)
- ✅ Datasets (Superstore orders + returns)

---

## 🛠️ Tools & Skills Used

- **Tableau Desktop / Tableau Public**
- Dashboard Design & UX
- Calculated Fields & Filters
- LEFT JOINs
- Profitability & ROAS Modeling
- Visual Data Storytelling

---

## ✅ Key Takeaways

- Visual analysis helps quickly pinpoint both **profit drivers** and **financial risks**.
- **Advertising should be data-informed**, seasonal, and regionally targeted for impact.
- Return data is just as valuable as sales data for making retention and product decisions.
- Dashboard presentation matters — stakeholders need clarity, not clutter.

---

> “Dashboards don’t just report data — they tell stories that lead to action.”  
> This project demonstrates how to transform messy retail data into insights that guide smarter decisions.

---
