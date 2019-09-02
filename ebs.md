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
