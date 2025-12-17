# 🚕 Ride-Hailing Analysis (Uber)

## 📌 Project Overview

This project analyzes Uber ride-hailing data to understand **demand–supply dynamics**, **cancellation drivers**, **revenue patterns**, and **weather impacts**. The goal is to derive actionable insights that can help improve operational efficiency, reduce cancellations, and optimize pricing and driver incentives.

---

## 🎯 Objective

* Analyze ride request patterns across time and locations
* Identify factors leading to trip cancellations and "No Cars Available" events
* Understand revenue contribution by ride type
* Assess the impact of weather on demand, cancellations, and fulfillment
* Provide data-driven recommendations to reduce churn and improve service

---

## 📂 Dataset Information

* **Source:** Uber Ride Analysis Dataset (CSV)
* **Records:** ~6,945 rides
* **Columns:**

  * `request_id`
  * `pickup_point`
  * `drop_point`
  * `request_timestamp`
  * `start_timestamp`
  * `drop_timestamp`
  * `trip_cost`
  * `extra_tip`
  * `driver_id`
  * `trip_status`
  * `ride_type`
  * `payment_method`
  * `weather`

---

## 🧹 Data Cleaning & Preprocessing

* Converted timestamp columns to `datetime`
* Standardized text fields (pickup, drop, ride type, payment method, weather)
* Handled missing timestamps for cancelled and no-car trips
* Retained cancelled trips for churn analysis but excluded them from duration/revenue metrics

---

## 🛠 Feature Engineering

* Extracted temporal features:

  * `request_hour`
  * `request_day`
* Created derived metrics:

  * `wait_time` (start − request)
  * `trip_duration` (drop − start)
* Categorized time into **Peak** vs **Off-Peak** hours

---

## 📊 Exploratory Data Analysis

### Univariate Analysis

* Ride type distribution
* Trip status distribution

### Bivariate Analysis

* Hourly demand trends
* Cancellation rates by hour
* Revenue by ride type
* Weather vs trip status

### Multivariate Analysis

* Pickup location vs hour heatmap
* Tip vs trip duration by ride type
* Wait time and trip duration distributions

---

## 📈 Visualizations Used

* Line charts (hourly demand, cancellation rate)
* Heatmaps (pickup location vs hour)
* Bar charts (revenue, cancellations)
* Box plots (wait time, trip duration)
* Scatter plots (tips vs duration)

All visualizations were created using **Matplotlib** and **Seaborn**.

---

## 🔍 Key Insights

* Peak demand occurs during **8–10 AM** and **6–8 PM**
* Cancellation and "No Cars Available" events spike during peak hours
* Rainy weather increases cancellations by ~20%
* **UberXL**, while fewer in number, contributes disproportionately higher revenue
* Longer trips tend to receive higher tips
