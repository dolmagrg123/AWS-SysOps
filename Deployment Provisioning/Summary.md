## EC2 Launch Issues

Two common reasons for an instance failing to launch:

* **InstanceLimitExceeded error** (You have exceeded the default limit for number of instances you can launch in the Region.)


* **InsufficientInstanceCapacity error** (AWS does not currently have enough available On-Demand capacity to service your request.)

## EBS Volumes and IOPS 

* IOPS(Input/Output Operations per second) used to benchmark performance for SSD volumes.
* IOPS is dependent on the size of your volume.

#### Two approaches for dealing with hitting the IOPS limit for your volume:

* Increase the volume size -(only works if your GP2 volume is <3333GB.)
* Change to Provisioned IOPS if your GP2 volume is 3333GB or greater or you need more than 10k IOPS.

## Bastion Hosts(JUMPBOX)

* A Bastion is a host connected to a Public subnet.
* You can connect to it over the internet.
* Used to securely connect to instances in a Private subnet.
* Allows you to safely administer your EC2 instances without exposing them to the internet
* For incoming SSH/RDP only.
* Does not enable outgoing requests - e.g. internet access for our instances.


## 3 Types of Load Balancers

* Application Load Balancers : http/https
* Network Load Balancers : TCP, High performance and low latency
* Classic Load Balancers : Both application and network but low level for application

* Pre-Warm Your Elastic Load Balancer if you expect a sudden and significant increase in traffic to your application.
* Static IP addresses can be provided by a Network Load Balancer, 1 per subnet
* You can place your ALB nehind a NLB to get the benefit of both

## ELB Error Messages

* 4XX - Client side errors -- Problem with the client request, identify the problem, fix the request and retry
* 5XX - Server side errors -- Identify and fix the problem with you webserver / application/ database / load balancer



