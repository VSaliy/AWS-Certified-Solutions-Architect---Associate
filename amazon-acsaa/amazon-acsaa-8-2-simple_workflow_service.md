AWS Certified Solutions Architect: Associate - 8.0 SQS, SWF, and SNS
============================================================

filename: amazon-acsaa-8-2-simple_workflow_service
Title: Amazon Simple Workflow Service
Subtitle: AWS Certified Solutions Architect: Associate

8.2 Amazon Simple Workflow Service
------------------------------------------------------------

* Basics
	+ Divides a workload into tasks
	+ Each task represents a distinct phase in a process
	+ Custom applications handle decision logic
	+ Workflow has high durability as each decision returns to the workflow (Diagram)
	+ An application can crash and resume where it left off. 
* Workflows
	+ Can process synchronously, asynchronously or both
	+ Workflow Domains
		- Define partitions within the workflow environment
		- Workflows in different domains cannot communicate with each other
	+ Workflow History
		- Complete detailed record of all events in the workflow
* Actors (3 types)
	+ Workflow Starters
		- Any application that can initiate a workflow
	+ Workflow Deciders
		- The logic that coordinates the task
		- Schedules tasks
		- Provides input to the tasks
		- Handles any events that occur while the workflow is executing
	+ Activity Workers
		- A single process (thread) that performs the work
* Tasks (3 types)
	+ Activity Tasks
		- Tells an activity worker to perform its function
		- Contains all the necessary data
	+ AWS Lambda Tasks
		- Executes a Lambda function instead of calling an activity worker
	+ Decision Tasks
		- Determines the next step in the workflow
* Advanced Functions
	+ Task Lists 
		- Allow you to view and influence the organization of tasks
	+ Long Polling
		- Used by default by activity workers and deciders
	+ Workflow Execution Closure
		1. Completed
		2. Canceled
		3. Failed
		4. Timed Out
		5. New Execution
		6. Terminated
	