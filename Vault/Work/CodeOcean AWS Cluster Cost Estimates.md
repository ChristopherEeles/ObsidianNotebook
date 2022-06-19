# CodeOcean AWS Cluster Cost Estimates

**Assumptions**:
- Six users
- One month of service
- Bill is representative of the use case

## Cloud Services

**NOTE:  All costs in USD!**

- **CloudWatch**: monitoring and observability service
	- Billed for requests and for storage logs
	- $55.00 per month; $10 per user per month

- **Data Transfer**
	- Appear to be no costs associated with data transfer
	- Very small bandwidth fee ($0.16)

- **Elastic Compute Cloud (EC2):** Actual virtual machines which run code on the cluster
	- Elastic Compute NAT Gateway: allow private subnet to connect to external services, but external services cannot initiate connection
		- Two gateways were used for the entire month (720 hrs) for $36.0 per gateway
		- This is likely a fixed cost and won't scale with users; worst case would be one gateway per three users per month ($36.00 per 3 users per month)
	- Linux VMs: These make up a surprisinly small portion of the bill, suggesting that not much actual compute was done
		- ~850 hrs across 3 VM types; 141 hrs per user per month
		- $237.99, works out to $39.67 per user per month; round up to $50 per user per month
		- This will likely be the most variable cost, since it is entirely dependent on usage
	- Elastic Block Store (EBS): high performance block storage, probably used attached to VMs to persist data between VM allocations
		- Majority of this cost is per GB per month for storage; this cost will likely scale proportional to the number of users as well as over time, as data from previous analyses accumualtes
		- Currently about 100 GB per user per month: $62.09 / 6 = 10.34 per user per month; round to $12 per user per month

- **Elastic File System**: Similar to EBS, but has a true heirarchical file system, instead of being flat files
	- Not sure what this would be used for, maybe storing configuration files for the cluster
	- Could also be for VM storage, but seems weird to mix and match EBS and EFS
	- $35 per month; $6 per user per month

- **Elastic Load Balancer:** load balancer distrubutes network traffic between multiple instances of an application service
	- Probably used within the cluster to scale out services with increased users
	- $17.14 per month, round to $25 per month and use as fixed cost

- **ElastiCache:** in memory caching
	- Probably used for the chat features in CodeOcean, maybe for caching recent database queries
	- $13.11 per month; round to $3 per user per month

- **OpenSearch Service:** For analzying cluster logs
	- $30.00 per month; $5.00 per user per month; probably doesn't scale linearly with users

- **Relational Database Service:** PostgreSQL database, likely used for storing user login credentials and other cluster related sensitive data
	- $35 per month, unlikely to scale unless there are lots of users (like 100s)

- **Route 53:** DNS service for routing end users to IP addresses; allows users to access the cluster without using an IP address
	- $1 per month, unlikely to scale

- **Secrets Manager:** Store secrets for the cluster, probably to authenticate admins
	- $0.80 per month, unlikely to scale

- **Simple Notification Service:** Send emails to cluster admins
	- No cost

- **Simple Storage Service:** (S3) Storage bucket
	- Probably for cluster logs and configuration; maybe data back-ups for VM storage
	- $1.25 per user per month

### Approximate Cost Formula

### Scaling Costs
CloudWatch $10 per user per month
Virtual Machies $50 per user per month
Elastic Block Storage $12 per user per month, likely growing per user cost over time
Elastic File System $6 per user per month
ElastiCache $3 per user per month
OpenSearch Service $5 per user per month
Simple Storage Service (S3) $1.25 per user per month

**Total***: 87.25 + tax per user per month = $96.33 per user per month; round to $100 per user per month

**CAD Total:** $130 per user per month (assuming 1 USD = 1.3 CAD)

### Relatively Fixed Costs
Elastic Compute NAT Gateway $72 per month
Elastic Load Balancer $25 per month
Relational Database Service $35 per month
Route 53 $1 per month
Secrets Manager $1 per month

**Total:*** $135 per month + tax = 151.42 per month; round to $160 per month

**CAD Total:** $208 CAD per month (assuming 1 USD = 1.3 CAD)