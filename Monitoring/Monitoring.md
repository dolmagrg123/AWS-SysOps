### Cloud Watch

* Monitor resources and applications that run on AWS(monitor performance)

##### Host Level metrics consists of:
1. CPU utilization
2. Network
3. Disk
4. Status Checks

Note **

* Ram Utilization is a custom metric
* For Custom Metric: min granularity=1 minute(Turn on detailed monitoring)
* Standard monitoring set in EC2 will give 5 minute intervals

#### Terminated Instances
You can retrieve data from any terminated EC2 or ELB instance after its termination. CloudWatch Logs by default are stored indefinitely.

#### Metric Granularity

* 1 minute for detailed monitoring
* 5 minutes for standard monitoring

###### Cloudwatch can also be used on premise
Not Restricted to just AWS resources. Can be on premise too. Just need to download and install the SSM agent and CloudWatch agent.

#### EBS Different Volume Types

5 Different Types of EBS Storage:
* General Purpise(SSD)
* Provisioned IOPS(SSD)
* Throughput Optimised Hard Disk Drive
* Cold Hard Disk Drive
* Magnetic
 ###### Key IOPS Metrics:
 You can burst up to 3000 IOPS. If you need more than 3000 but less than 10,000 just increase the volume size. Anything over 10,000 IOPS move to PIOPS.(Provisioned IOPS)

#### CloudTrail

CloudTrail monitors API calls in the AWS platform.

#### ELB- Monitoring Types
4 Different Ways to monitor your load balancers

1. CloudWatch metrics
2. Access logs: Trace errors using **Access Logs** stored in S3 for EC2 instances that are already deleted.
3. Request Tracing
4. CloudTrail logs

#### Elasticache consists of two engines
1. Memcached
2. Redis

(Use:Example: Finding the top ten producs used)

Monitoring Elasticache

* CPU Utilization
* Swap Usage
* Evictions
* Concurrent Connections

#### CloudWatch Dashboard

Dashboards are multi-region and can display any widget to any region. To add the widget,change to the region that you need and then add the widget to the dashboard. Always save dashboards.

#### Billing Alarms

You can create Billing Alarms to automatically alert you for when you go above a pre-defined cost that you set.

#### AWS Organizations

* Centrally Manage Poilicies Across Multiple AWS Accounts
* Control Access to AWS services
* Automate AWS Account Creation And Management
* Consolidate Billing Across Multiple AWS Accounts

#### AWS Resource Groups

* TAG Everything
* Two Types of Resource Groups
* Classical(Across the World)
* Systems Manager Resource Groups(Within a region)

#### AWS Config Rules

* **Complaince checks:**

* Trigger
  * Periodic
  * Configuration Changes
* Manged Rules
  * About 40 (at time of recording)
  * Basic, but fundamental

* **Permission needed for config**

* AWS Config requires an IAM Role with
  * Read only permission to the recorded resources
  * Write access to S3 logging bucket
  * Publish access to SNS

* **Restrict Access**

* Users need to be authenticated with AWS and have the appropriate permission set via IAM policies to gain access.
* Only Admins needing to set up and manage Config requires full access
* Provide read only permission for Config day-to-day use.

#### Monitoring Config:

* Use CloudTrail with Config to provide deeper insight into resources.
* Use Cloud Trail to monitor access to Config, such as someone stopping the Config Recorder.

### CloudWatch Vs CloudTrail Vs Config

* CloudWatch monitors performance
* CloudTrail monitors API calls in the AWS platform
* AWS Config records the state of your AWS environment and can notify you of changes

### Health Dashboards
* Service Health Dashboard: Entire AWS environment on a continental basis
* Personal Health Dashboard: Provides alerts and remediation guidance when AWS is experiencing events that may impact you.



































