# Task 26 – Azure Virtual Machine & Networking Setup

## Objective

The objective of this task was to understand and implement the basic infrastructure setup in Microsoft Azure, including:

* Creating a Resource Group
* Deploying a Virtual Machine
* Configuring Virtual Network and Subnets
* Managing Public IP and Network Security Groups
* Understanding Availability Zones and VM sizes

This task focused on foundational Azure infrastructure concepts.

---

#  Infrastructure Created

##  Resource Group

* Created a dedicated Resource Group to logically organize all resources.
* This helped in managing and deleting resources easily after testing.

---

##  Virtual Machine Deployment

* Created a Linux Virtual Machine (Ubuntu).
* Selected free-tier eligible VM size where available.
* Configured authentication using SSH.
* Attached Network Security Group (NSG).

---

## Virtual Network (VNet)

* Created a custom Virtual Network.
* Defined address space.
* Configured subnet for VM deployment.

This allowed understanding of Azure networking structure.

---

##  Public IP Configuration

* Assigned a Public IP address to enable external SSH access.
* Configured inbound rule to allow SSH (Port 22).

---

##  Availability Zones & VM Size Testing

* Explored availability zone selection.
* Attempted deploying VMs in different zones.
* Tested different VM sizes to stay within free-tier limits.

---

# Limitations Faced (Free Trial Constraints)

During this task, several limitations were encountered due to Azure Free Trial restrictions:

###  1. VM Size Unavailability

Some free-tier VM sizes (like B1s) were not available in selected regions.

###  2. Regional vCPU Quota Limits

The subscription reached its regional vCPU quota limit, preventing deployment of additional VMs.

###  3. Availability Zone Restrictions

Certain regions did not support availability zones for free-tier sizes.

###  4. Region-Specific Resource Constraints

Some regions (e.g., EUAP regions) caused validation errors or limited configuration options.

---

# How These Issues Were Handled

* Switched regions where possible.
* Deallocated unused VMs to free up vCPU quota.
* Selected smallest available VM size.
* Used Standard SSD instead of Premium SSD to avoid extra cost.
* Deleted unused resources immediately after testing.

Despite these limitations, core learning objectives were achieved successfully.

---

#  Verification Performed

* VM successfully deployed.
* SSH access confirmed.
* Public IP connectivity tested.
* Resource group structure verified.
* Networking configuration validated.

---

#  Cost Management

* Used Free Trial subscription.
* Avoided Premium disk and unnecessary services.
* Deallocated and deleted resources after testing.
* Ensured no NAT Gateway or Load Balancer was created.


---

#  Conclusion

This task provided hands-on experience with Azure infrastructure deployment and networking configuration. Although some limitations were encountered due to free trial regional quotas and VM size availability, the core objectives were successfully completed.

The task strengthened understanding of Azure compute, networking, and cost management best practices.

---

