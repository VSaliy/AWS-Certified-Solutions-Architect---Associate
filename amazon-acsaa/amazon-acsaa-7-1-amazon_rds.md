AWS Certified Solutions Architect: Associate - 7.0 Databases and AWS
============================================================

filename: amazon-acsaa-7-1-amazon_rds
Title: Amazon Relational Database Service
Subtitle: AWS Certified Solutions Architect: Associate

7.1 Amazon Relational Database Service
------------------------------------------------------------

* Relational Databases
	+ Most common type of DB in use today
	+ Use the *Structured Query Language* (SQL)
	+ (Example Diagram)
	+ Primary Key
		- Allows a record (row) in one table to be *related* to rows in another table
	+ OLTP vs OLAP
	+ AWS supports 6 different RDB engines
	+ Unsupported DB engines can be run within an EC2 instance
	+ (Diagram about responsibilities)
* Data Warehouses
	+ Primarily OLAP
	+ Batch write operations performed infrequently
	+ RDS can perform both OLAP and OLTP roles
		- However, usually OLTP
		- Redshift provides high-performance DW for OLAP
	+ RDS and Redshift can be combined for ultimate effect
* NoSQL Databases
	+ Overcomes limitations of RDS especially when it comes to scaling
		- RDS have issues with write access
		- Typically one master and one or more slaves
		- Slaves are read-only
		- (Diagram)
* Amazon RDS
	+ Database Instances
		- Allows for quick, managed, DB deployment
		- Replication is easy to configure
		- Does not provide shell access
		- Supports standard tools for the chosen engine
		- Can be created/maintained via the API
		- Instance Class
			+ Similar to an EC2 instance class
			+ Determines the CPU/RAM of the server
	+ Database Engines
		- MySQL
		- Oracle
		- PostgreSQL
		- Microsoft SQL Server
		- MariaDB
		- Amazon Aurora
	+ Licensing
		- License Included model
		- Bring Your Own License (BYOL)
	+ Storage Options
		- Magnetic
		- General Purpose SSD
		- Provisioned IOPS SSD
	+ Backup and Recovery
		- Recovery Time Objective (RTO)
			+ Typically hours or days
		- Recovery Point Objective (RPO)
			+ Typically minutes
		- Two systems
			+ Automated backups
				- Performed daily during a backup window
				- One day retained by default
				- Can be increased to 35 days maximum
				- Storage volume snapshot
			+ Manual Snapshots
				- Performed as needed
				- Retained until you delete them
	+ Multi-AZ Deployments
		- (Diagram)
		- Designed for disaster recovery, not performance
			+ Redshift or read-replicas should be used for performance
		- RDS configures and maintains the cluster
		- Complexity is reduced significantly
		- DB is assigned a DNS endpoint that can be flipped
		  from primary to slave
		- Auto-failover situations
			+ Failed AZ
			+ Compute unit failure on the primary database
			+ Storage failure on the primary database
	+ Scaling Up and Out
		- Scaling up is supported for all engines
		- Scaling out (horizontally) is only supported for some engines
		- Partitioning or sharding
			+ Amazon implements this in DynamoDB and Cassandra
		- Read Replicas
			+ Another method of scaling out
			+ Improves OLAP, but not OLTP
			+ Supported DB engines
				- MySQL
				- PostgreSQL
				- MariaDB
				- Amazon Aurora
	+ Security
		- Identity and Access Management (IAM)
		- Virtual Private Cloud (VPC)
		- Security Groups / Network ACLs
		- SSL / TLS / VPN
		- Database encryption