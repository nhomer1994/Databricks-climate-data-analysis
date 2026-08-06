# Global Climate Data Analysis within Databricks

A data engineering pipeline built entirely within the **Databricks**. This project ingests, structures, and analyzes global monthly climate anomalies using a serverless Medallion Architecture.

1. **Bronze (Raw)**: Ingests monthly global temperature anomaly files from NASA GISS into a managed Unity Catalog Volume.
2. **Silver (Cleaned)**: Restructures the matrix from a wide schema into a long-form format using PySpark `unpivot` for optimal querying.
3. **Gold (Analytics)**: Computes a 10-year rolling moving average using SQL window functions to smooth out seasonal noise.

## How to Run 

1. Import the notebooks into your **Databricks Git Folder**.
2. Query the final `gold_decadal_trends` table using the **Databricks SQL Editor** to visualize the metrics.
