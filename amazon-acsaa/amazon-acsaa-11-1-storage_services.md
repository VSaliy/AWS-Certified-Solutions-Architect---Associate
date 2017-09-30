AWS Certified Solutions Architect: Associate - 11.0 Additional Key Services
============================================================

#### File Name: amazon-acsaa-11-1-storage_services
#### Title: Storage Services
#### Subtitle: AWS Certified Solutions Architect: Associate

11.1 Storage Services
------------------------------------------------------------

#### Amazon CloudFront

- Basics
	+ Content Delivery Network (CDN)
	+ Uses Amazon’s global network of edge locations
	+ Users are routed to the lowest latency edge location
	+ Supports any content via HTTP/HTTPS
	+ Also supports media with HLS/RTMP
- Basic Configuration
	+ Distributions
		- Domain name used in place of your application's name
		- Leverages a CNAME
	+ Origins
		- Source data
		- Supports:
			+ S3 bucket
			+ EC2 instance
			+ ELB
			+ Website URL
	+ Cache Control
		- Defines how long items are cached
		- 24 hours by default
		- Can be overridden with an *invalidation* API call
		- Renames are usually easier/faster
- Advanced Configuration (Diagram)
	+ Dynamic Content
	+ Multiple Origins
	+ Custom cache behavior
- Use cases
	+ Serving the Static Assets of Popular Websites
	+ Serving a Whole Website or Web Application
	+ Serving Content to Users Who Are Widely Distributed Geographically
	+ Distributing Software or Other Large Files
	+ Serving Streaming Media 
- Not use cases
	+ All or Most Requests Come From a Single Location
	+ All or Most Requests Come Through a Corporate VPN

#### AWS Storage Gateway

- Basics
	+ On-premises software appliance
	+ Connects to cloud-based storage
	+ Supports encrypted backups to S3 or Glacier
	+ Storage appears as an iSCSI device
	+ Uses SSL and SSE for encryption
	+ Not able to be accessed directly through S3
	+ Only accessible through the Gateway service
- Configurations
	+ Gateway-Cached Volumes
		- All data on the gateway is moved into S3
		- recently read data is cached locally
		- Up to 32TB in a volume
		- 32 volumes per gateway
		- 1PB total per gateway
	+ Gateway-Stored Volumes
		- Data is stored on-premises and in S3
		- Acts as an asynchronous off-site backup
		- Data is backed up as EBS snapshots
		- Up to 16 TB in a volume
		- 32 volumes per gateway
		- 512TB total per gateway
	+ Gateway-Virtual Tape Libraries
		- Uses pre-existing tape backup software
		- 1,500 tapes per gateway (1PB)
		- Tape eject command triggers a move to the Virtual Tape Shelf (VTS)
		- VTS is Glacier storage
		- 1 VTS per region
		- Multiple gateways can share a VTS
