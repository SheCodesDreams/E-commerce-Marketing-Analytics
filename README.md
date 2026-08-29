# E-Commerce Marketing Analytics & Customer Segmentation

An end-to-end data analytics project focused on **customer acquisition, marketing campaign performance, customer behavior, customer segmentation, and marketing efficiency** for an e-commerce business.

The project combines **Python, Pandas, SQL, SQLite, and Power BI** to transform raw e-commerce data into actionable business insights.

---

## 📌 Project Overview

The objective of this project is to analyze how customers are acquired, how they behave after acquisition, which marketing campaigns perform efficiently, and which customer groups represent the greatest business opportunities.

The analysis addresses questions such as:

- Which acquisition channels generate the most revenue?
- Which channels generate the highest-value customers?
- Which campaigns provide the best return relative to budget?
- How does customer purchasing behavior differ across segments?
- Which customers are highly valuable?
- Which customers are at risk of disengagement?
- How does revenue change over time?
- Where should marketing resources be prioritized?

---

# 🎯 Business Problem

An e-commerce business needs to understand the effectiveness of its marketing activities and customer base in order to improve acquisition, retention, and marketing-spend efficiency.

This project analyzes customer, session, transaction, campaign, and geographic data to provide a data-driven view of:

- Acquisition performance
- Campaign efficiency
- Customer purchasing behavior
- Customer value
- Customer retention opportunities
- Revenue trends

---

# 📊 Dataset

The project uses five primary datasets:

| Dataset | Records | Description |
|---|---:|---|
| Customers | 200,000 | Customer demographics, loyalty and engagement information |
| Sessions | 2,000,000 | Website sessions, traffic sources, device usage and campaign interactions |
| Transactions | 500,000 | Orders, order values, item counts, payment methods and shipping information |
| Campaigns | 200 | Campaign types, budgets, target regions and campaign dates |
| Geographic Data | 100 | Regional income, urbanization and internet penetration information |

Approximately **2.7 million raw records** were analyzed across the datasets.

> The raw datasets are not included in this repository because of their size. Processed analytical datasets used in the project are included in the `outputs/` directory.

---

# 🛠️ Tools & Technologies

| Technology | Usage |
|---|---|
| **Python** | Data loading, cleaning, transformation and analysis |
| **Pandas** | Data manipulation and aggregation |
| **NumPy** | Numerical calculations |
| **SQL** | Business-oriented analytical queries |
| **SQLite** | Local analytical database |
| **Power BI** | Interactive dashboard and visualization |
| **Jupyter Notebook** | Analysis workflow and documentation |

---

# 🔄 Project Workflow

```text
Raw E-Commerce Data
        ↓
Data Cleaning & Validation
        ↓
Feature Engineering
        ↓
Customer Acquisition Analysis
        ↓
Campaign Performance Analysis
        ↓
Customer Behavior Analysis
        ↓
RFM Customer Segmentation
        ↓
SQL Business Analysis
        ↓
Power BI Dashboard
        ↓
Business Insights & Recommendations
```

---

# 🔍 Analysis Performed

## 1. Data Cleaning & Validation

The raw datasets were inspected and prepared before analysis.

Key steps included:

- Checking dataset dimensions and column structures
- Identifying missing values
- Checking duplicate records
- Converting date columns to datetime format
- Standardizing categorical values
- Validating identifiers
- Checking relationships between customers, campaigns and geographic data
- Handling missing numerical values where appropriate
- Creating cleaned analytical datasets

---

## 2. Customer Acquisition Analysis

Customer acquisition was analyzed across four acquisition channels:

- Ads
- Organic
- Email
- Social

Metrics included:

- Acquired customers
- Purchasing customers
- Repeat customers
- Total orders
- Total revenue
- Purchase conversion rate
- Revenue per acquired customer
- Orders per customer

### Channel Performance

| Acquisition Channel | Acquired Customers | Total Revenue | Revenue / Customer |
|---|---:|---:|---:|
| Ads | 66,831 | $20.02M | $299.60 |
| Organic | 66,388 | $19.92M | $300.07 |
| Email | 33,409 | $10.06M | **$301.06** |
| Social | 33,362 | $10.01M | $300.08 |

### Key Insight

**Ads generated the highest total revenue** because it acquired the largest number of customers.

However, **Email generated the highest revenue per acquired customer**, indicating stronger value per acquired customer despite its smaller acquisition volume.

This highlights the difference between **acquisition scale and acquisition efficiency**.

---

## 3. Campaign Performance Analysis

The project evaluates **200 individual marketing campaigns** across five campaign types:

- Display
- Email
- Search
- Affiliate
- Social

Campaigns were evaluated using:

- Acquired customers
- Purchasing customers
- Revenue
- Campaign budget
- Customer Acquisition Cost (CAC)
- Return on Ad Spend (ROAS)

### Campaign Type Performance

