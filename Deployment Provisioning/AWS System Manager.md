# System Manager (SSM) 

* SSM is a management tool which gives you visibility and control over your AWS infrastructure

* Integrates with CloudWatch allowing you view your dashboards, view operational data and detect problems

* Includes Run Command which automates operational tasks across resources- eg. security patching, package installs

* Organize your inventory, grouping resources together by application or environment- including in-premises systems

### Using System manager in EC2
* First create a IAM role with EC2RoleforSSM policy attached
* Launch EC2 instance, and attach IAM role just created
* Make note of last 4 letters of instanceID


##  Resource Groups
* Find Resources
* Save Resource Groups

## Insights
1. Built in Insights: 

Config, CloudTrail, Personal Health Dashboard, Trusted Advisor

#### Trusted Advisor:

Cost Optimization, Performance, Security, Fault Tolerance, Service Limits

2. Dashboard by CloudWatch
3. Inventory
4. Compliance

## Actions
1. Automation
2. Run Command

####  Run Command

* Allows you to run pre-defined commands on one or more EC2 instances
* Stop, restart, terminate, re-size instance
* Attach/detach EBS volumes
* Create snapshots, backup DynamoDB tables
* Aplly patches and updates
* Run an Ansible playbook
* Run a shell script









