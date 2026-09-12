# Project Workflow

## End-to-end pipeline

```text
CSV / Excel
    ↓
Snowflake RAW_DATA
    ↓
Streams
    ↓
Tasks
    ↓
Snowflake CLEAN_DATA
    ↓
Power Query
    ↓
Power BI
    ↓
DAX + Dimensional Model + Interactive Dashboard
```

## Snowflake layers

### RAW_DATA

Source datasets are loaded into the RAW_DATA layer.

### CLEAN_DATA

Cleaning, transformation, deduplication, enrichment, and incremental synchronization are handled in Snowflake before the data is consumed by Power BI.

### Streams & Tasks

Streams track changes in RAW_DATA tables and Tasks process eligible changes into CLEAN_DATA tables using incremental MERGE logic.

The complete SQL implementation will be documented in the `snowflake/` directory when the final SQL code is provided.

## Power BI layer

Power Query connects to the Snowflake CLEAN_DATA layer and preserves the existing Power BI model naming where required. The Power BI model contains fact and dimension tables for customer journeys, reviews, engagement, customers, products, geography, and calendar analysis.
