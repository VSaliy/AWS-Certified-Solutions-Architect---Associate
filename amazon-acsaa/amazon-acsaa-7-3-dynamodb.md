AWS Certified Solutions Architect: Associate - 7.0 Databases and AWS
============================================================

filename: amazon-acsaa-7-3-dynamodb
Title: Amazon DynamoDB
Subtitle: AWS Certified Solutions Architect: Associate

7.3 Amazon DynamoDB
------------------------------------------------------------

* Basics
	+ Fully managed NoSQL database
	+ You define a read/write capacity and upload your data
		- Capacity is assigned per-table
		- 1 capacity unit = 4KB of read or 1KB of write
	+ DynamoDB automatically provisions enough infrastructure to provide that capacity
	+ Automatically configures high-availability (Multi-AZ)
* NoSQL (Diagram)
	+ Data is stored differently than relational databases
	+ Each record must have a primary key
	+ All other values (attributes) are optional
		- Schema is not predefined
	+ Data types
		- Enforced by the application, not by DynamoDB
		- Only the primary key has to have a strictly defined data type
	+ Two types of Primary Keys
		- Partition Key
			+ Consists of one attribute
				- The key itself (sometimes called a hash key)
			+ DynamoDB builds an unordered hash index on this attribute
		- Partition and Sort Key
			+ Consists of two attributes
				- The key itself (sometimes called a hash key)
				- The sort key (sometime called a range key)
	+ Secondary Indexes
		- Global Secondary Index
			+ Provides an alternative partition and sort key
			+ Can be created at any time
		- Local Secondary Index
			+ Same partition key but a different sort key
			+ Can only be created at table creation
* Two Modes of Data Consistency
	+ Types
		- Eventually Consistent Reads
		- Strongly Consistent Reads
	+ Type is specified during the read request
* Scaling and Partitioning (Diagram)
	+ Partition key is used to distribute data
	+ New partitions can be added as the database scales
	+ Partition Limits
		- Around 10GB of data
		- 3,000 read capacity units
		- 1,000 write capacity units
	+ Some room for bursts, but not reliably
	+ Partitions can be split, but not merged
* DynamoDB
	+ Fully integrated with IAM
	+ IAM policy can restrict access to a table
	+ Conditions can restrict access to items/attributes
* DynamoDB Streams
	+ Provide a list of all changes in the last 24 hours
	+ Allows applications to act on new data
	+ Can be enabled/disabled