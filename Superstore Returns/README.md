# 🔄 Superstore Returns Analysis — Storytelling with Data in Tableau

## 🧾 Project Overview
**Sprint 5 — Storytelling with Data**  
**Program:** TripleTen Business Intelligence Analyst Bootcamp  
**Project Type:** Return Behavior Analysis + Dashboard Design + Storytelling  
**Prepared by:** Dena Taylor  
**Date:** August 2024  

The Superstore is experiencing a high volume of returned orders. As a business analyst, I was tasked with uncovering the **root causes** of these returns and presenting the findings to the CEO through an **interactive Tableau dashboard** and a structured narrative story.


## 🎯 Project Objective

- Determine **what’s causing the high number of returned orders**
- Analyze return rates by multiple dimensions (product, customer, geography, time)
- Deliver insights via a compelling **storytelling framework**
- Provide executives with a **dashboard** they can use to monitor and act on return trends

---

## 📂 Data Sources

- `Orders`: Transactional data including sales, products, categories, locations, and dates
- `Returns`: Binary return status indicating whether a product was returned

These two tables were merged via a **LEFT JOIN** on `Order ID`.

---

## 🔎 Part 1: What’s Causing Returns?

### ✅ Data Preparation
- Created a calculated field:
  ```text
  Returned_flag = IF [Returned] = "Yes" THEN 1 ELSE 0 END
Used AVG(Returned_flag) to calculate return rates

Used SUM(Returned_flag) to calculate total returns

### 📊 Key Worksheets Created
View	Chart Type	Purpose
Sales vs Returns	Scatterplot by Subcategory	Explore correlation between volume and return rate
Return Rate by Category	Bar Chart	Identify most problematic product categories
Return Rate by Customer	Filtered Table	Detect repeat returners (excluding 1-time buyers)
Geographic Return Rates	Map by State	Reveal regional return hotspots
Seasonal Trends	Line Chart (Monthly)	Spot return spikes over time
Composite Factors	Dual-axis & trellis charts	Combine factors like region + subcategory or date + category

🔍 Insight: Office Supplies and Technology had high returns in Q4. Certain customer segments returned products disproportionately.

## 📐 Part 2: Dashboard Design
✏️ Low-Fidelity Mockups
Sketched 3 versions of the dashboard using pen and paper

Chose the clearest layout with filters and interactive charts

Submitted scanned photos of the mockups

### 🧩 Final Dashboard Structure
Built in Tableau using layout containers

Added calculated fields, titles, legends, filters

Focused on executive usability with drill-down filters and tooltips

Final Features:
Interactive Map + Line Charts

Category breakdowns with color-coded return rates

Customer-focused filters

Clear navigation and usability

## 📖 Part 3: Storytelling & Executive Presentation
Story Arc Includes:
Problem Overview — What is the issue? How are returns measured (rate, volume, cost)?

Root Cause Analysis — Walkthrough of return trends by category, region, customer, and time

Dashboard Tour — Explanation of each chart and how to use filters

Strategic Recommendations — Product policies, customer flags, seasonal campaigns

Next Steps — Dashboard deployment, ongoing monitoring, data automation

### 🖥️ Presentation Format:

Submitted as a 5-minute recorded walkthrough of Tableau Story (or PDF if video unavailable)

### 📁 Files Included
File	Description
README.md	Project summary & insights
Superstore_Returns.twbx	Tableau packaged workbook
Mockup_Sketches/	3 mockup images
Dashboard_Template.png	Screenshot of container layout
Superstore Returns.pdf	Analysis summary
Presentation.mp4 (optional)	Narrated video walkthrough
Story_Draft_Captions.twbx	Story captions version

### 🛠 Tools & Skills Applied
Tableau Desktop / Tableau Public

LEFT JOINs

Calculated fields

Story Points

Dashboard UX

Data storytelling techniques

Executive communication

### ✅ Key Takeaways
Not all returns are equal — return rate offers more insight than raw return count

Certain categories, customers, and regions are responsible for the majority of returns

A clear dashboard paired with data storytelling helps executives identify problems fast

Business insights must be paired with actionable strategy

“Dashboards show the data. Stories explain what to do with it.”
This project proves how combining analytics and storytelling leads to better business outcomes.
