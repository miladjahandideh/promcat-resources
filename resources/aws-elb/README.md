# AWS Elastic Load Balancer
Elastic Load Balancing automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, IP addresses, and Lambda functions.
It can handle the varying load of your application traffic in a single Availability Zone or across multiple Availability Zones.

The metrics for AWS ELB are obtained through AWS Cloudwatch by using the [YACE exporter](https://github.com/ivx/yet-another-cloudwatch-exporter).

## Cloudwatch billing considerations
Using AWS Cloudwatch for monitoring can incur additional costs in your AWS billing.
See the [AWS Cloudwatch documentation](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_limits.html) for further details.

# Metrics
- BackendConnectionErrors
- HealthyHostCount
- HTTPCode_Backend_2XX
- HTTPCode_Backend_3XX
- HTTPCode_Backend_4XX
- HTTPCode_Backend_5XX
- HTTPCode_ELB_4XX
- HTTPCode_ELB_5XX
- Latency
- RequestCount
- SpilloverCount
- SurgeQueueLength
- UnHealthyHostCount

For further information, see the [Cloudwatch documentation on ELB metrics](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html).

# Attributions
The configuration files and dashboards are maintained by [Sysdig team](https://sysdig.com/).

Using [Yace - yet another cloudwatch exporter](https://github.com/ivx/yet-another-cloudwatch-exporter) with Apache 2.0 license.