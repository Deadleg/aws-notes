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
