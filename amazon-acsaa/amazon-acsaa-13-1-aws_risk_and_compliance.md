AWS Certified Solutions Architect: Associate - 13.0 AWS Risk and Compliance
============================================================

#### File Name: amazon-acsaa-13-1-aws_risk_and_compliance
#### Title: AWS Risk and Compliance
#### Subtitle: AWS Certified Solutions Architect: Associate

13.1 AWS Risk and Compliance
------------------------------------------------------------

* [Compliance in AWS](https://aws.amazon.com/compliance/)
	+ [Resources](https://aws.amazon.com/compliance/resources/)
	+ Shared Responsibility (Diagram)
	+ AWS Controls may need to be suplemented
		- Web Application Firewall
		- Intrusion Detection/Prevention System
		- Encryption
	+ Governance
		- Entirely the customer's responsibility
		- Recommendation:
			1. Take a holistic approach
			2. Design controls to meet compliance requirements
			3. Identify and document 3rd party controls
			4. Verify all control objectives are met
* Evaluating and Integrating AWS Controls
	+ AWS Provides IT control information 2 ways:
	+ Specific Control Definition
		- AWS publishes a Service Organization Controls 1 (SOC 1) Type II report
		- SOC1 is an in-depth audit of control design and operating effectiveness
		- Type 2 tests for adequacy of design (type 1) and operating effectivness (type 2)
		- Testing performed by an external auditor
	+ General Control Standard Compliance
		- ISO 27001
		- Payment Card Industry (PCI) Data Security Standard (DSS)
		- Federal Information Security Management Act (FISMA)
	+ [AWS Reports](https://aws.amazon.com/compliance/soc-faqs/)
* [AWS Risk and Compliance Program](https://d0.awsstatic.com/whitepapers/compliance/AWS_Risk_and_Compliance_Overview.pdf)
	+ Three core areas
	+ Risk Management
		- Internal and external risk assessments are performed
		- Primarily based on COBIT
			+ Control Objectives for Information and Related Technology
		- Public facing IPs are regularly scanned
			+ Does not include customer endpoints
		- Customers must request permission to run their own scans
	+ Control Environment
		- AWS has a framework for planning, executing, and controlling business operations
		- Part of their onboarding process for new employees
	+ Information Security
		- Internal security program to provide confidentiality, integrity and availability
		- Publishes [security whitepapers](https://d0.awsstatic.com/whitepapers/Security/AWS_Security_Whitepaper.pdf)
			+ Recommended reading prior to exam
* [AWS Reports, Certifications and Third-Party Attestations](https://d0.awsstatic.com/whitepapers/compliance/AWS_Certifications_Programs_Reports_Third-Party_Attestations.pdf)