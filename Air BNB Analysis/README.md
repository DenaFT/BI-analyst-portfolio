# 🏙️ Manhattan Airbnb Market Analysis

## 📊 Project Overview
**Sprint 1 - Spreadsheet Data Analysis**  
**Program:** TripleTen Business Intelligence Analyst Bootcamp  
**Project Type:** Excel-Based Data Cleaning & Analysis  
**Prepared by:** Dena Taylor  
**Date:** June 2024

This project analyzes the Manhattan short-term rental market using Airbnb data. The client requested insight on the most profitable property types and neighborhoods. I used Excel to clean the data, build pivot tables, and estimate revenue in order to provide investment recommendations.

---

## 🧠 Business Objectives

The client was looking to answer the following:

1. **Which neighborhoods and property sizes are most attractive for vacation rentals?**
2. **How much money did the top listings generate?**

---

## 📌 Key Findings

### 1. Most Attractive Neighborhoods
Using the `number_of_reviews_ltm` column as a proxy for popularity, I created a pivot table of average reviews per neighborhood (after cleaning capitalization and spacing errors in the `neighbourhood` column).

🔝 **Top 3 neighborhoods for vacation rentals:**
- **Harlem**
- **Midtown**
- **East Harlem**

> These areas showed consistently high review counts, signaling strong rental demand.

### 2. Most Popular Property Sizes
After cleaning the `bedrooms` column (treating blanks as 0 = studios), I found the most popular listing sizes by volume.

🛏️ **Top 3 property sizes:**
- **1-bedroom**
- **Studios (0-bedroom)**
- **2-bedroom**

> 1-bedrooms dominated across neighborhoods, except for Midtown, where studios were most preferred.

### 3. Neighborhood Preferences by Size
To determine bedroom trends per neighborhood, I cross-referenced bedroom count with top neighborhoods.

🏘️ Example:
- In **Harlem**, 1-bedrooms were most popular.
- In **Midtown**, **studios** were most preferred.

---

## 💰 Revenue Analysis

To calculate earnings:

- I marked listings that matched **top neighborhoods** and **preferred bedroom sizes** using a binary `top_listing` column.
- Then, using the `calendar` sheet, I calculated nightly revenue by checking availability (`available = "f"`) and summing up `adjusted_price` over 30 days.
- I used `SUMIF()` to pull total revenue into the `listings` sheet and estimated **annual earnings** by multiplying by 12.

### 💵 Top-Earning Listing:
- **Listing ID:** **36425889**
- **30-Day Revenue:** \$5,006
- **Estimated Annual Revenue:** **\$60,072**

---

## 🧹 Data Cleaning Summary

| Column                | Action Taken                                             |
|-----------------------|----------------------------------------------------------|
| `neighbourhood`       | Standardized capitalization & spacing → `neighbourhood_clean` |
| `bedrooms`            | Filled blanks with 0 → `bedrooms_clean`                 |
| `calendar.available`  | Converted `"f"` into revenue, else \$0 → `revenue_earned` |
| `top_listing`         | Created binary flag for top listings                     |
| `revenue_earned`      | Aggregated using `SUMIF()` from calendar sheet           |

✅ Change log and all assumptions are documented in a separate tab.

---

## 📄 Deliverables

- ✅ Cleaned Excel Workbook  
- ✅ Pivot Tables for Neighborhoods, Bedroom Sizes, and Revenue  
- ✅ Bar chart of Top 10 Neighborhoods by Review Count  
- ✅ Visual Revenue Ranking of Top Listings  
- ✅ Final Report

---

## 🔧 Tools & Skills Applied

- **Excel Formulas**: `IF()`, `SUMIF()`, `VLOOKUP()`, etc.  
- **Pivot Tables**  
- **Data Cleaning & Validation**  
- **Revenue Modeling**  
- **Chart Building & Visualization**  
- **Professional Formatting & Documentation**

---

## 🚀 Next Steps

This project built foundational spreadsheet analysis skills. Future sprints will build on this by introducing:

- SQL querying  
- Tableau/Power BI dashboards  
- Python data manipulation  
- Predictive modeling techniques

---

> 💡 “Excel may be simple, but the insights you can uncover are powerful.”  
> This analysis helps guide smart investments in NYC’s dynamic short-term rental market.

---
