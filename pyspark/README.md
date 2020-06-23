# PySpark

## Notes

These notes are based on DataCamp's "[Introduction to PySpark](https://www.datacamp.com/courses/introduction-to-pyspark)" course.

- Spark DataFrames are immutable.
- The `.withColumn()` method returns all columns plus a new one.
- It is possible to apply column-wise operations in the `.select()` method:
  - `df.select(df.col+10)`
- The `.selectExpr()` method takes SQL expressions as a string:
  - `df.selectExpr("col+60 as new_col")`
- The aggregation methods are methods of the `pyspark.sql.GroupedData` class. Thus, to compute the minimum value of a column, for example, it is necessary to _group_ first (another option is to use the `.agg()` method):
  - `df.groupBy().min("col").show()`
- `import pyspark.sql.functions as F`
- Use the `.withColumnRenamed()` method to rename a column.
