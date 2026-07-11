# ADF Variables, System Variables & Metadata

## Variables
- Temporary runtime storage
- Types:
  - String
  - Integer
  - Boolean
  - Array

## Activities
- Set Variable
- Append Variable

## System Variables
- Pipeline Name
- Run ID
- Trigger Name
- Trigger Time

## Metadata
Metadata = Data about Data

## Get Metadata Activity
Used to retrieve:

- Exists
- Size
- Last Modified
- Child Items

## Common Pattern

Get Metadata
↓
ForEach
↓
Copy Activity

## Production Practices
- Check file existence
- Use child items for automation
- Store run information

## Interview Notes
- Variable vs Parameter
- Metadata
- Child Items
- Get Metadata Activity