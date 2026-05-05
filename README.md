# Tesco Retail Productivity Analyser — 2023

## Overview

This project delivers end-to-end retail productivity analysis for Tesco's Operations Development team. Using transactional data from 8 Hertfordshire stores across 2023, it identifies revenue patterns, fulfilment performance gaps, and store-level productivity opportunities — translating raw data into clear, actionable business recommendations for operational planning.

---

## Business Questions

1. Which product categories drive the most revenue and how is performance changing over time?
2. What is the network cancellation rate and where are the biggest fulfilment gaps?
3. Who are the highest-value customers and what drives their spend?
4. How does store performance vary across the network?
5. What seasonal and day-of-week patterns should operations plan around?

---

## Tools & Technologies

| Tool | Purpose |
|---|---|
| Python 3 | Core analysis and automation |
| Pandas | Data preparation and KPI calculation |
| Matplotlib & Seaborn | Statistical visualisation |
| Tableau Public | Interactive operational dashboard |
| Chart.js | Standalone web dashboard |
| Jupyter Notebook | Analysis and reporting environment |

---

## Project Structure

```
tesco-retail-productivity/
│
├── data/
│   └── tesco_retail_data.csv          # 15,000 transactions, 12 fields
│
├── tesco_retail_analysis.ipynb        # Full analysis notebook
├── tesco_analytics_dashboard.html     # Standalone interactive dashboard
└── README.md
```

---

## Dataset

| Field | Description |
|---|---|
| `transaction_id` | Unique transaction reference |
| `date` | Transaction date (Jan–Dec 2023) |
| `store_location` | Store name across 8 Hertfordshire locations |
| `customer_id` | Customer reference (3,000 unique customers) |
| `product_name` | Product name |
| `category` | Product category (8 categories) |
| `quantity` | Units per transaction |
| `unit_price` | Price per unit (GBP) |
| `total_amount` | Transaction revenue (GBP 0.00 for cancellations) |
| `status` | Fulfilled / Cancelled |
| `payment_method` | Contactless, Card, Cash, Clubcard Pay+ |
| `clubcard_member` | Yes / No |

---

## Key Findings & Recommendations

### Revenue & Seasonality
- Full year network revenue: **GBP 72,103** across 13,882 fulfilled orders
- December peaks at GBP 6,516 — **21% above annual average**
- February is the weakest trading month at GBP 5,361
- **Recommendation:** Initiate stock build from October. Target February with promotional activity to lift the weakest trading period.

### Cancellation Rate
- Network cancellation rate: **7.5%** — 1,118 lost orders
- Health & Beauty: **10.0%** — highest in the network
- Meat & Fish: **9.5%** · Household: **8.8%** — both above network average
- **Recommendation:** Audit stock availability in the top 3 categories. Implement automated weekly alerting when category cancel rate exceeds 10%.

### Customer Value
- Clubcard members spend **8% more per order** on average
- Top 10% of customers represent a disproportionate share of total revenue
- **Recommendation:** Activate personalised Clubcard offers targeting high-value customers in their top spend category.

### Store Performance
- Welwyn Garden City leads the network at GBP 14,972 revenue
- Welwyn GC also carries an **8.5% cancellation rate** — above the 7.5% network average
- **Recommendation:** Prioritise fulfilment process review at high-revenue / high-cancellation stores. Share operational best practices from the lowest-cancel locations across the network.

### Day-of-Week Patterns
- Saturday is the peak trading day across all stores
- Monday is consistently the lowest volume day
- **Recommendation:** Align staffing rotas, delivery schedules, and stock replenishment to reflect weekend demand concentration.

---

## Analysis Notebook — Section Summary

| Section | Content |
|---|---|
| 1 | Environment setup and library imports |
| 2 | Data loading, schema inspection, quality assessment |
| 3 | Data cleaning — datetime conversion, feature engineering, status segmentation |
| 4 | Headline KPIs — revenue, orders, cancellation rate, average order value |
| 5 | Revenue by category — ranked analysis with share breakdown |
| 6 | Monthly revenue trend — time series with MoM growth |
| 7 | Cancellation analysis — by category and store, estimated revenue impact |
| 8 | Customer analysis — spend distribution, value segmentation, Clubcard uplift |
| 9 | Store performance — revenue and fulfilment rate comparison |
| 10 | Trading patterns — weekly trend, rolling average, day-of-week volume |
| 11 | Summary findings and prioritised business recommendations |

---

## Tableau Dashboard

Five-view interactive operational dashboard:

1. **Monthly Trend** — seasonal revenue shape across all 12 months with average reference
2. **Revenue by Category** — ranked revenue contribution by product category
3. **Cancellation Rate** — diverging colour bars showing performance vs network average
4. **Store Performance** — revenue comparison across all 8 locations
5. **Day of Week** — gradient intensity bars showing daily trading patterns

---

## Running the Notebook

```bash
# Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# Launch
jupyter notebook

# Open tesco_retail_analysis.ipynb
# Run: Kernel → Restart & Run All
```

---

## Contact

**Praneet Sivakumar**  
MSc Data Science — University of Hertfordshire  
Email: connect.with.praneet@gmail.com  
LinkedIn: linkedin.com/in/praneetsivakumar  
GitHub: github.com/praneetsivakumar