| Campaign Type | Acquired Customers | Revenue | Budget | ROAS |
|---|---:|---:|---:|---:|
| Social | 31,851 | $9.56M | $7.49M | **1.28** |
| Email | 45,050 | $13.48M | $10.80M | **1.25** |
| Search | 37,882 | $11.37M | $9.12M | **1.25** |
| Affiliate | 32,887 | $9.94M | $8.40M | **1.18** |
| Display | 52,320 | $15.66M | $13.93M | **1.12** |

### Key Insight

Display campaigns produced the **highest total revenue**, but had the **lowest ROAS** among the five campaign types.

Therefore, high revenue does not necessarily indicate high marketing efficiency. Campaign budgets should be evaluated using both **revenue and efficiency metrics such as CAC and ROAS**.

---

## 4. Customer Behavior Analysis

Customers were classified based on purchase frequency:

- No Purchase
- One-time Customer
- Repeat Customer
- Highly Engaged Customer

### Customer Purchase Segments

| Segment | Customers | Total Revenue | Avg. Revenue / Customer | Avg. Orders |
|---|---:|---:|---:|---:|
| Repeat Customer | 120,974 | $40.64M | $335.98 | 2.80 |
| Highly Engaged Customer | 21,555 | $14.50M | **$672.60** | 5.58 |
| One-time Customer | 41,004 | $4.87M | $118.78 | 1.00 |
| No Purchase | 16,457 | $0 | $0 | 0 |

### Key Insight

Repeat customers represent the largest purchasing group and generate the majority of analyzed revenue.

Highly Engaged Customers are smaller in number but generate substantially higher revenue per customer.

This indicates that **retention and repeat purchasing are major revenue opportunities**.

---

# 5. RFM Customer Segmentation

RFM analysis was used to segment customers based on:

### Recency
How recently the customer made a purchase.

### Frequency
How often the customer purchased.

### Monetary
How much revenue the customer generated.

The analysis produced seven customer segments:

- Champions
- Loyal Customers
- Potential Loyalists
- Developing Customers
- At Risk
- High Value At Risk
- Low Engagement

### RFM Segment Summary

| Segment | Customers | Avg. Recency | Avg. Frequency | Avg. Monetary | Total Revenue |
|---|---:|---:|---:|---:|---:|
| Champions | 46,185 | 105.12 | 4.24 | $575.67 | **$26.59M** |
| At Risk | 32,081 | 414.42 | 3.61 | $435.06 | **$13.96M** |
| Loyal Customers | 33,394 | 114.00 | 2.55 | $215.41 | $7.19M |
| High Value At Risk | 13,563 | 530.38 | 1.75 | $413.04 | $5.60M |
| Low Engagement | 46,006 | 572.02 | 1.41 | $108.37 | $4.99M |
| Developing Customers | 10,501 | 121.35 | 1.13 | $93.09 | $0.98M |
| Potential Loyalists | 1,811 | 121.20 | 1.39 | $393.58 | $0.71M |

### Key Insights

- **Champions** are the largest high-value segment and generated approximately **$26.59M**.
- **At Risk** customers generated approximately **$13.96M** while showing substantially higher recency, making them an important retention opportunity.
- **High Value At Risk** customers have relatively high monetary value but low purchase frequency, making them a strong re-engagement opportunity.
- **Low Engagement** is one of the largest customer groups but contributes substantially less revenue than Champions.

---

# 6. Revenue & Acquisition Trends

Monthly acquisition analysis was performed across **33 acquisition months**.

Metrics included:

- Acquired customers
- Purchasing customers
- Repeat customers
- Revenue
- Orders
- Purchase conversion rate
- Repeat rate
- Revenue per acquired customer
- Month-over-month revenue change
- Month-over-month acquisition change

The analysis shows a substantial decline in acquisition volume and revenue across later acquisition cohorts.

### Example Revenue Trend

```text
January 2022  → $16.10M
February 2022 → $10.72M
March 2022    → $8.78M
```

Later periods contain substantially smaller acquisition cohorts and revenue levels.

### Business Implication

The decline warrants further investigation into:

- Acquisition effectiveness
- Marketing activity
- Customer demand
- Cohort behavior
- Retention and repeat purchasing

---

# 🧮 SQL Business Analysis

The processed analytical datasets were loaded into a **SQLite database** for SQL-based business analysis.

SQL was used to demonstrate both technical querying ability and business-oriented analysis.

### SQL Concepts Demonstrated

- `SELECT`
- `WHERE`
- `GROUP BY`
- Aggregate functions
- `CASE`
- Common Table Expressions (`CTE`)
- Subqueries
- `RANK()`
- `ROW_NUMBER()`
- `LAG()`
- `PARTITION BY`
- Calculated business metrics
- Ranking and benchmarking

### Example SQL Analysis

```sql
SELECT
    acquisition_channel,
    acquired_customers,
    total_orders,
    total_revenue,
    ROUND(
        total_revenue / acquired_customers,
        2
    ) AS revenue_per_customer
FROM channel_performance
ORDER BY revenue_per_customer DESC;
```

This query compares acquisition channels using customer volume, order volume, revenue, and revenue generated per acquired customer.

---

# 📊 Power BI Dashboard

