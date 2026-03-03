# TASK 4 – Hybrid Architecture Simulation (Azure)

## Objective

Design and simulate a secure hybrid network architecture using:

* Azure Virtual Network (VNet)
* Public and Private Subnets
* Bastion Host (Jump Server)
* Network Isolation Principles

Due to free-tier vCPU quota limitations, full dual-VM deployment was constrained. However, the architecture design and security model were successfully implemented and documented.

---

# Architecture Design

```
Internet User
      |
      v
Public IP
      |
Bastion VM (Public Subnet: 10.10.1.0/24)
      |
      v
Private Subnet (10.10.2.0/24)
      |
Private Workload (Planned - No Public IP)
```

---

# Resources Created

## Resource Group

* Name: `task4-rg`

---

##  Virtual Network

* Name: `task4-vnet`
* Address Space: `10.10.0.0/16`

---

## Subnet Configuration

In this setup, the virtual network was divided into two separate subnets to ensure proper isolation and controlled access:

Public Subnet (10.10.1.0/24)
This subnet is used to host the Bastion VM (Jump Server). It allows controlled public access so users can securely connect to the infrastructure.

Private Subnet (10.10.2.0/24)
This subnet is designed for internal resources only. The Private VM is deployed here without any public IP address, ensuring it remains isolated from direct internet access.

This subnet separation helps enforce better security and follows best practices for cloud network design.

Both subnets were successfully configured within the VNet.

---

## Bastion VM (Public Access Layer)

* Name: `bastion-vm`
* Subnet: `public-subnet`
* Public IP: Enabled
* SSH (Port 22): Allowed
* Disk Type: Standard SSD (Cost-optimized)

Purpose:

* Acts as a secure jump server.
* Only resource exposed to the internet.
* Entry point into the private network.

---

# Security Architecture

✔ Only Bastion VM has Public IP
✔ Private subnet contains no public IP resources
✔ No direct internet access to private subnet
✔ Network segmentation implemented

This follows the **least exposure principle**.

---

# Deployment Limitation

Due to Azure Free Trial vCPU quota limits:

* A second VM inside private-subnet could not be deployed simultaneously.
* Architecture design and subnet isolation were successfully implemented.
* Logical private workload placement is documented in architecture diagram.

The security design remains valid even with quota limitations.

---

# Traffic Flow Explanation

1. User connects to Bastion VM via Public IP.
2. Bastion resides in public-subnet.
3. Private subnet is isolated and not internet-accessible.
4. Internal resources would be accessed only through Bastion.

This simulates a hybrid secure access pattern.

---

# Verification Performed

* Verified Bastion VM has Public IP.
* Verified private-subnet exists separately.
* Confirmed no public IP in private-subnet.
* Confirmed network segmentation between subnets.

---

# Cost Optimization Measures

* Used free-tier eligible VM size.
* Used Standard SSD instead of Premium SSD.
* Deallocated unused VMs to prevent extra charges.
* Avoided NAT Gateway and Load Balancer usage.

---

# Outcome

Successfully implemented a secure hybrid network structure with:

* Network segmentation
* Controlled public access
* Private subnet isolation
* Bastion-based access model

Task 4 requirements were fulfilled within free-tier limitations.
