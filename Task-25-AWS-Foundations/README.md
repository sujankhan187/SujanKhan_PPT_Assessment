# TASK 1 – Basic Cloud Setup (AWS)

## Objective

To create and configure basic AWS cloud resources including compute and storage services, and verify public access.

---

## Services Used

* Amazon EC2
* Amazon S3
* IAM
* Security Groups
* Public IP

---

##  Implementation Steps

### Step 1: Launch EC2 Instance

* Selected Amazon Linux / Ubuntu AMI
* Instance Type: t2.micro (Free tier eligible)
* Created new Key Pair
* Enabled SSH (Port 22) in Security Group
* Assigned Public IP

### Step 2: Connect to EC2

Used SSH command:

```bash
ssh -i key.pem ec2-user@<Public-IP>
```

Verified successful login.

---

### Step 3: Install Web Server

Installed Apache:

```bash
sudo yum install httpd -y
sudo systemctl start httpd
```

Created sample index.html file.

---

### Step 4: Verify Public Access

* Copied EC2 Public IP
* Opened in browser
* Confirmed website loading successfully

---

### Step 5: S3 Bucket Creation

* Created S3 bucket
* Uploaded sample file
* Verified object accessibility

---

## Architecture Diagram

User
↓
Internet
↓
EC2 Instance (Public Subnet)
↓
S3 Bucket (Storage)

---

## Screenshots Included

* EC2 Instance running state
* Security Group inbound rules
* SSH connection proof
* Web page via Public IP
* S3 bucket and uploaded object

---

## Output Verification

* EC2 running successfully
* Website accessible via Public IP
* S3 object uploaded successfully

---

## Cost Optimization

* Used Free Tier eligible instance
* Terminated EC2 after testing
* Deleted S3 bucket after verification

--
