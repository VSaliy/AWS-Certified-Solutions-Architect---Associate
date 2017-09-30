AWS Certified Solutions Architect: Associate - 3.0 Amazon EC2 and EBS
============================================================

filename: amazon-acsaa-3-1-amazon_ec2_basics
Title: Amazon EC2 Basics
Subtitle: AWS Certified Solutions Architect: Associate

3.1 Amazon EC2 Basics
------------------------------------------------------------

* Introduction
	+ What is EC2? 
	+ Elastic Compute Cloud
* Instance Types
	+ Defines resources
		- vCPU
		- Memory
		- Storage
		- Network
	+ Types
		- m4: Balanced
		- c4: CPU Optimized
		- r3: Memory Optimized
		- i2: Storage Optimized
		- g2: GPU Optimized
* Amazon Machine Images (AMI)
	+ Deployable system image
		- OS and configuration
		- Initial state of patches
		- Applications and system software
	+ All are currently x86 Windows/Linux images
	+ Can be private, published from Amazon or published by 3rd parties
* Addressing an instance
	+ Public DNS name
	+ Public IP
	+ Elastic IP
* Initial access
	+ RDP/SSH
	+ Password/Key file
* Virtual Firewall
	+ EC2-Classic Security Group
	+ VPC Security Group
* Instance Lifecycle
	+ Bootstrapping
		- Passing a script to an OS at boot time
			+ Apply patches
			+ Join a directory
			+ Install software
			+ Copy files
			+ Installing Chef/Puppet/SC client
	+ VM Import/Export
		- Allows moving instances between and on-premises environment
	+ Instance metadata
* Instance tags
	+ Allow tracking instances
	+ Up to 10 per instance
	+ Very useful for reporting
		- Project
		- Environment
		- BillingCode
* Monitoring an instance
	+ Basic CloudWatch
* Modifying an instance
	+ Instance type
	+ Security groups
	+ Termination protection
* Pricing options
	+ Types
		- On-demand Instances
		- Reserved Instances
			+ All Upfront
			+ Partial Upfront
			+ No Upfront
		- Spot Instances
	+ Solutions can mix types
		- Reserved for minimum load
		- On-demand for peak load
* Tenancy
	+ Shared Tenancy
	+ Dedicated Instances
		- Dedicates hardware to a client
		- Instances can launch on any dedicated host
	+ Dedicated Host
		- Allows mapping instances to specific dedicated hosts
		- Useful for meeting licensing requirements
* Placement groups
	+ Common 10Gbps network connection within an AZ
	+ Allows placing instances together that can benefit from improved networking
	+ Example: Web front-end and database back-end
* Storage
	+ Instance Stores (Ephemeral Storage)
		- Attached to the physical host
		- Does not survive a shutdown or failover
			+ Does survive a reboot
		- Designed for temporary use
	+ Elastic Block Store (EBS Storage)
		- Persistent storage
		- Replicated within the AZ
		- Types
			+ Magnetic
			+ General Purpose SSD
			+ Provisioned IOPS
* Backup/Recovery (Snapshots)
	+ Point-in-time snapshots
	+ Stored in S3, although containers are not able to be managed
	+ Must be manipulated through EC2
	+ Stored in the same region as the instance
	+ Can be copied to other regions
	+ New volumes can be provisions from the snapshot
* Encryption
	+ Instances can be encrypted
	+ Used AWS KMS
	+ Uses AES-256
	+ Minimal impact on performance