An interactive Power BI dashboard was developed to provide an executive-level view of marketing and customer performance.

## Dashboard Components

### KPI Cards

- Total Revenue
- Acquired Customers
- Total Orders
- Average Order Value

### Marketing Performance

- Monthly Revenue Trend
- Revenue by Acquisition Channel
- Revenue by Campaign Type
- ROAS by Campaign Type
- Purchase Conversion by Channel

### Customer Analytics

- Customer Segment Distribution
- RFM-driven customer insights

### Filtering

An **Acquisition Channel slicer** allows users to filter the dashboard by:

- Ads
- Organic
- Email
- Social

---

## 📷 Dashboard Preview

> Add a screenshot of the Power BI dashboard to `images/dashboard.png`.

![E-Commerce Marketing Analytics Dashboard](images/dashboard.png)

---

# 💡 Key Business Insights

### 1. Scale and efficiency tell different stories

Ads generated the largest amount of revenue due to high customer acquisition volume, while Email generated the highest revenue per acquired customer.

### 2. Retention is a major revenue opportunity

Repeat customers generated approximately **$40.64M**, substantially more than one-time customers.

### 3. Champions are highly valuable

The Champions segment generated approximately **$26.59M** and had an average monetary value of approximately **$575.67**.

### 4. At-Risk customers represent an important opportunity

At Risk and High Value At Risk customers have previously demonstrated meaningful purchasing value but show signs of inactivity.

### 5. Revenue alone is insufficient for campaign evaluation

Display campaigns generated the highest total revenue but had the lowest campaign-type ROAS.

### 6. Later acquisition cohorts show declining performance

Both acquisition volume and revenue decline considerably across later acquisition months, suggesting an opportunity for deeper cohort and retention analysis.

---

# 💰 Business Recommendations

## 1. Strengthen Customer Retention

Prioritize **At Risk** and **High Value At Risk** customers through targeted re-engagement campaigns.

## 2. Increase Repeat Purchases

Develop personalized offers and lifecycle campaigns aimed at converting one-time customers into repeat customers.

## 3. Protect High-Value Customers

Use loyalty benefits, personalized communication and targeted experiences to retain Champions and Highly Engaged Customers.

## 4. Optimize Marketing Budgets

Evaluate campaigns using both revenue and efficiency metrics such as CAC and ROAS rather than revenue alone.

## 5. Leverage High-Value Acquisition

Email should be considered for further evaluation because it achieved the highest revenue per acquired customer and the highest purchase conversion rate among the analyzed channels.

## 6. Investigate Declining Acquisition Trends

Further analysis should examine why later acquisition cohorts contribute substantially less revenue and customer volume.

---

# 📈 Key Project Metrics

| Metric | Result |
|---|---:|
| Raw records analyzed | ~2.7M |
| Customers | 200,000 |
| Sessions | 2,000,000 |
| Transactions | 500,000 |
| Campaigns | 200 |
| Total Revenue | **$60.01M** |
| Average Order Value | **$120.03** |
| Purchasing Customers | **183K+** |
| Repeat Customers | **142K+** |
| RFM Segments | 7 |
| Campaign Types | 5 |

---

# 📁 Project Structure

```text
E-Commerce-Marketing-Analytics/
│
├── data/
│   └── README.md
│
├── notebooks/
│   └── marketing_analysis.ipynb
│
├── outputs/
│   ├── customer_metrics.csv
│   ├── campaign_performance.csv
│   ├── campaign_type_performance.csv
│   ├── channel_performance.csv
│   ├── monthly_acquisition.csv
│   ├── monthly_channel.csv
│   ├── rfm_customer_segments.csv
│   ├── segment_summary.csv
│   ├── budget_recommendation.csv
│   └── marketing_funnel.csv
│
├── powerbi/
│   └── E-Commerce-Marketing-Performance-Dashboard.pbix
│
├── README.md
├── .gitignore
└── requirements.txt
```

---

# 🚀 How to Run

## 1. Clone the repository

```bash
git clone https://github.com/SheCodesDreams/E-commerce-Marketing-Analytics.git
cd E-commerce-Marketing-Analytics
```

## 2. Install dependencies

```bash
pip install -r requirements.txt
```

## 3. Open the notebook

Open:

```text
notebooks/marketing_analysis.ipynb
```

Run the notebook from top to bottom to reproduce the analysis workflow.

## 4. Open the Power BI dashboard

Open the `.pbix` file located in:

```text
powerbi/
```

---

# 🔮 Future Improvements

Potential extensions include:

- Customer Lifetime Value (CLV) analysis
- Cohort retention analysis
- Churn prediction
- Campaign response prediction
- Customer propensity modeling
- A/B testing analysis
- Predictive customer segmentation
- More detailed geographic performance analysis

---

# 👤 Author

**Srinija Jonnakuti**

B.Tech — Mathematics & Computing  
IIT Guwahati

---

## ⭐ Project Highlights

**Python • Pandas • SQL • SQLite • Power BI • RFM • Customer Analytics • Marketing Analytics • Business Intelligence**
