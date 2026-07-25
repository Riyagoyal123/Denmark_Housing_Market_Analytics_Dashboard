# 🏡 Housing Market Analytics Dashboard

An end-to-end cloud data warehouse and analytics solution built to analyze real estate valuation, property transactions, price per square meter, and market trends across Denmark's municipalities.

---

## 📌 Project Overview

Understanding real estate market fluctuations, pricing per square meter ($\text{DKK/m}^2$), and property demand trends requires scalable cloud storage and robust analytics.

This project delivers a complete cloud-to-BI analytics pipeline:
1. **Cloud Data Warehousing (Google BigQuery):** Storing, processing, and querying massive housing dataset tables in BigQuery using standard SQL.
2. **Business Intelligence (Power BI):** Connecting directly to BigQuery, creating custom DAX measures, data modeling, and building interactive visual dashboards.
3. **Market Recommendations:** Generating data-driven insights into regional pricing disparities, sales velocity, and property valuations across Danish regions (e.g., Hovedstaden, Syddanmark, Midtjylland).

---

## 🛠️ Tech Stack & Tools

| Layer | Technology | Purpose |
| :--- | :--- | :--- |
| **Data Warehouse** | **Google BigQuery** | Cloud data storage, high-speed SQL execution, data partitioning |
| **Business Intelligence** | **Power BI Desktop** | Direct connection to BigQuery, data modeling, DAX measures, visual insights |
| **Data Querying** | **SQL** | Aggregations, spatial filtering, and price calculations |
| **Documentation** | **Markdown / Git** | Code documentation and version control |

---

## 🏗️ Data Architecture & Pipeline

```text
  ┌────────────────────────┐       ┌────────────────────────┐       ┌────────────────────────┐
  │   Housing Dataset      │       │ Google BigQuery        │       │  Power BI Desktop      │
  │ (Real Estate Listings) │ ───►  │ (Cloud Data Warehouse) │ ───►  │ (Interactive Dashboard)│
  └────────────────────────┘       └────────────────────────┘       └────────────────────────┘

📂 Repository Structure
Plaintext
Denmark_Housing_Market_Analytics_Dashboard/
│
├── dataset/
│   └── denmark_housing_sample.csv       # Sample dataset schema
├── sql/
│   ├── bigquery_table_setup.sql         # Schema definition and partitioning logic
│   └── market_analysis_queries.sql      # Analytical queries (price/m², regional averages)
├── dashboard/
│   └── denmark_housing_analytics.pbix   # Interactive Power BI report file
├── assets/
│   └── dashboard_preview.png            # Dashboard screenshots
└── README.md                            # Documentation

📊 Key Business Questions Answered
1.) Regional Valuation Gaps: How do average price per square meter ($\text{DKK/m}^2$) compare across major municipalities (e.g., Copenhagen vs. Aarhus vs. Odense)?

2.) Property Type Dynamics: What is the distribution of sales between single-family homes (Villaer), apartments (Ejerlejligheder), and holiday homes (Sommerhuse)?

3.) Pricing Trends Over Time: How have housing listing prices and actual valuation trends evolved quarterly and annually?

4.) Price vs. Area Correlation: What is the relationship between lot area, floor size, construction year, and overall property valuation?

📈 Dashboard Features & Visual Highlights
1.) Executive Summary: High-level KPIs showing total housing market value ($\text{DKK}$), average property price, median area ($\text{m}^2$), and total active listings.

2.) Geographic Analysis: Map visualization detailing valuation intensity across Danish postal codes and regions.

3.) Property Metrics Comparison: Interactive slicers allowing filtering by Year Built, Property Type, Region, and Price Range.
