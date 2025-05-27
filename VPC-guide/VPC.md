# VPC [Virtual Private Cloud]  

- A VPC is a virtual network that you create in the cloud.  
- It's like having your own network within a larger network.  
- Within this VPC, you can create and manage various resources, such as servers, databases, and storage.  
- This virtual network is completely isolated from other user's networks, so your data and applications are secure and protected.
- Just like a physical network, a VPC has its own set of rules and configurations.
- You can define the IP address range for your VPC.
- To connect your VPC to the internet, you can set up gateways or routers.
- This act as an entry and exit points for traffic going in and out of your VPC.
---
![VPC](/VPC.png)

---
## Common Components in VPC  

### Subnet  
```
A subnet, or subnetwork, is a logical division of an IP network, that improves efficiency, security, and management.
Subnetting involves dividing a network using a subnet mask, which distinguishes the network portion from the host portion of an IP address. 
```
### Internet Gateway  
```
It enables communication between resources in a private network (like a Virtual Private Cloud or corporate network) and the public Internet.
It serves as the bridge between internal networks and external internet services.
```
### Load Balancers  
``` 
A load balancer is like a traffic cop for your web applications.
When many users try to access your website or service at the same time,
the load balancer distributes all these requests across multiple servers to prevent any single server from getting overwhelmed.  
They also handle security, scalability, observability, and resilience.
```
### NAT gateway (Network Address Translation)  
```
NAT gateways enables instances in a private subnet (with no public IP) to connect to the internet.
The NAT Gateway translates the private IP (of EC2) to its own public IP and forwards the traffic to the internet. 
```
### Route Table (AWS)  
```
Used for routing. It determines where network traffic from your subnet or gateway is directed.
```
### Security groups  
```
A security group acts as a virtual firewall for instances (EC2 instances or other resources) within a VPC.
It controls inbound and outbound traffic at the instance level.
Security groups allow you to define rules that permit or restrict traffic based on protocols, ports, and IP addresses.  
```
### Network ACL's (Access Control Lists)  
```
A Network Access Control List is a stateless firewall that controls inbound and outbound traffic at the subnet level.
It operates at the IP address level and can allow or deny traffic based on rules that you define.
Network ACLs provide an additional layer of network security for your VPC.
```
### EC2 Instances  
```
Amazon EC2 (Elastic Compute Cloud) is a core service offered by Amazon Web Services (AWS) that provides scalable,
on-demand virtual servers (instances) in the cloud.
```
### VPC flow logs  
```
VPC Flow Logs is a feature provided by Amazon Web Services (AWS) that captures information about the IP traffic going to and from network interfaces in a Virtual Private Cloud (VPC).
```
### Peering Connections
```
Use a VPC peering connection to route traffic between the resources in two VPCs.
```
### Traffic Mirroring 
```
Copy network traffic from network interfaces and send it to security and monitoring appliances for deep packet inspection.
```

[Also Refere](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-example-private-subnets-nat.html)
