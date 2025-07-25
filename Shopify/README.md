# 📦 Shopify Returns Analysis — Storytelling with Data in Tableau

## 🧾 Project Overview
**Sprint 5 — Storytelling with Data**  
**Program:** TripleTen Business Intelligence Analyst Bootcamp  
**Project Type:** Data Analysis + Dashboard Design + Data Storytelling  
**Prepared by:** Dena Taylor  
**Date:** August 2024  

This project focused on helping the CEO of a large e-commerce company (Shopify Superstore) understand the **root causes of customer returns** and how to reduce them. Using Tableau, I designed interactive visuals, built a structured dashboard, and delivered an executive-ready narrative that walks through data-backed findings.

## 🎯 Project Objective

- Identify key patterns and causes behind returned orders
- Visualize return behavior by product, customer, geography, and time
- Build a dashboard for executive monitoring and decision-making
- Present findings using a data-driven story arc in Tableau

---

## 📂 Data Overview

- **Orders**: Product-level sales data including region, category, date, and profit
- **Returns**: Order IDs with return status

📌 Joined using a **LEFT JOIN** on `Order ID`

### 📐 Calculated Field for Return Tracking:
```text
IF [Returned] = "Yes" THEN 1 ELSE 0 END
This field was used to calculate:

Return Rate → AVG(Returned Flag)

Total Returns → SUM(Returned Flag)

## 📊 Exploratory Visualizations
📌 Worksheets Created:
Visualization	Chart Type	Purpose
Return Rate vs Total Sales	Scatterplot by Subcategory	Do more sales mean more returns?
Return Rate by Category	Bar Chart	Spot product lines with high returns
Return Rate by Customer	Filtered Table	Identify high-returning customers
Returns by Region	Geographic Map	Pinpoint geographic concentrations
Return Trends Over Time	Line Chart by Month	Spot seasonal return behavior
Composite Views	Dual-Axis / Trellis Charts	Blend multiple return factors (e.g., Category + State)

💡 Insight: Certain categories (e.g., Technology, Office Supplies) had high return rates, especially during Q4. Some customers returned more than 30% of their orders, and return behavior was more concentrated in certain regions (e.g., California, New York).

## 📐 Dashboard Design
## 📝 Mockups & Template
Designed 3 low-fidelity dashboard mockups on paper

Chose final layout based on clarity and alignment with executive priorities

Created a container-based layout in Tableau

## 🧩 Final Dashboard Features:
Map of returns by state

Monthly return trend line

Return rate by product category and subcategory

Filterable customer-level return table

KPI summary cards

## 📖 Storytelling & Presentation
Built a Tableau Story with the following narrative arc:

Overview Slide — Why returns matter, how they’re measured

Root Cause Breakdown:

Sales vs Returns

Category and Customer return rates

Geography and Seasonality

Dashboard Walkthrough:

How to use filters

What each chart means

Actionable Insights:

Products to review or retire

Customers to flag for return behavior

Seasonal return trends to prepare for

Conclusion & Recommendations:

Monitor with dashboard

Revisit return policy thresholds

Implement quality checks in Q4

## 🎤 Final Presentation:
Submitted as a narrated 3–5 minute screen recording of the Tableau Story (or PDF version).

## 📁 Files Included
File	Description
README.md	This project summary
Shopify_Returns.twbx	Tableau packaged workbook
Mockups/	3 scanned dashboard mockups
Dashboard_Template.png	Screenshot of empty container layout
Shopify.pdf	Written project analysis
Tableau_Story_Captions.twbx	Story Points version
Presentation.mp4 (optional)	Executive walkthrough (recording)

## 🛠 Tools & Skills Used
Tableau Public / Desktop

LEFT JOINs & calculated fields

KPI creation & filtering

Story Points for narrative flow

Executive communication & dashboard design

## ✅ Key Takeaways
Return behavior is influenced by product type, customer history, seasonality, and location

Not all returns are created equal — use return rate rather than total returns for actionable insight

Dashboards should enable self-service exploration by leadership, not just report snapshots

Storytelling with data creates engagement and clarity for non-technical stakeholders

“Data informs. Storytelling inspires action.”
This project was a comprehensive dive into using visual analytics and storytelling to drive smarter business decisions.
