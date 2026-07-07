# Azure Data Factory Introduction

## 1. What is Azure Data Factory

Azure Data Factory (ADF) is a cloud-based data integration service provided by Microsoft Azure.
It is used to automate data movement and data workflows.
ADF helps organizations build ETL and ELT pipelines.
It can connect to various data sources and destinations.

## 2. Why Companies Use ADF

Companies use ADF to automate repetitive data processing tasks.
It reduces manual effort and improves reliability.
ADF supports scheduling, monitoring, and orchestration of data workflows.
It helps organizations manage large-scale data pipelines efficiently.

## 3. Pipeline

A pipeline is a collection of activities that perform a complete workflow.
It defines the sequence of tasks required to process data.
A pipeline can include copying, transforming, and validating data.

## 4. Activity

An activity is an individual task inside a pipeline.
Examples include Copy Data, Lookup, ForEach, and Execute Pipeline.
Multiple activities together form a complete pipeline.

## 5. Linked Service

A Linked Service is a connection configuration used by ADF.
It allows ADF to connect to data sources and destinations.
Examples include Azure SQL Database, ADLS Gen2, and APIs.

## 6. Dataset

A Dataset represents a specific data structure within a data store.
It can point to a file, table, or collection of data.
Datasets are used by activities to read and write data.

## 7. Integration Runtime

Integration Runtime (IR) is the execution engine of Azure Data Factory.
It performs data movement and activity execution.
Azure IR is commonly used for cloud-based data integration.

## 8. ADF vs Databricks

ADF is mainly used for orchestration, scheduling, and data movement.
Databricks is used for large-scale data transformation and analytics.
ADF manages workflows while Databricks performs heavy data processing.

## 9. ADF vs SSIS

SSIS is a traditional on-premises ETL tool from Microsoft.
ADF is a modern cloud-based data integration service.
ADF provides better scalability and cloud-native capabilities.

## 10. Real Company Architecture

Source systems such as ERP, CRM, APIs, and databases send data to ADF.
ADF loads the data into ADLS Bronze layer.
Data is then transformed into Silver and Gold layers.
Power BI consumes Gold layer data for reporting and analytics.