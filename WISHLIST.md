# Wishlist

- Create an application to consume a currency valuation API and persist this data to enable the monetary values to be converted to USD before it would be persisted as .parquet
- Use a text analysis tool to extract more information from free-form text values compared to the RegEx approaches.
- Convert the exploration notebooks (data_1.ipynb, data_2.ipynb and data_3.ipynb) to a production-ready code:
    - Convert similar transformations to a generic functions (e.g.: salary and bonus transformations)
    - Convert every SparkSQL query to a Python function using PySpark API (SparkSQL was used for better exploration) 
    - Using PySpark API would be possible to also add better tests that could be mocked
    - Use a data quality tool, such as Great Expectations to ensure that every business rule identified in the exploration will be followed or updated.
- Add a charts library to plot some query results to better identify some corner-cases and outliers and better present the analysis.