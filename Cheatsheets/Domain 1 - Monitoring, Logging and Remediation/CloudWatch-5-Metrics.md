# Metrics in Amazon CloudWatch

Metrics are the fundamental concept in Amazon CloudWatch. A metric represents a time-ordered set of data points that are published to CloudWatch. Think of a metric as a variable to monitor, and the data points as representing the values of that variable over time. You can use these metrics to verify that your system is performing as expected.

Metrics are data about the performance of your systems. By default, many services provide free metrics for resources (such as Amazon EC2 instances, Amazon EBS volumes, and Amazon RDS DB instances). You can also enable detailed monitoring for some resources, such as your Amazon EC2 instances, or publish your own application metrics. Amazon CloudWatch can load all the metrics in your account (both AWS resource metrics and application metrics that you provide) for search, graphing, and alarms.

-   Metric data is **kept for 15 months**, enabling you to view both up-to-the-minute data and historical data.
-   CloudWatch comes with many **predefined** metrics that are generally name spaced by AWS Service.

### AWS/EC2 Per-Instance Metrics

-   CPPUUtilization, DiskReadOps, DiskWriteOps, DiskReadBytes, DiskWriteBytes, MetadataNoToken, MetadataNoTokenRejected, NetworkIn, NetworkOut, NetworkPacketsIn, NetworkPacketsOut

### AWS/EC2 CPU credit metrics for Burstable Performance Instances

-   CPUCreditUsage, CPUCreditBalance, CPUSurplusCreditBalance, CPUSurplusCreditsCharged

### AWS/EC2 T3 Dedicated Hosts Metrics

-   DedicatedHostCPUUtilization

### AWS/EC2 Amazon EBS Metrics for Volumes attached to Nitro-based instances

-   EBSReadOps, EBSWriteOps, EBSReadBytes, EBSWriteBytes, EBSIOBalance%, EBSByteBalance%

### Status Check Metrics for EC2 Instances

Available at a 1-minute frequency at no charge. For a newly-launched instance, status check metric data is only available after the instance has completed the initialization state (within a few minutes of the instance entering the running state).

-   StatusCheckFailed, StatusCheckFailed_Instance, StatusCheckFailed_System, StatusCheckFailed_AttachedEBS

### AWS/EBS Status Check Metric

-   VolumeStalledIOCheck

### AWS/EC2 metrics for mirrored traffic

-   NetworkMirrorIn, NetworkMirrorOut, NetworkPacketsMirrorIn, NetworkPacketsMirrorOut, NetworkSkipMirrorIn, NetworkSkipMirrorOut, NetworkPacketsSkipMirrorIn, NetworkPacketsSkipMirrorOut

### AWS/AutoScaling metrics for Auto Scaling Groups

Amazon EC2 Auto Scaling metrics that collect information about Auto Scaling groups are in the AWS/AutoScaling namespace. Amazon EC2 instance metrics that collect CPU and other usage data from Auto Scaling instances are in the AWS/EC2 namespace.

### AWS/Usage metrics

-   ResourceCount

### AWS Provided Metrics (AWS Pushes them):

| Types of Monitoring  | Description |
| ------------- | ------------- |
| Basic Monitoring  | Metrics are collected at a 5 minute interval  |
| Detailed Monitoring  | Metrics are collected at a 1 minute interval  |

### Custom Metrics (Yours to push):

| Resolution Types  | Description |
| ------------- | ------------- |
| Basic Monitoring  | 1 minute resolution  |
| Detailed Monitoring  | all the way to 1 second resolution  |

### Resources / Videos
- https://www.youtube.com/watch?v=Yxl7e88cTAQ 