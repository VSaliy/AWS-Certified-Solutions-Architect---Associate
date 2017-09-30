AWS Certified Solutions Architect: Associate - 8.0 SQS, SWF, and SNS
============================================================

#### File Name: amazon-acsaa-8-3-simple_notification_service
#### Title: Amazon Simple Notification Service
#### Subtitle: AWS Certified Solutions Architect: Associate

8.3 Amazon Simple Notification Service
------------------------------------------------------------

* Basics
	+ Allows you to send notifications
	+ Publish-Subscribe messaging paradigm
	+ Can use push or client poll
	+ Supports SMS, Mobile and Email among others
* Components (Diagram)
	+ Publishers
	+ Subscribers
	+ Topics
		- Defined in SNS
		- Name must be unique within your SNS topics
		- Subscribers attach to a topic
		- Publishers announce to the same topic
* Scenarios
	+ Monitoring applications
	+ Time-sensitive updates
	+ Relaying events between workflows
	+ Moving data between stores
	+ Updating records in business systems
* Advanced Features
	+ Fanout
		- One message is sent to multiple queues
		- (Diagram)
		- Scenarios
			+ Dev/Prod
			+ Accounting/Shipping
			+ Prod/DR
	+ AWS System Alerts
		- Changes to an Auto Scaling group
	+ Push email and text messaging
	+ Mobile push notifications
		- Performed through an app
		- e.g. Announcing a new version