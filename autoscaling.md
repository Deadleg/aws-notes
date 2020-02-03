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

## Dynamic scaling

- Target tracking scaling
- Step scaling
- Simple scaling

If multiple policies trigger, the policy with the largest number of instances will be used (for both scale out and in).

### Target tracking policy

Recommended to scale at 1 minute intervals (requires detailed monitoring).

## Simple scaling

## Step scaling

Does not support cooldowns.

Scaling types:

- ChangeInCapacity
- ExactCapacity
- PercentageChangeInCapacity

Instance warmup: can specify (in seconds) number of seconds for and instance to start. While starting the aggregated metrics aren't counted nor is it counted towards it's current capacity.

## Cooldowns

Only for simple scaling. Default 300 seconds.

## Terminations

### Default

1. Find AZ with most instances and at least 1 non-protected instance.
2. Find instances aligning with allocation strategy (remove lowest priority instances).
3. Oldest launch configuration
4. Ties broken by instances to the closest billing hour

### Customised

- OldestInstance
- NewestInstance
- OldestLaunchConfiguration
- ClosestToNextInstanceHour
- Default
- OldestLaucnTemplate
- Allocation strategy


## Lifecycle hooks

Default wait timeout is 1 hour, up to 38 hours or 100 times heartbeat timeout.
