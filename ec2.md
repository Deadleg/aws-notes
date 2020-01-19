# EC2

## Hibernate

Not charged when stopped. EBS is still charged (with RAM contents).

### Prerequisites

- C, M, R families only.
- Memory less than 150GB.
- Amazon linux or ubuntu.
- Root volume must be encrypted.

### Limitations

- Can't change instance type
- Can't create snapshots
- Can't be hibernernated 60+ days.

## Networking

### Multiple ip addresses

Security groups to network interface.

### ENI

Primary IPv4.
One EIP per private IPv4.
One public IPv4.
Many IPv6.

Can move within the same VPC and AZ.

## Volumes

More than 40 can cause boot failures.

Windows: 26 (red hat 17)

## AMI

Launch permissions:

- public
- explicit
- implicit

## Placement groups

- Cluster: Group of instances in the same AZ.
- Partition: Groups of instances across AZs (think Elasticsearch index partitions).
- Spead placement group: Distinct racks.

Cannot merge placement groups.

Instance can only belong on one placement group.

`host` tenancy cannot be placed in placement group.

### Cluster

Can span peered VPC.

10Gbps flow limit for all connections to all machines. 100 Gbps aggregate.

Internet traffic and direct connect are limited to 5 Gbps.

### Partition

Each partition on its own rack.

Max 7 partitions per AZ.

Group with dedicated instances can only have 2 partitions.

Not support for dedicated hosts.

## Spread

Max 7 running instances.

Not supported for dedicated instances or hosts.
