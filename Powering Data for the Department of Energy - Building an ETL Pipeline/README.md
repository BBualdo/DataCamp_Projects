﻿# ⚡ Powering Data for the Department of Energy - Building an ETL Pipeline

### Project Description
You’ve started as a Data Engineer at an energy company, tasked with automating the manual, time-consuming process analysts previously used to retrieve and clean quarterly sales and capability data. Your goal is to build a monthly data pipeline to streamline insights and save time for data consumers.

## 🎯 Objective

1. First, define an `extract_tabular_data()` function to ingest tabular data. This function will take a single parameter, `file_path`. If `file_path` ends with .csv, use the `pd.read_csv()` function to extract the data. If `file_path` ends with `.parquet`, use the `pd.read_parquet()` function to extract the data. Otherwise, raise an exception and print the message: _"Warning: Invalid file extension. Please try with `.csv` or `.parquet`!"._

2. Create another function with the name `extract_json_data()`, which takes a `file_path`. Use the `json_normalize()` function from the `pandas` library to flatten the nested JSON data, and return a pandas `DataFrame`.

3. Next, we'll need to build a function to transform the electricity sales data. To do that, we'll create a function called `transform_electricity_sales_data()` which takes a single parameter `raw_data`. `raw_data` should be of type `pd.DataFrame`. The `transform_electricity_sales_data()` needs to fulfill some requirements that are described below in the docstring following the function definition.

4. To load a DataFrame to a file, we'll define one more function called `load()`, which takes a DataFrame and a `file_path`. If the `file_path` ends with `.csv`, load the DataFrame to a CSV file. If instead the `file_path` ends with `.parquet`, load the DataFrame to a Parquet file. Otherwise, raise an exception that outputs a message in this format: _"Warning: {filepath} is not a valid file type. Please try again!_"_