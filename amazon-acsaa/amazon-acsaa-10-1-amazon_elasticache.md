AWS Certified Solutions Architect: Associate - 10.0 Amazon ElastiCache
============================================================

#### File Name: amazon-acsaa-10-1-amazon_elasticache
#### Title: Amazon ElastiCache
#### Subtitle: AWS Certified Solutions Architect: Associate

10.1 Amazon ElastiCache
------------------------------------------------------------

* Basics
	+ In-Memory Caching (Diagram)
	+ 100ms = 1% decrease in sales
	+ Two popular solutions
		- Memcached
			+ In-memory key/value data store
			+ Typically stores the results from a DB query
			+ Stores data in blobs so it can store anything
		- Redis
			+ Provides all the features of Memcached
			+ Adds support for rich data types
				- Strings
				- Lists
				- Sets
			+ Data persists on disk
				- Allows surviving a failed master
				- Any replica can be promoted
	+ Challenging to configure for distributed systems
		- Both technologies use clusters for scalability
	+ ElastiCache simplifies that
		- Mostly automated
		- Compliant with Memcached and Redis
		- Clusters controlling the cache are fully managed
* Design
	+ More small nodes will provide better availability
	+ Memcached supports auto discovery, but requires client software
		- Client supports .NET, Java and PHP
	+ Scaling is built around EC2 instances (Horizontal/Vertical)
	+ Use Multi-AZ Replication (Diagram)
		- Replication is asynchronous so some delay is introduced
	+ Backups
		- Memcached is entirely in-memory so you cannot use snapshots
		- Redis persists on disk so you can use snapshots
	+ Control access with IAM