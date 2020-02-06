# snapshots

## Sharing

Sharing unencrypted snapshot with another account allows other account to restore directly from that snapshot. Cannot share mssql/oracle with TDE

## Storage

### gp2

Up to 64TiB of storage except SQLServer up to 16TiB. Min 20GiB

### Provisioned IOPs

100 GiB - 64TiB _except_ sqlserver, max 16 TiB, min 20GiB for express/web, 100GiB otherwise.

1,000 - 80,000 IOPs _except_ sqlserver max 64,000 on Nitro instances

## Read replicas

MariaDB, MySQL, Oracle, and PostgreSQL use native replication.

MySQL/MariaDB writable.

## Databases

### Oracle

Up to 5 read replicas.

Only EE license.

### poatgres

Up to 5 read replicas.

### mariadb

Can restore from MYSQL 5.6 snapshots.

Up to 5 read replicas. Can chain read replicas 4 deep.

### Aurora

Can autoscale read replicas.

#### Cloning

Copy-on-write minimizes disk usage.

Up to 15 clones based on a copy (including nested clones).

#### PostgreSQL

Can use logical replication e.g. individual tables.

#### MySQL

V1 = MYSQL 5.6.

Can invoke lambdas via `lambda_sync/async`.

Load text or xml from S3.

Save data into S3.

Master to Master available (max 2 masters). Aurora V.1 only.

Backtracking limited to 72 hours.



