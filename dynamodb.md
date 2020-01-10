# DynamoDB

## Consistency

Eventually consistant in general, can be strongly consistent.

Cannot be used on global secondary indexes.

## Scan

Max size 1MB. Limit is applied before filters.

Eventually consistant, can set `ConsistentRead=true` to strong consistency. Consumes twice as many read capacity units.

Can parallel scan by specifying

- Total segments (same on every request).
- Segment number (unique)

## Transactions

Up to 25 write operations.

Cannot target the same item with multiple operations.

Operations:
- Put
- Update
- Delete
- ConditionCheck

## Capacity modes

Can switch between modes once every 24 hours.

Max item size 400KB

### On-demand

1 RQU=1 strongly consistent or 2 eventually consistant reads for up to 4KiB.
1 WQU=1 strongly write up to 1 KiB. Transactions require 2 units.

### Provisioned

1 RQU=1 strongly consistent or 2 eventually consistant reads for up to 4KiB. Transactions require 2 units.
1 WQU=1 strongly write up to 1 KiB. Transactions require 2 units.

## Indexes

Can only create one at a time.

### Global secondary index

Up to 20 per table. Has it's own capacity units.

### Local secondary index

Up to 5 per table. Can only create a table creation time. Inherits capacity units of table. 10GB limit on total number of items per partition key.

Sort keys do not need to be unique.
