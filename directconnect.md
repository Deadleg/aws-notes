# Direct Connect

## Resiliency toolkit

### Max resilieny

Use two seperate direct connect locations and multiple devices per location.

### High reliency

Use two seperate direct connect locations.

### Development and test

One location, multiple devices.

### Classic

Existing connections

## Connections

- Dedicated connection: 1 physical connection to 1 customer. Requested via AWS through the console or API.
- Hosted connection: Physical connection managed by AWS Direct Connect Partner.

## Virtual interfaces

Choose one of 

- Private virtual interface: Access VPC via private IP addresses.
- Public virtual interface: Access public AWS services using public IP addresses.
- Transit virtual interface: Connected to one or more VPC transit gateways.'

## LAG

All connections must use the same bandwitch.

Maximum 4 connections per LAG.

Connections must terminate as same Direct Connet endpoint.

## Direct Connect Gateway

Cannot create public virtual interface.

