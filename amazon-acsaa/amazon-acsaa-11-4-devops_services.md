AWS Certified Solutions Architect: Associate - 11.0 Additional Key Services
============================================================

#### File Name: amazon-acsaa-11-4-devops_services
#### Title: DevOps Services
#### Subtitle: AWS Certified Solutions Architect: Associate

11.4 DevOps Services
------------------------------------------------------------

#### DevOps

* AWS OpsWorks
	+ Configuration management service
	+ Built around open-source Chef solution
	+ Most applications require multiple services
		- ELB
		- App Servers
		- Database Servers
	+ OpsWorks combines them into a *stack* (Diagram)
	+ *Layers* are defined to manage scaling and other tasks
	+ Example uses
		- Multi-tier web applications
		- Continuous Integration
* AWS CloudFormation
	+ Version control system for AWS resources
	+ Uses *templates* and *stacks* to manage solutions (Diagram)
	+ *templates* are JSON text files that define the resources
	+ The resources combine to form a *stack*
	+ *parameters* can be used to modify the stack for testing (Diagram)
	+ Uses
		- Launch test environments
		- Replicate between environments
		- Deploy in new AWS regions
* AWS Elastic Beanstalk
	+ Dead-simple platform for deploying web applications
	+ Components
		- *application*: Logical collection of components
		- *application version*: Specific, labeled iteration of an application
		- *environment*: The application
		- *environment configuration*: Parameters that define how the application behaves
	+ Supported platforms
		- Java
		- Node.js
		- PHP
		- Python
		- Ruby
		- Go
		- Containers
			+ Tomcat
			+ Passenger
			+ Puma
			+ Docker
* AWS Trusted Advisor (Diagram)
	+ Reports on your account based on best-practices
		- Cost optimization
		- Security
		- Fault tolerance
		- Performance improvement
	+ Four checks provided at no cost
		- Service Limits
		- Security Groups - Specific Ports Unrestricted
		- IAM Use
		- MFA on Root Account
	+ Business or Enterprise support plan adds over 50 other checks
* AWS Config
	+ Security and Governance solution
	+ Provides inventory, configuration history and change 
	  notifications for AWS resources
	+ Maintaines Configuration Items for every resource in a region
	+ Use case
		- Discovery
		- Change management
		- Continuous Audit and Compliance
		- Troubleshooting
		- Security and Incident Analysis
	+ Integrates with CloudTrail
	+ Configuration items are stored in S3
	+ History file is populated every 6 hours by default