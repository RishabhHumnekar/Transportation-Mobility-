# 🚖 GoodCabs — Transportation & Mobility Data Insights

> **CodeBasics Resume Challenge #13** | Domain: Transportation & Mobility | Function: Operations

---

## 📌 Project Overview

**Goodcabs** is a cab service company operating across **10 tier-2 Indian cities**, committed to supporting local drivers while delivering excellent passenger experiences. As part of their 2024 growth initiative, the Chief of Operations required an urgent performance assessment across key metrics.

This project analyses **426K trips** (Jan–Jun 2024) to deliver actionable insights on revenue, trip performance, passenger behaviour, and service quality.

**Tools Used:** `Power BI` · `MySQL` · `Excel` · `SQL`

---

## 📊 Key Metrics at a Glance

| Metric | Value |
|---|---|
| Total Revenue | ₹108M |
| Total Trips | 426K |
| Total Passengers | 238K |
| New Passengers | 177K |
| Repeat Passengers | 61K |
| Repeat Passenger Rate (RPR%) | 25.73% |
| Average Fare per KM | ₹13.28 |
| Average Fare per Trip | ₹254.02 |
| Average Distance per Trip | 19.13 km |
| Average Passenger Rating | 7.66 |
| Average Driver Rating | 7.83 |
| New vs Repeat Trip Ratio | 0.71 |

---

## 🗂️ Project Structure

```
goodcabs-data-insights/
│
├── sql/
│   ├── business_requests.sql       # 6 ad-hoc SQL business request queries
│   └── primary_analysis.sql        # 8 primary analysis queries
│
├── powerbi/
│   └── goodcabs_dashboard.pbix     # 5-page interactive Power BI dashboard
│
├── data/
│   ├── trips_db_schema.sql         # Trip-level database
│   └── targets_db_schema.sql       # Monthly performance targets database
│
├── presentation/
│   └── goodcabs_insights.pptx      # Presentation for Chief of Operations
│
└── README.md
```

---

## 📈 Power BI Dashboard — 5 Pages

### 1. Revenue
- Monthly revenue by city (area/stream chart)
- Average fare per km (₹13.28) and per trip (₹254.02)
- % Contribution by trip type (Long / Medium / Short) — Weekday vs Weekend
- Monthly revenue contribution heatmap per city
- Monthly revenue growth rate waterfall chart
- Average distance vs fare per trip by city

### 2. Trips
- Total trips vs target gauge — **426K actual / 429K target**
- Weekday vs weekend trip breakdown by city
- New vs Repeat passenger trip ratio: **0.71**
- City-Month target gap table (actual − target trips)
- Repeat trip frequency distribution (2–10 trips) by city

### 3. Passengers
- Total: 238K | New: 177K | Repeat: 61K | RPR: 25.73%
- RPR% heatmap by city and month
- New passenger acquisition performance vs target
- Top 3 cities — new acquisition: **Jaipur (46K), Kochi (26K), Chandigarh (19K)**
- Bottom 3 cities: **Surat (11.6K), Vadodara (10.1K), Coimbatore (8.5K)**

### 4. Ratings & Distance
- Average distance and fare per trip benchmarked by city
- Jaipur: highest distance (30 km) and fare (₹483.92)
- Surat: lowest fare (₹117.27), 11 km average
- Passenger vs driver rating comparison per city

### 5. Overall Summary
- Executive KPI cards with sparkline trends
- Full city comparison table (revenue, trips, passengers, ratings)
- Best/least performing city matrix by trip count segment
- Ranked revenue contribution with highest/lowest contributing months

---

## 💡 Key Insights

1. **Revenue Hub Concentration** — Jaipur (34.4%), Kochi (15.7%), and Chandigarh (10.2%) drive ~60% of total revenue. Mysore and Coimbatore need demand stimulation strategies.

2. **Repeat Passengers Drive Business** — Repeat passengers generated **51% of revenue** and **58% of trips**. Strong case for loyalty programs and subscription-based growth models.

3. **Trip & Passenger Target Gaps** — Overall shortfall of **–3,097 trips** vs target. Jaipur missed new passenger targets by –8K. Lucknow had the largest trip deficit (–7,701). June saw a **–14.61% revenue decline**.

