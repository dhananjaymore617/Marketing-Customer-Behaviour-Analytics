# Marketing & Customer Behaviour Analytics

An end-to-end marketing analytics project using **Snowflake, Power BI, DAX, and Power Query** to analyze customer engagement, conversion funnels, product performance, and customer feedback.

## Project Workflow

**CSV / Excel → Snowflake (RAW_DATA + CLEAN_DATA, Streams & Tasks) → Power Query → Power BI**

## Objective

Analyze customer conversion, marketing engagement, product performance, and customer feedback to identify opportunities to improve conversion rates, engagement, and customer satisfaction.

## Technology Stack

- **Snowflake** — cloud data warehouse with RAW_DATA and CLEAN_DATA layers, Streams for change tracking, and scheduled Tasks for incremental processing and automated transformations.
- **SQL** — data quality checks, cleaning, transformation, deduplication, and analytical preparation.
- **Power Query** — final data shaping and integration from Snowflake into the Power BI model.
- **Power BI** — dimensional modeling, DAX measures, KPIs, interactive dashboards, and business analysis.
- **CSV / Excel** — source data.
- **Python / NLP** — customer review enrichment and sentiment analysis.

## Analysis Areas

- Conversion funnel and conversion rates
- Customer engagement and content performance
- Product-level conversion performance
- Views, clicks, and likes trends
- Customer ratings and sentiment
- Customer feedback and recurring themes
- Monthly and product-level performance

## Current Repository Structure

```text
Marketing-Customer-Behaviour-Analytics/
├── README.md
├── data/
├── snowflake/
├── power-query/
├── power-bi/
├── insights/
└── documentation/
```

> SQL scripts, dashboard files, screenshots, insights, and supporting documentation will be added as the project repository is completed.

## Business Context

The project is based on a business case focused on declining customer engagement and conversion rates, the need to improve marketing effectiveness, and the use of customer feedback to guide product and service improvements. fileciteturn7file0L5-L11

The analysis focuses on three main goals: improving conversion rates, enhancing customer engagement, and improving customer feedback scores. fileciteturn7file0L35-L44

## Key Analysis Findings

The reference analysis reports an overall conversion rate of **8.5%**, total views of **2,982,369**, total clicks of **458,345**, total likes of **73,618**, and an average customer rating of **3.7**. fileciteturn7file1L5-L12

The analysis also identifies a decline in views later in the year, relatively low clicks and likes compared with views, and stronger view performance for blog content in selected months. fileciteturn7file1L24-L30

Customer feedback analysis shows **275 positive**, **82 negative**, **60 mixed-negative**, **21 mixed-positive**, and **8 neutral** reviews; the rating distribution includes **140 four-star** and **135 five-star** reviews. fileciteturn7file1L34-L40

## Dashboard

The Power BI dashboard covers conversion, social media engagement, customer reviews, product performance, and monthly trends. Dashboard assets will be added to the repository as the project is finalized.
