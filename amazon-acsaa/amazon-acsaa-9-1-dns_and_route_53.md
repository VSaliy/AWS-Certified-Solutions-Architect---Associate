AWS Certified Solutions Architect: Associate - 9.0 DNS and Amazon Route 53
============================================================

#### File Name: amazon-acsaa-9-1-dns_and_route_53
#### Title: DNS and Route 53
#### Subtitle: AWS Certified Solutions Architect: Associate

9.1 DNS and Route 53
------------------------------------------------------------

* Basics (Diagram)
	+ Top-Level Domains (TLDs)
	+ Top-Level Domain Registrars
	+ Domain Names
	+ IP Addresses
	+ Hosts
	+ Subdomains
	+ Fully Qualified Domain Name (FQDN)
	+ Name Servers
	+ Zone Files
* DNS Resolution
	1. Check the host file
	2. Check the DNS cache
	3. Contact DNS Server
		- Root Hint Servers
		- TLD Servers
		- Domain-Level Name Servers
* Record Types
	+ Start of Authority (SOA)
	+ A and AAAA
	+ Canonical Name (CNAME)
	+ Mail Exchange (MX)
	+ Name Server (NS)
	+ Pointer (PTR)
	+ Sender Policy Framework (SPF)
	+ Text (TXT)
	+ Service (SRV)
* Route 53
	+ Domain Registration
	+ Hosted Zones
	+ Routing Policies
		- Simple
		- Weighted
		- Latency Based
		- Failover
		- Geolocation
	+ Health Checking
* Building Resiliency with Route 53
	+ Use an ELB in every region
	+ Use cross-zone load balancing with connection draining
	+ Use auto scaling
	+ Use health checks in the ELB and in Route 53
	+ Point application domain names to the ELBs using CNAMEs
	+ Create a failover domain pointing to a static page
	+ Assign the failover domain as a *secondary target* for the application alias
	+ Use Amazon CloudFront for serving application content