# Task 7: Create EFS and Connect to Multiple Ubuntu Instances

## Objective
To configure Amazon Elastic File System (EFS) and mount it to EC2 instances to demonstrate shared and scalable storage.

---

## Services Used
- Amazon EC2
- Amazon EFS
- Security Groups
- NFS (Network File System)

---

## Steps Performed

1. Created a Security Group allowing:
   - SSH (Port 22)
   - NFS (Port 2049)

2. Launched Ubuntu EC2 instance in default VPC with public IP enabled.

3. Created Amazon EFS (Regional) in the same VPC.

4. Attached the same Security Group to EFS mount targets.

5. Connected to EC2 using SSH.

6. Installed NFS client:
   ```bash
   sudo apt update
   sudo apt install nfs-common -y
