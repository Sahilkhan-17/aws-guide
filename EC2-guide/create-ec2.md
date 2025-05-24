# Create virtual machines / servers (EC2) on AWS  

There are different ways to create or use AWS services:  

### 1. Using AWS Console (GUI) [Manual]  
### 2. Using Infrastructure as Code (IaC):  
- **AWS CLI** (practical way)  
- **AWS CDK** (Cloud Development Kit)  
- **AWS CFT** (Cloud Formation Template, writing `.yaml` file)  
- **Terraform**  
### 3. Using Script Automation:  
- **AWS API**  
- **Shell Script**  
- **Python** (using `Boto3` module)  

---

## To create EC2 instances on AWS using AWS Console (GUI) (Manual Process)  

### Steps:  
1. **Login** to [AWS Console](https://aws.amazon.com/console/).  
2. **Search** for the service **EC2** in the AWS Console.  
3. Go to the **Instances** tab.  
4. Click on **Launch Instances**.  
5. Fill up the details & while filling details, click on **Create new key pair**.  
   - **Key pair name** = `Test` (or any name of your choice)  
   - **Key pair type** = `RSA`  
   - **Private key file format** = `.pem`  
   - Click on **Create key pair** button.  
     *(This will download & save a `.pem` file to your local machine, which is required for logging into the EC2 instance later.)*  
6. In **Network Settings**, check if **Auto-assign public IP** is enabled (if not, enable it).  
7. Under **Inbound security group rules**, verify:  
   - **Type** = `SSH`  
   - **Source type** = `Anywhere`  
8. *(leave other settings as default as of now.)*  
9. Click on **Launch instance**.  

✅ Your **EC2 instance (VM/server)** is now created and running on AWS.  

---

## Log in to the EC2 Instance using Terminal  
You can connect to the EC2 instance using:  
- **AWS Web UI (EC2 Instance Connect)**  
- **Terminal (SSH)**  

- **Terminal Options:**  
  - **Mac:** iTerm  
  - **Windows:** MobaXterm, Putty, NoMachine  

### Steps:  
1. **Set Permissions for the `.pem` File** (downloaded while creating Instance on aws):  
   ```bash
   chmod 600 /Users/user_name/Downloads/Test.pem  # Change path to your .pem file
   ```

2. **Connect via SSH with Key Pair:**  
   ```bash
   ssh -i /Users/user_name/Downloads/Test.pem ubuntu@Public_IP_Address  # Replace with your EC2 instance's IP
   ```
   - **`-i`** flag specifies the identity (key) file.  
   - Replace:  
     - **`/Users/sahil/Downloads/Test.pem`** → Your `.pem` file path.  
     - **`Public_IP_Address`** → Your EC2 instance’s **public IP**.  

 - It will ask to confirm the fingerprint—type **`yes`**. 

✅ **You’re now connected to your EC2 instance!**  

### Important Notes:  
- Always use the **Public IP address** (not private).  
- For **Windows (Putty)**, convert `.pem` to `.ppk` before use.  

