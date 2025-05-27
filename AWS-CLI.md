### **AWS CLI**  
**AWS CLI (Command Line Interface)** is a tool that lets you control AWS services **using typed commands** instead of clicking buttons in the AWS Console. It's like giving text-based orders to AWS from your computer's terminal.  

### **Why Use AWS CLI?**  
✅ **Faster** – Automate tasks with scripts (no manual clicking).  
✅ **Powerful** – Access advanced features not always available in the Console.  
✅ **Great for DevOps** – Manage AWS in code (Infrastructure as Code).  

---

### **Example: Launching an EC2 Instance with AWS CLI**  
Let’s say you want to **start a cloud server (EC2) using just commands**.  

#### **Step 1: Download & Install AWS CLI**  
- Download from [aws.amazon.com/cli](https://aws.amazon.com/cli/) or install via:  
  ```bash
  pip install awscli
  ```
  
- Check the AWS CLI version:
  ```bash
  aws --version
  ```

#### **Authenticate with AWS User Account**
Follow these steps to authenticate:

1. Go to [AWS Console](https://console.aws.amazon.com/)
2. Click on your profile
3. Navigate to "Security credentials"
4. Scroll to "Access keys" section
5. Click on "Create access key" button
6. Mark the checkbox and click "Create Access key"

   #### ` IMP : Never share these access keys with anyone. `

7. Copy both the:
   - **Access key**
   - **Secret access key**
8. Save them in a secure location on your machine.


#### **Step 2: Configure AWS Credentials**  
- Go to **AWS CLI**, type command:
  
  ```bash
  aws configure
  ```
- This will ask you to enter your `AWS Access Key`, `Secret Key`, and default region like `us-east-1`, copy & paste it  
- This way your `AWS User` account is authenticated to `AWS` using `AWS CLI`

#### **Step 3: Launch an EC2 Instance**  
  ```bash
  aws ec2 run-instances \
    --image-id ami-0abcdef1234567890 \  # Amazon Linux AMI
    --instance-type t2.micro \          # Free-tier eligible
    --key-name MyKeyPair                # Your SSH key name
  ```

**Output:**  
  ```json
  {
    "InstanceId": "i-1234567890abcdef0"
  }
  ```

  **Your EC2 server is now running!**   

- This way you can now create and use different **AWS Services** like `S3`, `EBS`, etc using `AWS CLI Commands`  
  [AWS CLI Commands for different AWS Services](https://docs.aws.amazon.com/cli/latest/)

---

#### **Real-World Use Cases**  
1. **Automate Backups** – Script EBS snapshots nightly.  
2. **Deploy Apps** – Launch 100 servers with one command.  
3. **Check Costs** – Quickly list all S3 buckets and their sizes.  

---

#### **AWS CLI vs. AWS Console**  
| Feature          | **AWS CLI**                     | **AWS Console (GUI)**          |  
|------------------|---------------------------------|--------------------------------|  
| **Speed**        | Faster (for bulk tasks)         | Slower (manual clicks)         |  
| **Learning Curve** | Requires command knowledge    | Beginner-friendly              |  
| **Automation**   | Perfect for scripts/cron jobs   | Not automatable                |  

---

#### **Try These Basic AWS CLI Commands**  
1. **List S3 Buckets**  
   ```bash
   aws s3 ls
   ```
2. **Stop an EC2 Instance**  
   ```bash
   aws ec2 stop-instances --instance-ids i-1234567890abcdef0
   ```
3. **Download a File from S3**  
   ```bash
   aws s3 cp s3://my-bucket/file.txt ./local-folder/
   ```



