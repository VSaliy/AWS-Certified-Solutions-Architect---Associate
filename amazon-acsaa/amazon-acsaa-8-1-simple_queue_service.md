AWS Certified Solutions Architect: Associate - 8.0 SQS, SWF, and SNS
============================================================

filename: amazon-acsaa-8-1-simple_queue_service
Title: Amazon Simple Queue Service
Subtitle: AWS Certified Solutions Architect: Associate

8.1 Amazon Simple Queue Service
------------------------------------------------------------

* Basics
	+ Messaging buffer used to decouple cloud services
	+ Acts as a broker between services
	+ A single queue can be shared with multiple components
	+ Messages are guaranteed to be delivered at least once
		- Can be delivered multiple times
		- Apps should be designed to handle multiple messages
	+ Delivery is guaranteed, although order is not
* Message Lifecycle (Diagram)
* Visibility Timeout (Diagram)
	+ Hides a message after a certain period of time passes
	+ Timeout starts as soon as the message is initially read
	+ Prevents multiple read processes from duplicating workload
	+ Can hold up to 120,000 messages for up to 12 hours
* Delay Queues
	+ Hides a message immediately
	+ Allow holding messages for later processing
	+ 0-900 seconds (15 minutes)
* Identifies
	+ Each queue is assigned a name (identifier) when created
		- Must be unique among your queues
	+ Each message is assign an ID
		- A *receipt handle* is issued when reading a message
		- The *receipt handle* is used to delete the message from the queue
* Messages
	+ Contain two components
		1. Message Body
			- The contents of the message
		2. Message attributes
			- Metadata that describes the message body
			- Up to 10 attributes
* Advanced Features
	+ Long Polling
		- Used in place of frequent repetitious polling to save CPU
		- Can stretch a single poll into a 20 second window
	+ Dead Letter Queues
		- Used to store messages that were not successful processed
		- Useful for troubleshooting and alerting
	+ IAM Access Control