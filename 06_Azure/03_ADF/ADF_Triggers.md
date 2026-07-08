# ADF Triggers

## 1. What is a Trigger

A Trigger is a mechanism that automatically starts a pipeline based on a schedule or event.

## 2. Types of Triggers

- Schedule Trigger
- Tumbling Window Trigger
- Event Trigger

## 3. Schedule Trigger

A Schedule Trigger runs pipelines at fixed intervals such as daily or hourly.

## 4. Trigger Configuration

Trigger Name: TR_Daily_Sales_Load
Type: Schedule
Recurrence: Every 1 Day
Execution Time: 08:00 AM

## 5. Trigger Naming Standard

TR_ prefix is used for trigger names.

## 6. Business Use Cases

- Daily Data Load
- Hourly Refresh
- Automated Reporting
- Scheduled ETL Pipelines

## 7. Trigger vs Debug

Debug is used for testing.
Trigger is used for automated execution.

## 8. Interview Questions

Triggers are commonly used to automate pipeline execution based on schedules or events.