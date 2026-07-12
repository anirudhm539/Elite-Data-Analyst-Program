# Spark Session, DataFrames & First PySpark Program

## Objective

Learn how to create and work with Spark DataFrames in Azure Databricks.

---

# Spark Session

Spark Session is the entry point to Spark.

Databricks automatically creates:

```python
spark
```

Unlike standalone Spark:

```python
from pyspark.sql import SparkSession

spark = SparkSession.builder \
    .appName("Demo") \
    .getOrCreate()
```

---

# First Databricks Program

```python
print("Hello Databricks")
```

Output:

```text
Hello Databricks
```

---

# Create Dataset

```python
data = [
    ("Anirudh", 50000),
    ("Rahul", 60000),
    ("Priya", 70000)
]

columns = ["name", "salary"]
```

---

# Create DataFrame

```python
df = spark.createDataFrame(data, columns)
```

Spark automatically inferred schema:

```text
name   -> string
salary -> long
```

---

# Display DataFrame

```python
display(df)
```

Databricks interactive visualization.

Features:

- Sorting
- Filtering
- Charts
- Export

---

# Show DataFrame

```python
df.show()
```

Output:

```text
+-------+------+
| name  |salary|
+-------+------+
|Anirudh|50000 |
|Rahul  |60000 |
|Priya  |70000 |
+-------+------+
```

---

# Select Columns

```python
df.select("name","salary").show()
```

Used to retrieve required columns.

---

# Print Schema

```python
df.printSchema()
```

Output:

```text
root
 |-- name: string (nullable = true)
 |-- salary: long (nullable = true)
```

---

# display() vs show()

## display()

Databricks-specific.

Used for:

- Exploration
- Visualization
- Analysis

## show()

Native Spark function.

Used for:

- Debugging
- Development
- Production support

---

# Interview Questions

## What is SparkSession?

SparkSession is the entry point for working with Spark.

## What is a DataFrame?

A distributed tabular data structure organized into rows and columns.

## Difference between display() and show()?

display() is Databricks-specific and interactive.

show() is native Spark and works in any Spark environment.

---

# Enterprise Usage

DataFrames are used for:

- ETL Pipelines
- Data Engineering
- Analytics Processing
- Data Transformation
- Reporting Pipelines