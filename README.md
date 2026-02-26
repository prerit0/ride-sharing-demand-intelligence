# Ride-Sharing Demand & Revenue Intelligence  
### Dynamic Surge Pricing Simulation | NYC Yellow Taxi Data (Jan 2025)

---

## 📌 Project Overview

This project analyzes NYC Yellow Taxi trip data to uncover demand patterns, revenue behavior, and simulate a dynamic surge pricing strategy.

The primary objective was to:

- Perform large-scale data cleaning and feature engineering  
- Analyze demand and revenue trends using SQL and Python  
- Identify peak demand periods and geographic concentration  
- Simulate a percentile-based surge pricing model  
- Estimate projected revenue uplift  
- Build a regression model to predict fare amount  
- Deliver business insights through an interactive Power BI dashboard  

---

## 📊 Dataset

Source: NYC Taxi & Limousine Commission (TLC)  
Data Used: January 2025 Yellow Taxi Trip Records  

Official dataset link:  
https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page  

The dataset includes:

- Pickup & drop-off timestamps  
- Trip distance  
- Fare and total amount  
- Tip amount  
- Passenger count  
- Pickup and drop-off location IDs  

Total records analyzed (after cleaning): ~3.4M+ trips

---

## 🧹 Data Cleaning & Feature Engineering

- Removed extreme outliers using 99th percentile filtering  
- Handled missing values with median imputation (where applicable)  
- Created `trip_duration_min` from timestamps  
- Engineered new features:
  - Revenue per mile  
  - Revenue per minute  
  - Tip percentage  
  - Weekend indicator  
- Optimized data types for performance  

---

## 🔍 Exploratory Data Analysis (SQL + Python)

### 📈 Hourly Demand Insights
- Peak demand observed at 6 PM  
- Revenue peaks at 5 PM  
- Clear commuter-driven demand pattern  

### 📅 Weekend vs Weekday Analysis
- Weekdays dominate total trip volume and revenue  
- Minimal difference in average fare and tip percentage  

### 🗺 Geographic Insights
- Revenue heavily concentrated in Manhattan  
- Airport-related zones contribute significant per-trip revenue  

---

## 🚀 Dynamic Surge Pricing Simulation

A percentile-based surge pricing strategy was implemented:

- < 75th percentile → 1.0x  
- 75–90th percentile → 1.2x  
- 90–97th percentile → 1.5x  
- > 97th percentile → 2.0x  

### 📊 Results

Projected Revenue Increase: **24.56%**

Revenue uplift was primarily concentrated during peak evening commute hours.

---

## 🤖 Fare Prediction Model

Model: Linear Regression  
Features Used:
- Trip distance  
- Trip duration  

Model Performance:

- R² Score: 0.92  
- Mean Absolute Error: $2.33  

Trip distance was identified as the strongest predictor of fare amount.

---

## 📊 Dashboard

A 3-page Power BI dashboard was built to present:

1. NYC Taxi Demand - Revenue - Surge Analysis
2. Location Based Revenue - Intelligence
3. Surge Pricing Impact  

(Screenshots included in repository)

---

## 🛠 Tech Stack

- Python (pandas, numpy, matplotlib, seaborn)  
- SQL (DuckDB for aggregations)  
- Scikit-learn  
- Power BI  
- Git & GitHub  

---

## 📁 Project Structure
Dashboard/ → 3 Dashboards
notebooks/ → Data cleaning, EDA, ML
processed/ → Cleaned dataset (excluded from Git)
raw/ → Original dataset (excluded from Git)
insights/ → EDA insights & summaries
README/ → Project Summary
Requirements/ → Project Requirements

---

## ▶️ How to Reproduce

1. Clone the repository  
2. Install dependencies:
   pip install -r requirements.txt  
3. Run notebooks in order:
   - 01_data_cleaning.ipynb  
   - 02_eda_analysis.ipynb  
   - 03_simple_regression.ipynb  
4. Open `dashboard_dataset.csv` in Power BI  

---

## 💡 Key Takeaway

This project demonstrates an end-to-end data science workflow — from raw data processing to business strategy simulation — combining analytics, modeling, and visualization to drive revenue-focused insights.