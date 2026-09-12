# Snowflake

This folder contains the Snowflake implementation for the Marketing & Customer Behaviour Analytics project.

## Architecture

```text
CSV / Excel
    ↓
RAW_DATA
    ↓
Streams
    ↓
Tasks
    ↓
CLEAN_DATA
    ↓
Power Query
    ↓
Power BI
```

## SQL organization

| File | Purpose |
|---|---|
| `00_complete_original.sql` | Exact SQL supplied for the project, including comments, exploratory queries, tests, and commented-out alternatives. |
| `01_database_setup.sql` | Warehouse, database, and schema setup. |
| `02_streams.sql` | Streams used for change tracking on RAW_DATA tables. |
| `03_eda_and_cleaning.sql` | EDA, duplicate checks, data-quality checks, and transformation queries. |
| `04_clean_tables.sql` | CLEAN_DATA table creation and initial customer-journey transformation/load. |
| `05_tasks.sql` | Incremental MERGE Tasks for customer journey, customers, geography, products, and engagement. |
| `06_testing_and_validation.sql` | Test inserts, stream checks, task checks, and validation queries. |

## Important note

The original SQL contains intentionally commented statements, exploratory queries, intermediate checks, and test queries. They have **not** been deleted. The complete original script is preserved in `00_complete_original.sql`, while the other files organize the implementation by purpose so the repository is easier to read and present.

The supplied SQL does not contain a completed incremental Customer Reviews Task, so no review task has been invented. Customer-review enrichment remains part of the separate review-data workflow.
