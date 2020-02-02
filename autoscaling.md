# Autoscaling

## Lifecylcle

Scale out -> pending -> (hook wait) -> (hook proceed) -> InService
Detach -> Detaching -> Detached
Scale in/fail health check -> Terminating -> (hook wait) -> (hook proceed) -> Teminated
EnterStandBy -> EnteringStandby -> StandBy

## Launch templates

Cannot assign multiple network interfaces.

Cannot choose a host of use host placement affinity.

## Auto Scaling Groups

### Multiple instances types

Spot instance strategies are

- capacity-optimized: get instances that have hightest capacity (lower chance of interruption).
- lowest-price: get instances with lowerst price (higher chance of interruption).

### Load balancing

Optionally health checks can use load balancer health check. Must pass health check from all load balancers otherwise it will be considered unhealthy.

### Weighting

Can over provision capacity. Distributions over AZs and spot allocation strategies are evaluated before avoiding overages.
