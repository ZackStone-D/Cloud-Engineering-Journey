AWS SAA Cloud Foundations-Project

Create VPC
What is it - Virtual Private Cloud. When created it serves as a logical boundary where compute, storage, databases live. Every resource in AWS lives inside of a VPC

Create Subnet 
    Serves as a section or slice of the available IP addresses in a VPC. Allows for resources to be organized in sections. Subnets can be spread across multiple availability zones to keep resources running when one subnet fails.

Create Route Table 
    Route tables establish traffic flow between resources. A public subnet's route table has an entry of IGW 0.0.0.0/0 and private subnets have no IGW route established.

Create IGW
    The internet gateway is attached to the VPC and sits at the edge b/w the VPC and the public internet. It enables two way traffic in and out. A subnet becomes public when its route table has 0.0.0.0/0 entry targeting the IGW. An IGW isn't always necessary private and internal-only apps don't need and IGW

Create EC2 
    The elastic cloud compute instance is assigned to a subnet. The subnet's route table determines whether the EC2 instance has access to the internet or is private. The EC2 instance is where operating systems, workloads, and applications run.