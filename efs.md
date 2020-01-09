# EFS

## Connectivity

Requires EC2 instance to use AWS DNS while mounting.

Need to define mount targets per VPC to connect to, with NFS port (2049) open on the security group.

### Direct connect/VPN

Recommend to connect via IP.

## Data consistency

close-to-open consistency (NFS)

## Storage classes

IA has higher first byte latency

### Lifecycle management

Can transition files to IA. Min file size 128 KB.

Types are:

- `AFTER_7_DAYS`
- `AFTER_14_DAYS`
- `AFTER_30_DAYS`
- `AFTER_60_DAYS`
- `AFTER_90_DAYS`

File metadata is stored in standard storage.

## File metering

2 KiB inode, plus many 4 KiB data blocks.

Directories are metered by the storage of the directory entries and the data structure that holds them rounded to up to the next 4 KiB.

Symlinks/special files are always 4KiB.

## Performance modes

- General Performance Mode
- Max I/O

## Throughput

All file systems can burst to 100MiB/s. Over 1 TiB can burst 100MiB/s per TiB.

Gain credits 50MiB/s/TiB (50KiB/s/GiB). Minimum disk size 1GiB.

Need to wait 24 hours before decreasing provisioned throughput or changing throughput mode.
