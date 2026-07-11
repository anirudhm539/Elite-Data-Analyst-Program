# ADF Enterprise Logging & Audit

## What is Logging
Recording execution details of pipelines and activities.

Examples:
- Pipeline Started
- Pipeline Completed
- Pipeline Failed

## What is Audit
Tracking who made changes and when.

Examples:
- Pipeline Modified
- Trigger Updated
- Deployment Performed

## Logging vs Audit

Logging:
Tracks system execution details.

Audit:
Tracks user actions and changes.

## Enterprise Logging Architecture

ADF Pipeline
    ↓
Activity Logs
    ↓
Log Analytics
    ↓
Azure Monitor
    ↓
Alerts

## Common Log Fields

Pipeline Name
Run ID
Start Time
End Time
Status
Rows Processed
Error Message

## Success Logging

Pipeline: PL_Sales_Load
Status: Success
Rows Processed: 250000

## Failure Logging

Pipeline: PL_Sales_Load
Status: Failed
Error: File Not Found

## Audit Trail

Modified By: Rahul
Action: Updated Watermark Logic
Date: 01-Aug-2026

## Azure Monitor

Used for:
- Metrics
- Alerts
- Dashboards

## Log Analytics

Used for:
- Log Queries
- Error Analysis
- Historical Monitoring

## Activity Log

Tracks:
- Resource Changes
- Deployments
- User Actions

## Enterprise Alerting Strategy

Alert When:
- Pipeline Fails
- File Missing
- Runtime Increases
- Data Volume Drops

## Production Support Flow

Pipeline Failed
    ↓
Check Logs
    ↓
Find Root Cause
    ↓
Fix Issue
    ↓
Re-run Pipeline

## Interview Notes

Q. Difference between Logging and Audit?
A. Logging tracks system events, Audit tracks user actions.

Q. Why is logging important?
A. Helps identify failures and troubleshoot production issues.

Q. Which Azure services help in monitoring?
A. Azure Monitor, Log Analytics, Activity Log.