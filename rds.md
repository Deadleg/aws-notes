# snapshots

## Sharing

Sharing unencrypted snapshot with another account allows other account to restore directly from that snapshot. Cannot share mssql/oracle with TDE

## Storage

Up to 64TiB of storage except SQLServer up to 16TiB. Min 20GiB

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
