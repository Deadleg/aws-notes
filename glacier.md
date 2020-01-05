# S3 Glacier

Not same as storage classes.

## Structure

Data is stored in values. Objects are called archive.

Actions on archives are called `jobs`.

## Inventory

Generated every 24 hours.

## Jobs

Operations are:

- `select` (SQL)
- `archive-retrieval`
- `inventory-retrieval`

### Select

Output to s3 bucket in same region.

### Tiers

- Expidited: 1-5 minute retrieval
- Standard: 3-5 hours
- Bulk: 5-12 hours

## Retrieval policies

- No retrieval limit
- Free tier only
- Max retrieval rate

## Quota

1000 vaults per region. Can delete a vault when all archives are deleted.
