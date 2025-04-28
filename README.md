# stockpriceanalysis
Stock Price Data Analysis - PySpark Project

Project Overview
This project demonstrates a simple stock price data analysis using PySpark. The goal was to analyze historical stock price data and extract key metrics such as average stock prices, daily percentage change, and the highest/lowest stock prices. The project showcases the use of PySpark to process and analyze large financial datasets efficiently.

Tools Used
1. PySpark: For processing and analyzing large-scale datasets.
2. Python: Programming language used to implement the analysis logic.
3. CSV: Dataset format used for storing and loading stock price data.
4. Databricks: provided a managed Apache Spark environment for scalable and efficient data analysis.
5. Apache Spark: Distributed computing framework used for handling large data efficiently.

Data
The dataset used for this project contains historical stock price information, including columns like:
- **date**: Date of the stock price data.
- **stock_symbol**: Unique identifier for each stock.
- **open**: Opening price for the stock on a given day.
- **high**: Highest price for the stock during the day.
- **low**: Lowest price for the stock during the day.
- **close**: Closing price for the stock on the given day.
- **volume**: Volume of stock traded.

Methodology
The project followed these steps for data processing and analysis:
1. **Data Loading**: Loaded the stock price data into a PySpark DataFrame from CSV files.
2. **Data Cleaning**: Handled missing values using `dropna()` and removed duplicate rows with `dropDuplicates()`.
3. **Data Transformation**: Applied transformations such as calculating daily percentage change and calculating average prices.
4. **Aggregation**: Used `groupBy()` and `agg()` to calculate metrics like average price, highest price, and lowest price per stock.
5. **SQL Operations**: Registered the DataFrame as a temporary SQL table and used SQL queries to analyze the data.
6. **File Writing**: Exported the cleaned and transformed data to CSV files for further analysis.

Key PySpark Functions
1. **groupBy()**: Used to group the data by stock symbol for aggregation.
2. **agg()**: Applied aggregation functions like average, max, and min.
3. **withColumn()**: Used to add new columns, such as calculating the daily percentage change.
4. **filter()**: Filtered data based on conditions like price thresholds.
5. **select()**: Selected specific columns from the DataFrame.
6. **createOrReplaceTempView()**: Registered the DataFrame as a temporary SQL table to run SQL queries.
7. **write.csv()**: Saved the final output to a CSV file.


Conclusion
This project provided a practical introduction to PySpark, showcasing how to handle large financial datasets, perform basic stock price analysis, and export the results for further reporting. The use of PySpark's distributed processing power allowed for efficient data manipulation, even with large datasets. This project can be extended by incorporating more advanced techniques like time-series analysis or machine learning for stock price prediction.
