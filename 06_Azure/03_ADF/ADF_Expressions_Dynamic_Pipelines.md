# ADF Expressions & Dynamic Pipeline Design

## Expressions
Runtime formulas used to generate dynamic values.

## Common Expressions

Current Time:
@utcNow()

Pipeline Parameter:
@pipeline().parameters.FileName

Variable:
@variables('CurrentFile')

## Date Functions

Year:
@formatDateTime(utcNow(),'yyyy')

Month:
@formatDateTime(utcNow(),'MM')

Day:
@formatDateTime(utcNow(),'dd')

## String Functions

concat()

toUpper()

toLower()

replace()

length()

## Benefits

- Reusability
- Scalability
- Less Hardcoding
- Enterprise Ready

## Interview Notes

- Expressions
- Dynamic Pipelines
- concat()
- utcNow()
- Pipeline Parameters