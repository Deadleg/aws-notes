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

## Volumes

More than 40 can cause boot failures.

Windows: 26 (red had 17)

## AMI

Launch permissions:

- public
- explicit
- implicit
