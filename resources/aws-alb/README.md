# AWS Application Load Balancer
Elastic Load Balancing automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, IP addresses, and Lambda functions.
An Application Load Balancer functions at the application layer, the seventh layer of the Open Systems Interconnection (OSI) model.

The metrics for AWS ALB are obtained through AWS Cloudwatch by using the [YACE exporter](https://github.com/ivx/yet-another-cloudwatch-exporter).

## Cloudwatch billing considerations
Using AWS Cloudwatch for monitoring can incur additional costs in your AWS billing.
Check the [AWS Cloudwatch documentation](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_limits.html) for further details.

# Metrics
## Load balancer metrics
- ActiveConnectionCount
- ClientTLSNegotiationErrorCount
- ConsumedLCUs
- DroppedInvalidHeaderRequestCount
- ForwardedInvalidHeaderRequestCount
- HTTP_Fixed_Response_Count
- HTTP_Redirect_Count
- HTTP_Redirect_Url_Limit_Exceeded_Count
- HTTPCode_ELB_3XX_Count
- HTTPCode_ELB_4XX_Count
- HTTPCode_ELB_5XX_Count
- HTTPCode_ELB_500_Count
- HTTPCode_ELB_502_Count
- HTTPCode_ELB_503_Count
- HTTPCode_ELB_504_Count
- IPv6ProcessedBytes
- IPv6RequestCount
- NewConnectionCount
- ProcessedBytes
- RejectedConnectionCount
- RequestCount
- RuleEvaluations

## Target metrics
- HealthyHostCount
- HTTPCode_Target_2XX_Count
- HTTPCode_Target_3XX_Count
- HTTPCode_Target_4XX_Count
- HTTPCode_Target_5XX_Count
- NonStickyRequestCount
- RequestCountPerTarget
- TargetConnectionErrorCount
- TargetResponseTime
- TargetTLSNegotiationErrorCount
- UnHealthyHostCount

## Metrics for Lambda functions that are registered as targets
- LambdaInternalError
- LambdaTargetProcessedBytes
- LambdaUserError

## User authentication metrics
- ELBAuthError
- ELBAuthFailure
- ELBAuthLatency
- ELBAuthRefreshTokenSuccess
- ELBAuthSuccess
- ELBAuthUserClaimsSizeExceeded

For further information, see the [Cloudwatch documentation on ALB metrics](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html).

# Attributions
The configuration files and dashboards maintained by [Sysdig team](https://sysdig.com/).

Using [Yace - yet another cloudwatch exporter](https://github.com/ivx/yet-another-cloudwatch-exporter) with Apache 2.0 license.