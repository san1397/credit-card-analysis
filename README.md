# Stock Price Analysis
Stock Price Analysis


**Tech Stack:**
- **Data Storage** - AWS S3
- **ETL & Transformation** - AWS Glue
- **Querying** - AWS Athena
- **Data Cataloging** - AWS Glue Crawler
- **Monitoring** - AWS CloudWatch
- **Access & Permissions** - AWS IAM
- **Data Warehouse** - Snowflake
- **Visualization** - Power BI

**Data Ingestion**
- I received millions of records of stock price data in CSV format.
- Columns - date, stock_symbol, open, high, low, close, volume
- Uploaded the raw files to an S3 bucket

**Data Cataloging with Glue Crawler**
- Created Glue Crawler to scan the CSV files and automatically create a table in the AWS Glue Data Catalog.
- Now I can query the raw data using Athena without manual schema definition.

  **Data Transformation using AWS Glue**
- Create an AWS Glue Job to transform the raw stock data.
- Key transformations:
     - Drop duplicates and nulls
     - Convert data column to proper format
     - Create new columns
     - After transformation, I saved the cleaned data in Parquet format in S3.

 **Data Load to Snowflake**
 - I used a connector to load the cleaned data from S3 to Snowflake.
 - In Snowflake, I created a table for analysis

**Querying with AWS Athena**
- Before loading into Snowflake, I ran SQL queries using Athena to validate the transformation

**Access Management with AWS IAM**
- Created IAM roles for:
   * Glue job execution
   * Athena query access
   * Snowflake data loading

**Monitoring with CloudWatch**
- Enavled CloudWatch Logs for Glue job runs
- Created alerts for Glue Job failures using CloudWatch Alarms
