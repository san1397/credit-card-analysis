# Credit Card Spent Analysis
Stock Price Analysis

**Summmary**
This project analyzes credit card customer behavior by processing and transforming raw data from multiple sources (customer, transaction, and card details). Using Python and pandas, I cleaned and merged the data, calculated total spend per customer, and categorized them into High, Average, and Low spenders based on percentile metrics. The transformed data was loaded into Snowflake for scalable storage and queried for insights. A dashboard was built using Power BI to visualize spending patterns and identify high-value customers for personalized offers.


**Tech Stack:**
- Python (pandas)
- Snowflake (Data Warehouse)
- Jupyter Notebook
- GitHub

**Key Features**
- Merged multiple CSV datasets to create a unified customer profile
- Cleaned and transformed data using pandas (e.g., date parsing, null handling)
- Calculated total spend per customer
- Created a column spend_category based on:
  - High Spend: >75th percentile
  - Average Spend: 25th–75th percentile
  - Low Spend: <25th percentile
- Loaded clean data into Snowflake warehouse





