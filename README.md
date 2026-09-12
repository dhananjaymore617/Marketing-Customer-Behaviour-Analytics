# Marketing & Customer Behaviour Analytics

An end-to-end marketing analytics project using **Snowflake, Power BI, DAX, and Power Query** to analyze customer engagement, conversion funnels, product performance, and customer feedback.

## Project Workflow

**CSV / Excel → Snowflake (RAW_DATA + CLEAN_DATA, Streams & Tasks) → Power Query → Power BI**

## Objective

Analyze customer conversion, marketing engagement, product performance, and customer feedback to identify opportunities for improving conversion, engagement, and customer satisfaction.

## Technology Stack

- **Snowflake** — cloud data warehouse with RAW_DATA and CLEAN_DATA layers, Streams for change tracking, and Tasks for scheduled incremental processing.
- **SQL** — database setup, data loading, validation, cleaning, transformation, deduplication, and incremental processing.
- **Power Query** — data shaping and integration from Snowflake into the Power BI model.
- **Power BI** — dimensional data modeling, DAX measures, KPIs, interactive dashboards, and business analysis.
- **CSV / Excel** — source data.

## Analysis Areas

- Conversion funnel and conversion rates
- Customer engagement
- Product-level conversion performance
- Views, clicks, and likes
- Customer ratings and sentiment
- Customer feedback
- Monthly and product-level performance

## Repository Structure

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

## Business Context

The project analyzes a marketing analytics business case involving customer engagement, conversion performance, and customer feedback. The supplied business-case presentation is being used only as reference material for understanding the business problem, objectives, analytical questions, and intended use of the analysis.

## Dashboard

The Power BI dashboard and supporting assets will be added to the repository as the project is finalized.

## Note

The Snowflake SQL implementation will be added to the `snowflake/` section and expanded later as the complete SQL scripts are provided.
