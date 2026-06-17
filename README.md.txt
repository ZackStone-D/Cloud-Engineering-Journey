README.md

Foundational Cloud Elements 

Create VPC

Isolated network, a boundary/fence for a Region.

	Design Patterns 
	
	Depending on company security, size, and preferred structure. Multiple AWS accounts can be used to with their own VPC's
	. A small organization may choose to use one AWS account with multiple VPC's per environment(DEV, PRODUCTION, ACCOUNTING)
	
	VPC is region scoped the entire region has to fail for the assets to stop functioning.

Create a Subnet

	1. link to appropriate VPC 
	
	VPC has a large number of useable addresses the subnet creates a slice of these resources and is linked to an availability zone(AZ)
	
	Design Pattern
	
	Subnets can be spread across availability zones so that multiple resources do not fail at the same time.

Create Internet gateway 

	Depending on architecture an internet gateway will be created. It is not necessary for internal/private resources to have an IGW. 
	Resources needing internet access will need the subnet routed to the public /0 address.
	The IGW lives between the VPC and the public internet
	 
Create Route Table 
	
	Determines network traffic path using IP addresses, allows traffic flow between different subnets can create public, private and many other 	types of subnets. Route table determines the type of subnet

	Design pattern
	if something can't talk to something else it is probably the route table
	entry points to resources public /0 private defined by admin or appropriate personnel

Create EC2

	Amazon elastic cloud compute. The EC2 instance is assigned to a subnet. The subnet is assigned a list of useable IP addresses. An EC2 	instances the VPC infrastructure- IGW, subnet, route table, and security groups to control network connectivity.

	
	
	