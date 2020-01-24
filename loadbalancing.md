# Loadbalancing

## ALB

Level 7 LB.

Rules evaulated in priority order.

Default routing is round robin.

Subnet requires at least a `/27` bitmask.

http2 enabled by default.

Targets over IPv4 regardless of client connection type.

### Actions

- authenticate-cognito
- authenticate-oidc
- fixed-response
- forward
- redirect

### Conditions

- host-header
- http-header
- http-request-method
- path-pattern
- query-string
- source-ip

### Target groups

Types:

- instances
- ip (internal ips)
- lambda

Algorithms:

- round_robin
- least_outstanding_requests

Can slow start new targets (ramp up requests in an up to 15 minute period).

5 minute (default) deregistration delay.

### Lambda targets

Max body size 1mb. Max response size 1mb.

## NLB

Level 4 load balancer.

Target select by flow hash algorithm.

TCP: Protocol, Source IP/port, Target IP/port, TCP seq number.
UDP: Protocol, Source IP/port, Target IP/port.

For public traffic can associate 1 public IP per subnet.

### Target groups

- instance
- internal ip

If routing by ip, the source IP is the load balancer IP. If routing by instance, then the source IP is the client IP.
