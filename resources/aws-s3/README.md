# AWS S3
Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance.

The metrics for AWS S3 are obtained through AWS Cloudwatch by using the [YACE exporter](https://github.com/ivx/yet-another-cloudwatch-exporter).

## Cloudwatch billing considerations
Using AWS Cloudwatch for monitoring can incur additional costs in your AWS billing.
See the [AWS Cloudwatch documentation](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_limits.html) for further details.

# Metrics
## Daily storage metrics
AWS Cloudwatch provides free daily storage metrics for all the buckets.
- BucketSizeBytes
- NumberOfObjects

## Requests metrics
By default, these 1-minute metrics are available at the Amazon S3 bucket level. You can also define a filter for the metrics collected using a shared prefix or object tag.
- AllRequests
- GetRequests
- PutRequests
- DeleteRequests
- HeadRequests
- PostRequests
- SelectRequests
- SelectScannedBytes
- SelectReturnedBytes
- ListRequests
- BytesDownloaded: Average (bytes per request), Sum (bytes per period),
- BytesUploaded: Average (bytes per request), Sum (bytes per period),
- 4xxErrors: Average (reports per request), Sum (reports per period)
- 5xxErrors: Average (reports per request), Sum (reports per period)
- FirstByteLatency
- TotalRequestLatency

## Replication metrics
Only replication rules that have the S3 Replication Time Control (S3 RTC) enabled will publish replication metrics.
- ReplicationLatency
- BytesPendingReplication
- OperationsPendingReplication


For further information, see the [Cloudwatch documentation on S3 metrics](https://docs.aws.amazon.com/AmazonS3/latest/dev/cloudwatch-monitoring.html).

# Attributions
The configuration files and dashboards are maintained by [Sysdig team](https://sysdig.com/).

Using [Yace - yet another cloudwatch exporter](https://github.com/ivx/yet-another-cloudwatch-exporter) with Apache 2.0 license.