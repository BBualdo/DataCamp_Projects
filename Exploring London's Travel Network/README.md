# 🚌 Exploring London's Travel Network

### Project Description
How do Londoners get around? Transport for London (TfL) is a vast public transport network that allows London's residents to efficiently travel around the UK's capital, to the tune of over 1.5 million journeys per day!

In this introductory project, you will work with a Snowflake, Amazon Redshift, Google BigQuery, or Databricks database containing data on journeys and transport types in London between 2010 and 2022. You will write SQL queries to find the most popular transport methods, examine when the London cable car (which connects London's Royal Docks, where the Mayor's office is located, to Greenwich Peninsula, home of the O2 arena) was particularly busy, and identify rare periods when the Underground (also known as "the tube" to locals) was less busy.

## 🎯 Objective

Write three SQL queries to answer the following questions:

What are the most popular transport types, measured by the total number of journeys? The output should contain two columns, 1) `journey_type` and 2) `total_journeys_millions`, and be sorted by the second column in descending order. Save the query as `most_popular_transport_types`.

Which five months and years were the most popular for the Emirates Airline? Return an output containing month, year, and `journeys_millions`, with the latter rounded to two decimal places and aliased as `rounded_journeys_millions`. Exclude null values and save the result as `emirates_airline_popularity`. Note - in Databricks SQL, aliased column names cannot be used in a `WHERE` clause, you will need to use original column names.

Find the five years with the lowest volume of `Underground & DLR journeys`, saving as `least_popular_years_tube`. The results should contain the columns `year`, `journey_type`, and `total_journeys_millions`.

Three SQL cells have been created for you in the workbook. To access the Databricks database, you will need to select data using the syntax `FROM tfl.journeys` (selecting from `journeys` without referring to the `tfl` schema first will result in an error).

**Note:** Please also ensure that you do not change the names of the DataFrames that the three query results will be saved as - creating new cells in the workbook will rename the DataFrame (see image below). Make sure that your final solutions use the names provided: `most_popular_transport_types`, `emirates_airline_popularity`, and `least_popular_years_tube`.