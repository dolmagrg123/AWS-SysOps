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
