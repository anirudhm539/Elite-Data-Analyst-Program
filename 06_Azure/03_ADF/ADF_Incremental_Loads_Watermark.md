# ADF Incremental Loads & Watermark Pattern

## Incremental Load
Load only new or changed records.

## Benefits
- Faster
- Lower Cost
- Scalable
- Enterprise Standard

## Watermark
Tracks last successful load.

Common Columns:
- LastModifiedDate
- CreatedDate
- UpdatedDate

## Watermark Pattern

Read Watermark
↓
Load New Records
↓
Update Watermark

## Strategies
1. Timestamp Based
2. ID Based
3. File Based

## Best Practices
- Store watermark separately
- Update watermark after success
- Maintain audit logs

## Interview Notes
- Incremental Load
- Full Load vs Incremental Load
- Watermark Pattern