# Food-Delivery-Operations-Analytics
### End-to-End Python Data Analysis | Zomato Delhi NCR | Sep 2024 – Jan 2025
End-to-end Python data analysis on 21,321 Zomato food delivery orders from Delhi NCR. Covers data cleaning, wrangling, feature engineering, KPI tracking, EDA, and 10 professional charts. Uncovers insights on delivery delays, customer ratings, and discount behaviour.

[![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)](https://python.org)
[![pandas](https://img.shields.io/badge/pandas-2.x-150458?logo=pandas)](https://pandas.pydata.org)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.x-orange)](https://matplotlib.org)
[![Seaborn](https://img.shields.io/badge/Seaborn-0.13-teal)](https://seaborn.pydata.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter)](https://jupyter.org)

---

##  Project Overview

This project analyses **21,321 food delivery orders** from Zomato's Delhi NCR operations to uncover
insights on delivery efficiency, customer satisfaction, discount behaviour, and peak demand patterns.

The goal is to simulate the work of a real data analyst helping a food delivery company answer:
- Where are we losing customer satisfaction?
- What is causing delivery delays?
- Are our discounts actually working?
- Which operational areas need immediate attention?

The project covers the **complete analyst workflow** — from raw messy data to actionable business
recommendations — across 9 structured phases.

---

##  Key Findings at a Glance

| Metric | Value |
|--------|-------|
| Total Orders Analysed | 21,321 |
| Delivery Success Rate | 99.1% |
| Average Order Value | ₹683 |
| Average Kitchen Prep Time | 17.3 mins |
| Delayed Orders (>35 min) | 8.5% |
| Peak Hour Order Share | 58.6% |
| Orders with Discounts | 61.1% |
| Average Discount | 13.7% of bill |
| Average Customer Rating | 4.36 / 5.0 |
| Orders Rated | 11.8% |

---

##  Business Insights Uncovered

**1. Peak Hours Create Operational Bottlenecks**
Orders between 12–2 PM and 7–10 PM account for ~59% of daily volume.
Delay rates nearly double during these windows compared to off-peak hours.
The 8–9 PM dinner slot is the single most congested hour.

**2. Delay Directly Harms Customer Ratings**
On-time orders consistently receive higher ratings than delayed orders.
Even with only 11.8% of orders rated, the pattern is clear and significant.

**3. Incorrect Order-Ready Marking Wastes Rider Time**
When restaurants mark orders ready incorrectly, rider idle time increases significantly.
Nearly 1 in 10 orders is marked incorrectly — a fixable operational problem.

**4. Discounts Drive Volume but Compress Net Revenue**
61% of orders use a discount averaging 13.7% off the bill.
Discounted orders show higher gross bill values, suggesting discounts do encourage
larger basket sizes — but margin impact needs monitoring.

**5. Demand Is Highly Concentrated by Subzone**
GK2 and Sector 4 together account for the majority of all orders.
Any service disruption in these two zones has outsized impact on overall performance.

---

##  Charts

| Chart | What It Shows |
|-------|--------------|
| Chart 1 | Hourly Order Volume vs Delay Rate (dual-axis) |
| Chart 2 | Orders by Day of Week — weekday vs weekend |
| Chart 3 | Delivery Time Distribution with mean and threshold lines |
| Chart 4 | Customer Rating: On-Time vs Delayed Orders (boxplot) |
| Chart 5 | Order Volume Heatmap — Hour × Day of Week |
| Chart 6 | Monthly Order Volume Trend (Sep 2024 – Jan 2025) |
| Chart 7 | Rider Wait Time by Order-Ready Marking Accuracy |
| Chart 8 | Average Order Value by Discount Range |
| Chart 9 | Cancellation and Rejection Reasons |
| Chart 10 | Subzone Performance — Order Volume vs Avg KPT |

---

##  Project Structure

```
Food-Delivery-Operations-Analytics/
│
├── optimizing_food_delivery_operations_through_python_analytics.ipynb
│                          ← Full analysis notebook (all 9 phases)
│
├── data/
│   └── order_history_kaggle_data.csv    ← Raw dataset from Kaggle
│
├── visuals/
│   ├── chart_01_hourly_demand_delay.png
│   ├── chart_02_orders_by_day.png
│   ├── chart_03_delivery_time_dist.png
│   ├── chart_04_delay_vs_rating.png
│   ├── chart_05_heatmap_hour_day.png
│   ├── chart_06_monthly_trend.png
│   ├── chart_07_ready_marking_wait.png
│   ├── chart_08_discount_order_value.png
│   ├── chart_09_cancellation_reasons.png
│   └── chart_10_subzone_kpt.png
│
└── README.md
```

---

##  Project Phases

| Phase | Name | What Was Done |
|-------|------|---------------|
| 1 | Dataset Understanding | Loaded data, inspected 29 columns, built data dictionary, identified missing values and data type issues |
| 2 | Data Cleaning | Removed duplicates, dropped empty columns, converted datetime and distance, renamed columns to snake_case, combined discount columns |
| 3 | Data Wrangling | Created delivered/cancelled subsets, counted items per order, built restaurant and subzone aggregation scorecards |
| 4 | Feature Engineering | Created 12 new columns — order_hour, day_name, is_weekend, peak_hour_flag, delay_flag, discount_pct, rating_band, and more |
| 5 | KPI Tracking | Computed 10 core business metrics and built a monthly KPI trend table |
| 6 | EDA | Answered 8 business questions across demand, operations, customer, and revenue analysis |
| 7 | Visual Storytelling | Built 10 professional charts using Matplotlib and Seaborn |
| 8 | Business Insights | Translated findings into 5 numbered executive-level insights with supporting data |
| 9 | Recommendations | Produced 4 prioritised recommendations with actions, metrics, and expected outcomes |

---

##  Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3 | Core language |
| pandas | Data loading, cleaning, wrangling, aggregation |
| NumPy | Numerical calculations, np.where(), np.select() |
| Matplotlib | Charts and visualisations |
| Seaborn | Boxplots and heatmaps |
| Jupyter Notebook | Interactive analysis environment |

---

##  Dataset

**Source:** [[Food Delivery Order History Data — Kaggle](https://www.kaggle.com/datasets/)
](https://www.kaggle.com/datasets/sujalsuthar/food-delivery-order-history-data)

**About the dataset:**
- 21,321 rows × 29 columns
- Covers Zomato food delivery orders in Delhi NCR
- Period: September 2024 to January 2025
- Includes order metadata, pricing, discounts, kitchen timing, rider timing, ratings, and complaints

**Data challenges handled:**
- Timestamp stored as unstructured text → converted to `datetime64`
- Distance stored as `"2km"`, `"<1km"` → converted to `float64`
- 88% of ratings missing → documented as analytical limitation
- 4 separate discount columns → combined into single `total_discount`
- 3 columns with 95%+ missing values → dropped

---

##  How to Run

**1. Clone the repository**
```bash
git clone https://github.com/VaishaliThati/Food-Delivery-Operations-Analytics.git
cd Food-Delivery-Operations-Analytics
```

**2. Install dependencies**
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

**3. Run the notebook**
```bash
jupyter notebook
```
Open `optimizing_food_delivery_operations_through_python_analytics.ipynb` and run all cells top to bottom.

---

##  Strategic Recommendations

**Rec 1 [HIGH PRIORITY] — Dynamic Rider Allocation**
Pre-position additional riders in GK2 and Sector 4 during 11:30 AM–2:30 PM and 6:30–10:30 PM.
Target: Delay rate below 15% during peak hours.

**Rec 2 [HIGH PRIORITY] — SLA Alerts for Slow Restaurants**
Auto-alert when a restaurant's rolling 10-order avg KPT exceeds 25 minutes.
Target: 90% of restaurants with avg KPT under 22 minutes.

**Rec 3 [MEDIUM PRIORITY] — Order-Ready Marking Compliance**
In-app training for restaurants with >10% incorrect marking rate.
Introduce an accuracy score on the merchant dashboard.
Target: Incorrect marking rate below 5%.

**Rec 4 [MEDIUM PRIORITY] — Optimise Discount Strategy**
A/B test reducing discount depth for repeat customers.
Redirect savings toward peak-hour rider incentives.
Target: Improve revenue per order while maintaining retention.

---

##  Author

**Vaishali Thati**

Aspiring Data Analyst | Python | SQL | Power BI | Excel | Data Storytelling

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](www.linkedin.com/in/thati-vaishali-7830332a9)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?logo=github)](https://github.com/VaishaliThati)

---

*Dataset sourced from Kaggle. This project was built for portfolio and learning purposes.*
