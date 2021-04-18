# Cleaning Data with PySpark

> **Source**: DataCamp's "[Cleaning Data with PySpark](https://www.datacamp.com/courses/cleaning-data-with-apache-spark-in-python)" course.

- Defining a Spark schema limits the data import to a single read operation (import performance).
- CSV files cannot be shared between workers during import and do not allow you to leverage _predicate pushdown_ (_predicate pushdown_ means that Spark will only process the data needed instead of reading the entire dataset).
  - Use the Parquet format instead.
- Negation: `~`.
