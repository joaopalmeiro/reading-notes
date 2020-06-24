# PySpark

## Notes

These notes are based on DataCamp's "[Introduction to PySpark](https://www.datacamp.com/courses/introduction-to-pyspark)" course:

- Spark DataFrames are immutable.
- The `.withColumn()` method returns all columns plus a new one.
- It is possible to apply column-wise operations in the `.select()` method:
  - `df.select(df.col+10)`
- The `.selectExpr()` method takes SQL expressions as a string:
  - `df.selectExpr("col+60 as new_col")`
- The aggregation methods are methods of the `pyspark.sql.GroupedData` class. Thus, to compute the minimum value of a column, for example, it is necessary to _group_ first (another option is to use the `.agg()` method):
  - `df.groupBy().min("col").show()`
- Use the `.withColumnRenamed()` method to rename a column.
- Spark only handles numeric data for modeling.
- `label` is the default name for the target variable.
- Split the data only after all the transformations.
  - `StringIndexer`, for example, does not always produce the same index even considering the same list of strings.
- Imports:
  - `import pyspark.sql.functions as F`
  - `import pyspark.ml.evaluation as evals`
  - `import pyspark.ml.tuning as tune`

These notes are based on DataCamp's "[Cleaning Data with PySpark](https://www.datacamp.com/courses/cleaning-data-with-apache-spark-in-python)" course:

- Normally, when importing data, an attempt is made to infer a schema, which implies reading the data twice. Defining a (Spark) schema limits this to a single read operation (import performance).
- CSV files cannot be shared between workers during import and do not allow you to leverage _predicate pushdown_ (Spark will only process the data needed instead of reading the entire dataset).
  - Use the Parquet format instead.
