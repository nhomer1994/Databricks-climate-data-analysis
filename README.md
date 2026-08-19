# Global Climate Data Analysis within Databricks and dbt

A data engineering pipeline built within **Databricks** with **dbt**. This project ingests, structures, and analyses global monthly climate anomalies using a serverless Medallion Architecture.

1. **Bronze (Raw)**: Ingests monthly global temperature anomaly files from NASA GISS into a managed Unity Catalog Volume.
2. **Silver (Cleaned)**: Restructures the matrix from a wide schema into a long-form format using PySpark `unpivot` for optimal querying.
3. **Gold (Analytics)**: Computes a 10-year rolling moving average using SQL window functions to smooth out seasonal noise.

Example output:

<img width="818" height="430" alt="Screenshot 2026-08-06 at 20 50 48" src="https://github.com/user-attachments/assets/5b522edf-c7c0-4d60-bff4-64d143270913" />

## How to Run 

1. Import the notebooks into your **Databricks Git Folder**.
2. Query the final `gold_decadal_trends` table using the **Databricks SQL Editor** to visualize the metrics.

### Currently updating to use dbt for better handling of data transforms
