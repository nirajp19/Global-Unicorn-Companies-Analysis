# 🌎 Global Unicorn Companies Analysis

![Project Cover](images/project-cover.png)

## 📌 Executive Summary

**Global Unicorn Companies Analysis** is a Power BI business intelligence case study that turns company-level unicorn data into an executive view of the global startup ecosystem.

The project examines five connected dimensions:

**Growth → Geography → Industry → Valuation → Funding**

It is framed as an **investment-intelligence problem**: a global venture capital team needs a structured way to understand where unicorn activity is concentrated, which industries have the most companies and value, and how funding compares with valuation.

> **Dataset scope:** the supplied `unicorn_companies` dataset contains **1,500 company records**, covering **15 countries, 38 cities, and 14 industries**.

---

## 🎯 Business Scenario

Imagine a global venture capital firm evaluating the startup ecosystem across markets and sectors.

Leadership does not want hundreds of rows of company data. They need answers to questions such as:

- Where are unicorn companies concentrated?
- Which cities have developed into major startup hubs?
- Which industries produce the largest number of unicorns?
- Which industries have higher average valuations?
- How much capital has been raised?
- How does reported valuation compare with capital raised?
- What patterns should analysts investigate further?

This dashboard converts those questions into an interactive Power BI experience.

---

## 🧩 Business Problem

The raw dataset contains company-level information, but raw records alone do not provide an executive view.

The analytical challenge was to transform:

```text
1,500 Company Records
        ↓
Structured Analysis
        ↓
Business KPIs
        ↓
Interactive Dashboard
        ↓
Investment Intelligence
```

The goal is **not** to predict which company will become the next unicorn.

Instead, the project describes patterns in the supplied dataset and provides a framework for comparing markets, industries, valuation, and funding.

---

## 👥 Intended Stakeholders

- Venture Capital / Investment Teams
- Investment Analysts
- Strategy Teams
- Business Analysts
- Startup Ecosystem Researchers
- Executive Leadership

---

## ❓ Key Business Questions

### Growth
1. How has unicorn creation changed over time?
2. Which periods show higher unicorn activity?

### Geography
3. Which countries contain the most unicorn companies?
4. Which cities act as major startup hubs?
5. How does unicorn concentration relate to average valuation?

### Industry
6. Which industries have the highest unicorn counts?
7. Which industries have the highest average valuation?
8. How does funding compare with valuation across industries?

### Capital Efficiency
9. Which industries have higher valuation relative to capital raised?
10. Which patterns deserve deeper investment analysis?

---

## 📊 Dataset

**File:** `data/unicorn_companies.csv`

| Metric | Result |
|---|---:|
| Unicorn companies | **1,500** |
| Countries | **15** |
| Cities | **38** |
| Industries | **14** |
| Average valuation | **$5.66B** |
| Total funding raised | **$2,561.8B** |
| Average years to unicorn | **7.5 years** |

### Main Fields

- Company
- Valuation ($B)
- Date Joined
- Country
- City
- Industry
- Select Investors
- Founded Year
- Total Raised ($B)
- Financial Stage
- Investors Count

See the full [Data Dictionary](docs/data-dictionary.md).

---

## 🧹 Data Preparation & Analytical Logic

The project uses the supplied dataset as the analytical source.

Key preparation/derivation steps:

1. Parse `Date Joined` as a date.
2. Extract joining year for time-series analysis.
3. Calculate approximate **Years to Unicorn**:
   `YEAR(Date Joined) - Founded Year`
4. Aggregate company records by country, city, industry, and year.
5. Calculate average valuation.
6. Calculate total capital raised.
7. Calculate **Funding Efficiency**:

```text
Funding Efficiency =
Valuation ($B) / Total Raised ($B)
```

Funding efficiency is used as a comparative analytical ratio. It is **not** profitability, ROI, or investment return.

---

## 🖥️ Dashboard

![Dashboard Preview](images/dashboard-preview.png)

### Page 1 — Executive Overview

The executive page provides the ecosystem snapshot:

- Unicorn count
- Average valuation
- Total funding raised
- Countries
- Industries
- Average years to unicorn
- Growth over time
- Top industries
- Total unicorns by country

### Page 2 — Geography Analysis

The geography page investigates:

- Country concentration
- City concentration
- Top country
- Top city
- Top countries by unicorn count
- Top cities by unicorn count
- Unicorn count vs. average valuation

### Page 3 — Industry Performance

The industry page compares:

- Industry count
- Top industry
- Highest average valuation industry
- Funding efficiency
- Unicorn count by industry
- Average valuation by industry
- Funding vs. valuation

### Page 4 — Key Insights

The final page converts the dashboard into an executive narrative:

- Business scenario
- Geographic observations
- Industry observations
- Strategic considerations

---

