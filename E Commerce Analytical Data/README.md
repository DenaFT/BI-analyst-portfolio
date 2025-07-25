# 🛒 E-Commerce Business Analytics Project

## 📊 Project Overview
**Sprint 3 — Business Analytics**  
**Program:** TripleTen Business Intelligence Analyst Bootcamp  
**Project Type:** Spreadsheet-Based Business Metrics Analysis  
**Prepared by:** Dena Taylor  
**Date:** July 2024

As a junior analyst at an e-commerce company, I was tasked with transforming raw user activity logs into meaningful business insights. This project focused on two core areas: building a **conversion funnel** to analyze how users interact with the website and performing a **cohort analysis** to understand customer retention behavior over time.

---

## 🧠 Business Goals

- Identify website conversion efficiency from product views to purchases.
- Build user acquisition cohorts to track purchasing behavior over months.
- Calculate and visualize retention metrics.
- Deliver a clean, organized spreadsheet model suitable for executive stakeholders.

---

## 📁 Data Description

The raw dataset (`raw_user_activity` tab) contains logs of user activity including:

- `user_id`: Unique customer identifier  
- `event_type`: View, cart open, or purchase  
- `category_code`: Product category  
- `brand`: Product brand  
- `price`: Purchase price in USD  
- `event_date`: Date of event in YYYY-MM-DD format  

---

## 📈 Part 1: Conversion Funnel

A pivot table was created in the `conversion_funnel` tab to visualize user progression through three funnel stages:

1. **View Product**
2. **Add to Cart**
3. **Purchase**

Additional metrics were calculated:
- **Total Conversion Rate** (Views → Purchase)
- **Step-by-Step Conversion Rate** (Each stage → Next stage)

> 🧩 Insight: The largest drop-off occurred between the cart and purchase stages, highlighting a potential bottleneck in the checkout experience.

---

## 📆 Part 2: Preparing Cohort Data

### 🧹 Data Filtering:
- Created a new `purchase_activity` sheet with only `purchase` events (4,845 rows total).
  
### 🕐 First Purchase Date:
- Created `first_purchase` pivot table to calculate each user's earliest purchase date.
- Used `VLOOKUP()` to map `first_purchase_date` back into the `purchase_activity` tab.

### 🗓️ Time-Based Features:
New fields were created to support cohort logic:
- `event_month`: Month of the purchase event (`YYYY-MM`)
- `first_purchase_month`: Month of the user's first purchase
- `cohort_age`: Months since the first purchase (`DATEDIF()` function)

---

## 📊 Part 3: Cohort Analysis & Retention

Using the `cohort_analysis` tab:
- Grouped users into **monthly cohorts** based on first purchase
- Columns represented `cohort_age` from 0 to 4 months
- Values: Count of unique purchasers per cohort/month

In `retention_rates`:
- Calculated monthly **retention %** by dividing each month’s user count by the cohort's starting size
- Excluded cohort_age 0 (acquisition month)

> 🔎 Key Finding: Cohorts showed strongest retention within the first month, with sharp drop-offs after month 2—pointing to a need for post-purchase engagement strategies.

---

## 📋 Part 4: Executive Presentation

Organized the workbook to ensure clarity and executive usability:

| Sheet | Description |
|-------|-------------|
| `Table of Contents` | Navigational index for all sheets |
| `Executive Summary` | Key results, insights, and assumptions |
| `conversion_funnel` | Funnel visualization of user behavior |
| `retention_rates` | Cohort retention % by month |
| `cohort_analysis` | Raw counts by cohort and month |
| `first_purchase` | Pivot table of earliest purchase dates |
| `purchase_activity` | Cleaned dataset for analysis |
| `raw_user_activity` | Original raw event log data |

Formatting improvements included:
- Bold headers and grid borders
- Conditional highlighting for cohort retention
- Frozen rows/columns for readability
- Consistent date formatting (`YYYY-MM`)

---

## 🔧 Tools & Techniques Used

- **Google Sheets**
- `VLOOKUP()`, `TEXT()`, `DATEDIF()`, `UNIQUE()` functions
- Pivot tables for segmentation and aggregation
- Funnel metrics and cohort-based modeling
- Spreadsheet organization for stakeholder delivery

---

## ✅ Key Takeaways

- Identified a conversion drop-off between cart and checkout stages
- Demonstrated how monthly cohort tracking reveals churn trends
- Applied spreadsheet logic to structure, automate, and communicate key metrics
- Delivered a clean, well-documented business analysis project

---

> “What gets measured gets managed — and this project shows how raw data can become executive strategy.”  
> From event logs to insight, this sprint solidified my foundation in user behavior analytics and retention strategy.

---
