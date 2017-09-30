AWS Certified Solutions Architect: Associate - 2.0 Amazon S3 and Glacier Storage
============================================================

filename: amazon-acsaa-2-3-amazon_glacier
Title: Amazon Glacier
Subtitle: AWS Certified Solutions Architect: Associate

2.3 Amazon Glacier
------------------------------------------------------------

* Introduction
	+ High latency, high durability storage
	+ Useful for tape backup replacement
	+ Useful for compliance requirements
* Archives
	+ Primary storage unit of Glacier
	+ 1 archive can contain up to 40TB of data
	+ Unlimited # of archives
	+ Each has a unique ID (no friendly name)
	+ Encrypted by default
	+ Immutable (cannot be changed)
* Vaults
	+ Containers of archives
	+ Each AWS account can have up to 1000 vaults
* Vault Locks
	+ Policies that enforce compliance
	+ For example Write-One-Read-Many (WORM)
	+ Policies cannot be changed once "locked"
* Data Retrieval
	+ Retrieval of up to 5% of data per month is free
	+ After that there is a charge
* Glacier vs S3
	+ Glacier can be used as a storage class within S3
	+ Serves as the end of the lifecycle for data