# Power Query

Power Query is used as the integration and final shaping layer between Snowflake `CLEAN_DATA` and the Power BI data model.

The final Power Query M definitions will be documented here after the source migration is finalized.

## Current flow

```text
Snowflake CLEAN_DATA
        ↓
Power Query
        ↓
Column naming / final shaping
        ↓
Power BI model
```

Existing Power BI table names and column names are intentionally preserved where required so that the existing relationships, visuals, and DAX measures remain compatible with the migrated Snowflake source.
