# Credit Card Spent Analysis

**Summmary** 
This project analyzes credit card customer behavior by processing and transforming raw data from multiple sources (customer, transaction, and card details). Using Python and pandas, I cleaned and merged the data, calculated total spend per customer, and categorized them into High, Average, and Low spenders based on percentile metrics. The transformed data was loaded into Snowflake for scalable storage and queried for insights. A dashboard was built using Power BI to visualize spending patterns and identify high-value customers for personalized offers.


**Tech Stack:**
- AWS S3 : Data Lake to store raw and transformed files.
- AWS Glue : Used for data transformation.
- AWS Lambda : Trigger Glue job when new file lands in S3
- AWS CloudWatch : Monitoring and logging job performance

**Process**
- Raw CSV files with 100000+ records is uploaded to S3.
- AWS Glue reads the file using PySpark, caste data types, drops unnecessary columns, and adds new metrics.
    - Credit Utilization Ratio = current_balance/credit_limit
    - Spend_category(High/Average/Low)
- Transformed data is written back to S3.
- Lambda function triggers Glue job on new file detection.
- CloudWatch monitors job logs and metrics.
- Transformed data is loaded into Snowflake.

**Outcome** 
Efficient, scalable ETL pipeline built with serverless AWS services, ensuring automated data
ingestion, transformation, and warehousing.




