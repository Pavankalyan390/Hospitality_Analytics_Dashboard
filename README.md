# Hospitality_Analytics_Dashboard

## Problem Statement❗

AtliQ Grands owns multiple five-star hotels across india. They have been in the hospitality industry for the past 20 years. Due to strategic moves from other competitors and ineffective decision-making in management, AtliQ Grands are losing it's market share and revenue in the luxury/business hotels category. As a strategic move, the managing director of AtliQ Grands wanted to incorporate "Business and Data Intelligence" to regain their market share and revenue. 

However, they do not have an in-house data analytics team to provide them with these insights.

--- 

## Project Overview

This project showcases a Hospitality Analytics Dashboard built in Power BI, designed to provide hotel managers and decision-makers with real-time performance insights.

The dashboard enables monitoring of revenue, occupancy, booking trends, and property-level performance across different cities and categories (Luxury vs. Business).

It combines 20+ DAX measures to calculate and analyze KPIs that are critical for the hospitality industry.

## Key Metrics(KPIs):

- ***Revenue*** – Total revenue generated from bookings.

- ***RevPAR (Revenue Per Available Room)*** = Revenue ÷ Total Available Rooms

- ***ADR (Average Daily Rate)*** = Total Room Revenue ÷ Rooms Sold

- ***Occupancy %*** = Rooms Sold ÷ Total Available Rooms × 100

- ***DSRN (Daily Sellable Room Nights)*** – Total rooms available to sell per day.

- ***SRN (Sellable Room Nights)*** – Total room nights available across period.

- ***Realisation %*** – Ratio of successful bookings (checked-in) vs total bookings.


## Important DAX Formulas

1. Revenue Formula

``` DAX
Revenue = SUM(fact_bookings[revenue-realized])
```

2. RevPAR Formula

```DAX
RevPAR = DIVIDE([Revenue],[Total_Capacity])
```

3. ADR Fomula

```DAX
ADR = DIVIDE([Revenue],[Total_bookings],0)
```

4. Realisation

```DAX
Realisation = 1-([Cancellation %]+[No Show rate %])
```

5. Occupancy Formula

```DAX
Occupancy = DIVIDE([Total_successful_bookings],[Total_Capacity],0)
```

6. DSRN ***(Daily Sellable Room Nights)***

```DAX
DSRN = DIVIDE([Total_Capacity],[No of Days])
```

**These formulas highlight how raw booking data is transformed into business KPIs for actionable insights.**

---


## Dashboard Sections

1. **KPI Summary Cards**

- Revenue: ₹1.69Bn

- RevPAR: 7,337

- ADR: 12.70K

- Occupancy %: 57.79%

- DSRN: 2,528

- Realisation %: 70.14%

***👉 Managers can quickly monitor business health at a glance.***

2. **Revenue by Category**

- Pie Chart shows revenue distribution between Luxury and Business categories.

- Helps identify which segment drives higher revenue contribution.

3. **Trends by Key Metrics**

- Line chart displaying Revenue, ADR, and Occupancy % trends over weeks (W19 to W31).

- Useful for identifying seasonality, demand shifts, and performance dips.

4. **Property-Wise Performance**

***A detailed table by property:***

- Shows Revenue, Bookings, RevPAR, ADR, DSRN, Occupancy %, Realisation %, Cancellations %, and Ratings.

- Helps compare Delhi vs Mumbai properties and identify top/bottom performers.

Example:

- Atliq Grands (Mumbai) generates highest revenue (117M) with strong ADR (16,141).

- Atliq Blu (Delhi) shows competitive occupancy (65.32%) with slightly lower ADR.

5. **Realisation % and ADR by Booking Platform**

- Bar + Line Combo Chart compares booking platforms (logging, journey, direct-online, etc.).

- Provides insights into which platforms drive high ADR & reliable bookings.


## 📈 Insights

1. Overall Revenue: Strong at ₹1.69Bn with steady ADR (12.7K).

2. Occupancy % (57.79%): Indicates scope for optimization in off-peak days.

3. Luxury vs Business Split: Luxury dominates revenue contribution (~61%).

4. Booking Platforms: Some platforms show lower realisation %, highlighting potential cancellation/guest drop-off issues.

5. Property-Level View: Certain properties in Mumbai consistently outperform Delhi in ADR, while Delhi properties maintain higher occupancy.


## ⚙️ Tech Stack

- Tool: Power BI

- Data Source: Hotel booking + revenue dataset

- Modeling: Star Schema (dim_date, dim_hotels, dim_rooms, fact_bookings, fact_aggregate_bookings)

- DAX: 20+ formulas for KPI calculation (RevPAR, ADR, Occupancy, Realisation %, etc.)


## 🚀 Key Learning

- Built end-to-end hospitality analytics project.

- Gained domain knowledge about hotel KPIs and performance drivers.

- Used advanced DAX measures to bring actionable insights.

- Learned the importance of business + analytics blend to support property managers’ decision-making.


















