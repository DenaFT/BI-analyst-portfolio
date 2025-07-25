# 🚖 Zuber Ride-Share Analysis — SQL Case Study

## 📊 Project Overview
**Sprint:** SQL-Based Data Exploration  
**Program:** TripleTen Business Intelligence Analyst Bootcamp  
**Project Type:** Database Querying & Insight Generation  
**Prepared by:** Dena Taylor  
**Date:** June 2024  

Zuber, a new ride-sharing company launching in Chicago, requested a deep dive into local taxi data to gain insights into passenger behavior, company competition, and the influence of weather on ride frequency. This SQL project focuses on real-world data analysis using multiple joined tables and conditional logic.

---

## 🧠 Business Objectives

1. **Understand passenger and company activity patterns** using taxi ride data.
2. **Identify the influence of weather conditions** on trip duration.
3. **Uncover the most competitive taxi providers** during targeted dates.
4. **Recommend data-backed strategies** for Zuber's launch in the Chicago market.

---

### 🗂️ Data Sources

The analysis was performed on a relational database with the following tables:

- `neighborhoods`: Information on Chicago neighborhoods
- `cabs`: Details on taxi providers and their vehicles
- `trips`: Trip logs including timestamps, distance, and locations
- `weather_records`: Hourly weather data for the city

---

## 🧪 Key Tasks & SQL Logic

### 1. 🚕 Ride Volume by Taxi Company (Nov 15–16, 2017)
```sql
SELECT company_name, COUNT(trip_id) AS trips_amount
FROM cabs
JOIN trips ON trips.cab_id = cabs.cab_id
WHERE trips.start_ts::date BETWEEN '2017-11-15' AND '2017-11-16'
GROUP BY company_name
ORDER BY trips_amount DESC;
```
Goal: Determine which companies had the highest trip volumes over a two-day period.

### 2. 🟡🔵 Filtered Volume for "Yellow" & "Blue" Companies (Nov 1–7, 2017)
```sql
SELECT company_name, COUNT(trip_id) AS trips_amount
FROM cabs
JOIN trips ON trips.cab_id = cabs.cab_id
WHERE start_ts::date BETWEEN '2017-11-01' AND '2017-11-07'
  AND (company_name LIKE '%Yellow%' OR company_name LIKE '%Blue%')
GROUP BY company_name;
```
Goal: Evaluate brand-dominant taxi companies by color branding.

### 3. 🏆 Rank Top 2 vs. Others (Nov 1–7, 2017)
```sql
SELECT 
  CASE 
    WHEN company_name = 'Flash Cab' THEN 'Flash Cab'
    WHEN company_name = 'Taxi Affiliation Services' THEN 'Taxi Affiliation Services'
    ELSE 'Other'
  END AS company,
  COUNT(trip_id) AS trips_amount
FROM cabs
JOIN trips ON trips.cab_id = cabs.cab_id
WHERE start_ts::date BETWEEN '2017-11-01' AND '2017-11-07'
GROUP BY company
ORDER BY trips_amount DESC;
```
Goal: Classify market share between major players and other providers.

### 4. 📍 Get Loop and O’Hare Neighborhood IDs
```sql
SELECT neighborhood_id, name
FROM neighborhoods
WHERE name LIKE '%Hare' OR name LIKE 'Loop';
```
Insight: Used to identify rides between the city center and the airport.

## 🌦️ Weather & Ride Duration Analysis
### 5. ☀️🌧️ Classify Weather Conditions
```sql
SELECT ts,
  CASE
    WHEN description LIKE '%rain%' OR description LIKE '%storm%' THEN 'Bad'
    ELSE 'Good'
  END AS weather_conditions
FROM weather_records;
```
Goal: Categorize hourly weather records into “Good” or “Bad” for ride analysis.

### 6. 📊 Analyze Ride Duration on Rainy Saturdays
```sql
SELECT trips.start_ts,
  CASE 
    WHEN weather_records.description LIKE '%rain%' OR weather_records.description LIKE '%storm%' THEN 'Bad'
    ELSE 'Good'
  END AS weather_conditions,
  trips.duration_seconds
FROM trips
JOIN weather_records ON trips.start_ts = weather_records.ts
WHERE pickup_location_id = 50 AND dropoff_location_id = 63
  AND EXTRACT(DOW FROM trips.start_ts) = 6
ORDER BY trips.trip_id;
```
Goal: Determine how rainy Saturdays affect ride durations from Loop to O’Hare.

## 📌 Summary of Insights
Flash Cab and Taxi Affiliation Services dominated the taxi market during the week of Nov 1–7, 2017.

Rainy weather tends to increase ride durations, especially on Saturdays.

Loop (ID: 50) and O'Hare (ID: 63) were focal points for airport travel and congestion.

“Yellow” and “Blue” taxis maintained a significant volume share during the period studied.

## 🔧 Tools & Skills Applied
SQL (PostgreSQL syntax)

Data JOINs and filtering

CASE statements for classification

Aggregations and grouping

Time-based filtering and weekday extraction

Real-world scenario analysis using weather + transit data

## 🚀 Next Steps
In upcoming sprints, I will:

Build visual dashboards (Power BI / Tableau)

Automate SQL queries using Python

Perform predictive modeling on transportation datasets

Develop recommendations based on traffic patterns and public transit proximity

> “Data is not just rows and columns — it’s insight waiting to be translated into action.”
> This project helped uncover how real-world factors like weather and location influence transportation dynamics.