4. **Rating Gap** — Driver rating (7.83) exceeds passenger rating (7.66). Lucknow and Vadodara show below-average passenger satisfaction, indicating service improvement zones.

5. **Weekday Demand Dominates** — Lucknow (50K) and Jaipur (44K) show strong weekday patterns, indicating business travel. Surat and Kochi show notable weekend activity suggesting tourism influence.

6. **Pricing Efficiency** — Jaipur commands the highest fare per trip (₹483.92 / 30 km). Pricing models across low-fare cities like Surat and Vadodara should be reviewed for margin optimisation.

---

## 🗄️ SQL — Ad-Hoc Business Requests

| # | Report | Description |
|---|---|---|
| BR-01 | City-Level Fare & Trip Summary | Total trips, avg fare/km, avg fare/trip, % contribution to total trips |
| BR-02 | Monthly Target Performance | Actual vs target trips per city-month; Above/Below Target status + % difference |
| BR-03 | Repeat Passenger Trip Frequency | % of repeat passengers by trip count (2–10 trips) per city |
| BR-04 | New Passenger Rankings | Top 3 and Bottom 3 cities by total new passengers |
| BR-05 | Highest Revenue Month per City | Peak revenue month per city with % contribution to city total |
| BR-06 | Repeat Passenger Rate Analysis | Monthly + city-wide RPR% (repeat passengers / total passengers) |

---

## ❓ Analysis Questions Addressed

### Primary (Data-Driven)
1. Top 3 and Bottom 3 cities by total trips over the full period
2. Average fare per trip vs average trip distance by city — pricing efficiency
3. Average passenger and driver ratings by city, segmented by new vs repeat passengers
4. Peak demand month and low demand month per city
5. Weekday vs weekend trip demand comparison across all 10 cities
6. Repeat passenger frequency and city contribution to higher trip counts
7. Monthly target achievement for trips, new passengers, and avg ratings
8. Highest and lowest RPR% cities (top 2 / bottom 2) and months

### Secondary (Research & Recommendations)
1. **Repeat Rate Drivers** — What factors (service quality, pricing, demographics) influence RPR% differences across cities?
2. **Tourism vs Business Demand** — How do festivals, events, and tourism seasons affect demand patterns?
3. **EV & Mobility Trends** — Should Goodcabs integrate electric vehicles or eco-friendly initiatives for tier-2 competitiveness?
4. **Local Partnerships** — Partnership opportunities with hotels, malls, and event venues to boost demand and loyalty
5. **Data Collection Gaps** — What additional data (wait times, cancellations, driver churn) would improve decision-making?

---

## 🏙️ City Performance Summary

| City | Total Trips | Total Revenue | Avg Distance (km) | Avg Fare/Trip (₹) | Avg Passenger Rating |
|---|---|---|---|---|---|
| Jaipur | 76.89K | ₹37.21M | 30.02 | 483.92 | 8.58 |
| Kochi | 50.70K | ₹17.00M | 24.07 | 335.25 | 8.52 |
| Lucknow | 64.30K | ₹9.46M | 12.51 | 147.18 | 6.49 |
| Chandigarh | 38.98K | ₹11.06M | 23.52 | 283.69 | 7.98 |
| Indore | 42.46K | ₹7.64M | 16.50 | 179.84 | 7.22 |
| Surat | 54.84K | ₹6.43M | 11.00 | 117.27 | 6.42 |
| Visakhapatnam | 28.37K | ₹8.02M | 22.55 | 282.67 | 8.43 |
| Mysore | 16.24K | ₹4.05M | 16.50 | 249.71 | 8.70 |
| Vadodara | 32.03K | ₹3.80M | 11.52 | 118.57 | 6.61 |
| Coimbatore | 21.10K | ₹3.52M | 14.98 | 166.98 | 7.88 |

---

## 🔗 Links

- 📊 [Live Power BI Dashboard](#)
- 💻 [GitHub Repository](#)
- 🎥 [Video Presentation](#)
- 💼 [LinkedIn Post](#)

---

*Built as part of CodeBasics Resume Project Challenge #13 — Transportation & Mobility Domain*
