﻿# ♻️ Building a Retail Data Pipeline

### Project Description
Mastering data pipelines is essential for Data Engineers today. It involves extracting, transforming, and loading data — a fundamental task that ensures information flows smoothly.

In this project, you will work with retail data from a multinational retail corporation Walmart. You will retrieve data from different sources, like SQL and parquet; prepare the data using some transformation techniques, and finally load the data in an easy-to-access format.

## 🎯 Objective

Build a data pipeline using custom functions to extract, transform, aggregate, and load e-commerce data. The SQL query for grocery_sales and the `extract()` function have already been implemented for you.

To start the project, **run the first two cells**, then proceed with the following steps:

1. Implement a function named `transform()` with one argument, taking `merged_df` as input, filling missing numerical values (using any method of your choice), adding a column `"Month"`, keeping the rows where the weekly sales are over $10,000 and drops the unnecessary columns. Ultimately, it should return a DataFrame and be stored as the `clean_data` variable.

2. Implement the function `avg_weekly_sales_per_month` with one argument (the cleaned data). This function will calculate the average monthly sales. For implementing this function you must select the "Month" and "Weekly_Sales" columns as they are the only ones needed for this analysis, then create a chain operation with `groupby()`, `agg()`, `reset_index()`, and `round()` functions, then group by the "Month" column and calculate the average monthly sales, then call `reset_index()` to start a new index order and finally round the results to two decimal places.

3. Create a function called `load()` that takes the cleaned and aggregated DataFrames, and their paths, and saves them as `clean_data.csv` and `agg_data.csv` respectively, without an index.

4. Lastly, define a `validation()` function that checks whether the two `csv` files from the `load()` exist in the current working directory.

**Note:** No engine is required to connect to the database, just execute your query in the SQL code cell provided, and the output will automatically be stored as a pandas DataFrame called `grocery_sales`, available for you to use in Python code cells.