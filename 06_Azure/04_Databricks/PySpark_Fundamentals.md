# PySpark Fundamentals

## Introduction

PySpark is the Python API for Apache Spark.

It allows developers to write Spark applications using Python while taking advantage of Spark's distributed processing capabilities.

PySpark is one of the most widely used technologies in modern Data Engineering because it combines the simplicity of Python with the power of Apache Spark.

Organizations use PySpark to process:

* Large datasets
* Data Lake workloads
* ETL pipelines
* Data transformations
* Data quality checks
* Analytics datasets

PySpark is considered one of the most important skills for Data Engineers working with Azure Databricks.

---

# What is PySpark?

PySpark is a Python interface for Apache Spark.

Instead of writing Spark code in Scala or Java, developers can use Python syntax.

PySpark allows users to:

* Read data
* Transform data
* Aggregate data
* Join datasets
* Clean data
* Write processed data

while Spark handles distributed execution in the background.

---

# Why Companies Use PySpark

Traditional Python works well for small datasets.

However, when data grows into hundreds of gigabytes or terabytes, traditional processing becomes slow.

PySpark solves this problem by distributing workloads across multiple machines.

Benefits include:

* Faster processing
* Scalability
* Fault tolerance
* Big data support
* Cloud integration

---

# PySpark Architecture

PySpark operates on top of Apache Spark.

Architecture Flow:

Python Code

↓

PySpark API

↓

Spark Driver

↓

Spark Executors

↓

Distributed Processing

↓

Results

The developer writes Python code, while Spark handles task distribution automatically.

---

# Key Components of PySpark

## Spark Session

Spark Session is the entry point for working with Spark.

Every PySpark application starts with a Spark Session.

Example:

spark = SparkSession.builder.appName("SalesAnalysis").getOrCreate()

The Spark Session provides access to Spark functionality.

---

## DataFrame

A DataFrame is the most important object in PySpark.

It represents structured data organized into rows and columns.

Example:

| CustomerID | Name  | City   |
| ---------- | ----- | ------ |
| 101        | Rahul | Delhi  |
| 102        | Priya | Mumbai |

DataFrames are similar to tables in SQL.

---

## Transformations

Transformations modify data and create a new DataFrame.

Examples:

* Select
* Filter
* Join
* Group By
* Sort

Transformations are lazy and are not executed immediately.

---

## Actions

Actions trigger execution and return results.

Examples:

* Show
* Count
* Collect
* First

Actions cause Spark to execute the transformation plan.

---

# Lazy Evaluation

One of Spark's most important concepts is Lazy Evaluation.

When transformations are applied, Spark does not execute immediately.

Instead, Spark creates an execution plan.

Execution occurs only when an action is called.

Example:

Filter Data

↓

Select Columns

↓

Group Data

↓

Count Records

Execution starts only during Count.

Benefits:

* Better optimization
* Faster performance
* Reduced resource usage

---

# DataFrame vs Pandas

| Feature            | Pandas          | PySpark     |
| ------------------ | --------------- | ----------- |
| Dataset Size       | Small to Medium | Very Large  |
| Processing         | Single Machine  | Distributed |
| Scalability        | Limited         | High        |
| Speed for Big Data | Slow            | Fast        |
| Memory Dependency  | High            | Distributed |

---

# Common PySpark Operations

## Reading Data

Used to load files into DataFrames.

Common formats:

* CSV
* JSON
* Parquet
* Delta

---

## Selecting Columns

Used to retrieve specific columns.

Example:

CustomerID

CustomerName

SalesAmount

---

## Filtering Data

Used to retrieve specific records.

Example:

Sales greater than ₹10,000.

---

## Sorting Data

Used to arrange data.

Example:

Highest sales first.

---

## Grouping Data

Used for aggregation.

Examples:

Total Sales by Region

Average Sales by Product

Maximum Revenue by Month

---

## Joining Data

Combines multiple datasets.

Example:

Customer Data

*

Sales Data

↓

Customer Sales Report

---

# Enterprise Example

Retail Company

Input Files:

sales_aug_2026.csv

customer_master.csv

product_master.csv

Workflow:

ADF

↓

ADLS Bronze

↓

PySpark Reads Files

↓

Data Cleaning

↓

Data Validation

↓

Business Rules

↓

Silver Layer

↓

Aggregation

↓

Gold Layer

↓

Power BI

PySpark performs all major transformations.

---

# Benefits of PySpark

## Scalability

Processes massive datasets.

---

## Performance

Uses distributed computing.

---

## Fault Tolerance

Recovers automatically from failures.

---

## Cloud Integration

Works seamlessly with Databricks and Azure.

---

## Python Simplicity

Easy for Python developers to learn.

---

# Best Practices

1. Use DataFrames instead of older RDDs.
2. Avoid unnecessary collect operations.
3. Filter data early.
4. Select only required columns.
5. Use partitioning wisely.
6. Cache frequently used datasets.
7. Monitor job performance.
8. Follow notebook documentation standards.

---

# Common Beginner Mistakes

## Using collect() on Huge Data

Can crash memory.

---

## Selecting All Columns

Leads to unnecessary processing.

---

## Ignoring Lazy Evaluation

Creates confusion during debugging.

---

## Poor Data Quality Checks

Produces unreliable outputs.

---

# Interview Questions

## Question 1

What is PySpark?

### Answer

PySpark is the Python API for Apache Spark that enables distributed data processing using Python.

---

## Question 2

What is a DataFrame?

### Answer

A DataFrame is a distributed collection of structured data organized into rows and columns.

---

## Question 3

What is Lazy Evaluation?

### Answer

Spark delays execution until an action is triggered, allowing optimization of execution plans.

---

## Question 4

What is the difference between Transformations and Actions?

### Answer

Transformations create execution plans while Actions trigger execution and return results.

---

## Question 5

Why is PySpark preferred for Big Data?

### Answer

PySpark distributes processing across multiple machines, making it scalable and efficient for large datasets.

---

## Question 6

What is the role of Spark Session?

### Answer

Spark Session is the entry point for interacting with Spark and creating DataFrames.

---

# Key Takeaways

* PySpark is the Python API for Apache Spark.
* It enables distributed data processing.
* DataFrames are the primary data structure.
* Transformations are lazy.
* Actions trigger execution.
* PySpark is a core skill for Databricks professionals.
* Most enterprise ETL pipelines rely heavily on PySpark.
