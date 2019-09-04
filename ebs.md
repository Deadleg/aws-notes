# Throughput

| |gp2|io1|st1|sc1|
|-|-|-|-|-|
|size|1G - 16T|4G - 16T|500G-16T|500G-16T|
|iops/mb/s|up to 16,000|up to 64,000|up to 500M/s|up to 250M/s|
|max throughput|250M/s|1000M/s|500M/s|250M/s|

SSD IO size = 16 KiB
HDD IO size = 1 MiB

gp2 max through put if size > 334 GiB, other burst > 170 GiB

io1 max iops only on nitro instances, 32,000 otherwise.

A1, C5, C5d, C5n, I3en, M5, M5a, M5ad, M5d, p3dn.24xlarge, R5, R5a, R5ad, R5d, T3, T3a, and z1d
Bare metal: c5.metal, c5n.metal, i3.metal, i3en.metal, m5.metal, m5d.metal, r5.metal, r5d.metal, u-6tb1.metal, u-9tb1.metal, u-12tb1.metal, and z1d.metal

# GP2

Min 100 IOPS, 3 IOP/GB. Max burst 3000.

`T = VIR`

# io1

Throughput gaurantee 99.9%

IOPS:GB = 50:1

IO size up to 32,000 IOPS = 256. 16 above.

# st1

40M/T baseline.

Burst 250M/T.

# sc1

12M/T baseline.

Burst 80M/T.

# snapshots

Full performance after each block accessed once.

Can encrypt on fly from unencrypted volume.

# Market place volumes

Can only attach to stopped instances.

Applied code to the instance.

Remove volume from instance disassociates code with instance.

# Monitoring

If AWS detects the volume is `impaired` it will suspend IO operations. Can override with `autoEnableIO`.

# Copying

5 concurrent copy requests per region.

Tags are not copied.

# Modifications

Can take around 24 hours for modifications to take affect.

IO changes in a few minutes to few hours.
