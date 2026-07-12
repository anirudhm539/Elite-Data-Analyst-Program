# DataFrame Transformations & Actions

## Objective

Learn how PySpark DataFrames are transformed and executed inside Spark.

---

# Transformations

Transformations create a new DataFrame.

They are lazily evaluated and do not execute immediately.

Examples:

- select()
- filter()
- where()
- withColumn()
- drop()
- distinct()
- orderBy()

---

## select()

Used to choose specific columns.

Example:

```python
employee_df.select("name", "salary")
```

---

## filter()

Used to filter rows.

Example:

```python
employee_df.filter(employee_df.salary > 55000)
```

---

## where()

Alternative to filter().

Example:

```python
employee_df.where(employee_df.department == "IT")
```

---

## withColumn()

Creates or modifies a column.

Example:

```python
employee_df.withColumn(
    "annual_salary",
    employee_df.salary * 12
)
```

---

## drop()

Removes columns.

Example:

```python
bonus_df.drop("bonus")
```

---

## distinct()

Removes duplicate records.

Example:

```python
department_df.distinct()
```

---

## orderBy()

Sorts records.

Ascending:

```python
employee_df.orderBy("salary")
```

Descending:

```python
employee_df.orderBy(
    employee_df.salary.desc()
)
```

---

# Actions

Actions trigger execution.

Examples:

- show()
- count()
- collect()
- first()
- take()

Example:

```python
employee_df.show()
```

---

# Transformations vs Actions

Transformations:

- Create new DataFrames
- Do not execute immediately
- Support Lazy Evaluation

Actions:

- Trigger execution
- Return results

---

# Lazy Evaluation

Spark stores transformations as a logical plan.

Execution occurs only when an Action is called.

Benefits:

- Query Optimization
- Reduced Processing Cost
- Better Performance

---

# Execution Plan

Used to understand how Spark will execute a query.

Example:

```python
lazy_df.explain()
```

Execution plans typically include:

- Logical Plan
- Optimized Logical Plan
- Physical Plan

---

# Interview Questions

## What is a Transformation?

A transformation creates a new DataFrame and is lazily evaluated.

## What is an Action?

An action triggers execution and returns results.

## What is Lazy Evaluation?

Spark delays execution until an action is called.

## What does explain() do?

Displays Spark's execution plan and optimization strategy.