## 🔎 Key Findings

### 🇺🇸 Geographic concentration

The **United States** is the largest country by unicorn count in the supplied dataset:

**709 companies / ~47.3% of all records**

The leading city by company count is **Seattle**, with **103 companies**.

This indicates substantial geographic concentration in the dataset.

### 💳 Industry concentration

**FinTech** is the largest industry:

**293 companies / ~19.5% of all records**

The next four industries by count are:

| Industry | Unicorn Count |
|---|---:|
| FinTech | 293 |
| Internet software & services | 282 |
| E-commerce & direct-to-consumer | 169 |
| Artificial intelligence | 156 |
| Health | 133 |

### 💰 Valuation

Average company valuation across the dataset:

**$5.66B**

The highest average valuation industry in the supplied data is:

**Supply chain, logistics, & delivery — approximately $10.00B**

### 💵 Funding

Total funding raised across the dataset:

**$2,561.8B**

This enables cross-industry and geographic comparisons between reported funding and valuation.

### ⚙️ Funding Efficiency

The highest average funding-efficiency result is:

**Supply chain, logistics, & delivery — 4.54×**

The metric is:

```text
Valuation ÷ Total Raised
```

It should be interpreted as an analytical comparison, not an investment-return measure.

---

## 💡 What the Analysis Tells Us

### 1. Unicorn activity is concentrated

A large share of records is concentrated in a relatively small number of countries and cities.

### 2. Company count and valuation tell different stories

The industry with the most unicorn companies is not necessarily the industry with the highest average valuation.

### 3. Funding adds another dimension

Comparing total capital raised with valuation gives a different perspective from simply counting companies.

### 4. Efficiency can be used as a screening metric

Funding efficiency can help analysts identify industries that deserve deeper investigation, alongside other financial and operational metrics.

---

## 🧠 Analytical Workflow

![Analytical Workflow](images/analytical-workflow.png)

---

## 🛠️ Technology Stack

| Technology | Role |
|---|---|
| **Power BI** | Data modeling, DAX, KPIs, interactive dashboard |
| **CSV / Excel** | Data source and preparation |
| **Data Analysis** | Aggregation, comparison and trend analysis |
| **GitHub** | Version control and portfolio presentation |

---

## 📁 Repository Structure

```text
global-unicorn-companies-analysis/
│
├── README.md
│
├── data/
│   └── unicorn_companies.csv
│
├── dashboard/
│   └── Global Unicorn Companies Dashboard.pbix
│
├── images/
│   ├── project-cover.png
│   ├── dashboard-preview.png
│   ├── dashboard-page-1.png
│   ├── dashboard-page-2.png
│   ├── dashboard-page-3.png
│   ├── dashboard-page-4.png
│   └── analytical-workflow.png
│
├── docs/
│   ├── project-story.md
│   ├── business-requirements.md
│   ├── data-dictionary.md
│   ├── kpi-dictionary.md
│   ├── dashboard-guide.md
│   ├── insights.md
│   └── limitations.md
│
├── sql/
│   └── analysis.sql
│
└── python/
    └── exploratory_analysis.py
```

---

## ⚠️ Assumptions & Limitations

- The analysis is based on the supplied `unicorn_companies` dataset.
- Valuation and funding values are treated as dataset fields.
- Funding efficiency is a ratio for analytical comparison; it does not measure profitability or investment return.
- Geographic concentration does not by itself imply future growth potential.
- The dashboard is descriptive/diagnostic rather than a predictive investment model.
- The dataset includes 2026 records; therefore, the latest period should be interpreted according to the dataset's supplied coverage.
- No external market data has been added to the core analysis.

See [Limitations](docs/limitations.md).

---

## 🚀 Future Enhancements

A future version could add:

- Investor-network analysis
- Funding-stage progression
- Cohort analysis
- Industry growth rates
- Country-level funding efficiency
- Investor concentration
- Company-level drill-through
- Automated data refresh
- Historical valuation trends
- Predictive modeling

---

## 📄 Project Documentation

- [Project Story](docs/project-story.md)
- [Business Requirements](docs/business-requirements.md)
- [Data Dictionary](docs/data-dictionary.md)
- [KPI Dictionary](docs/kpi-dictionary.md)
- [Dashboard Guide](docs/dashboard-guide.md)
- [Key Insights](docs/insights.md)
- [Limitations](docs/limitations.md)

---

## 👨‍💻 Author

**Niraj Pawar**

Data Analyst | Data Science | Business Intelligence

---

## ⭐ Portfolio Takeaway

This project demonstrates the complete analytical flow:

**Business Problem → Data → Preparation → KPI Design → Analysis → Power BI → Insights → Decision Support**

The objective was not simply to build a dashboard, but to create an analytical product that helps stakeholders understand the global unicorn ecosystem.
