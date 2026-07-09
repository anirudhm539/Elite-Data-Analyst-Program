# ADF Parameters & Dynamic Content

## Why Parameters
- Avoid hardcoded values
- Build reusable pipelines

## Parameter Types
1. Pipeline Parameters
2. Dataset Parameters
3. Linked Service Parameters

## Dynamic Content
- Runtime value generation
- Supports reusable designs

## Common Expressions

Pipeline Parameter:
@pipeline().parameters.FileName

Current Time:
@utcNow()

Current Year:
@formatDateTime(utcNow(),'yyyy')

Current Month:
@formatDateTime(utcNow(),'MM')

## Benefits
- Reusability
- Scalability
- Lower maintenance
- Enterprise-ready pipelines

## Interview Notes
- Pipeline Parameters
- Dynamic Content
- Parameterization Benefits