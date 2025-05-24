# aws-guide
Fundamentals of Cloud and AWS. 

---

## EC2

Amazon **EC2 (Elastic Compute Cloud)** is a core service offered by **Amazon Web Services (AWS)** that provides scalable, on-demand **virtual servers (instances)** in the cloud. 

### **Variety of Instance Types**
EC2 offers different **instance families** optimized for various workloads:

| **Instance Type** | **Use Case** |
|------------------|------------|
| **General Purpose (e.g., t4g, m6i)** | Balanced compute, memory, and networking (web servers, small databases) |
| **Compute Optimized (e.g., c7g, c6i)** | High-performance computing (batch processing, gaming servers) |
| **Memory Optimized (e.g., r7g, x2iezn)** | Memory-intensive workloads (in-memory databases, big data analytics) |
| **Storage Optimized (e.g., i4i, d3en)** | High-speed storage (NoSQL databases, data warehousing) |
| **GPU/Accelerated (e.g., p4, g5)** | Machine learning, graphics rendering, parallel processing |

## **How Amazon EC2 Works**
1. **Launch an Instance**: Choose an **AMI (pre-configured template)**, instance type, and configure networking.
2. **Connect to the Instance**: Use **SSH (Linux)** or **RDP (Windows)**.
3. **Deploy Applications**: Install software, run web servers, databases, etc.
4. **Monitor & Scale**: Use **Amazon CloudWatch** for performance tracking and **Auto Scaling** for dynamic adjustments.
5. **Terminate When Not Needed**: Stop or terminate instances to save costs.

## **Advantages of Amazon EC2**
✅ **Cost-Effective**: Pay only for what you use.  
✅ **Highly Scalable**: Instantly adjust capacity.  
✅ **Secure**: Built-in encryption, VPC, IAM controls.  
✅ **Reliable**: 99.99% uptime SLA.  
✅ **Global Infrastructure**: Deploy in multiple AWS regions.  

---

