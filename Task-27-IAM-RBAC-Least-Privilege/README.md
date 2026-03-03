# Task 27 – IAM, RBAC & Least Privilege (AWS + Azure)

## Objective

The objective of this task was to implement secure access control using:

* AWS IAM (Identity and Access Management)
* Azure RBAC (Role-Based Access Control)
* Custom policies
* Least privilege principle

This task demonstrates how cloud security is enforced by granting users only the minimum permissions required to perform specific actions.

---

#  AWS Implementation

## Overview

In AWS, IAM is used to manage:

* Users
* Groups
* Roles
* Policies

The goal was to create restricted access instead of giving full administrative permissions.

---

## Steps Performed

### Created IAM User

* Created a new IAM user for limited access testing.
* Disabled unnecessary permissions.

###  Created Custom Policy

* Defined a JSON policy to allow only specific actions.
* Example:

  * Allow S3 read access
  * Restrict EC2 or admin access

Policy was written using the least privilege model.

###  Attached Policy to User

* Attached custom policy to the IAM user.
* Verified that only allowed actions could be performed.

###  Tested Access

* Logged in using IAM user credentials.
* Confirmed:

  * Allowed actions worked.
  * Restricted actions were denied.

---

##  AWS Verification

--> IAM user created successfully
--> Custom policy attached
--> Unauthorized services blocked
--> Least privilege principle applied

---

# Azure Implementation

## Overview

In Azure, access control is managed using:

* Azure Active Directory (Entra ID)
* Role-Based Access Control (RBAC)
* Built-in and custom roles

---

## Steps Performed

### Created New User (Azure AD)

* Added a new user in Azure Active Directory.

### Assigned RBAC Role

* Assigned limited role such as:

  * Reader
  * Contributor (resource-level only)

Access was granted only at resource group level (not subscription level).

### Tested Role Permissions

* Logged in as the new user.
* Verified:

  * Only permitted actions were allowed.
  * Resource modification restrictions worked correctly.

---

## Azure Verification

--> User created successfully
--> RBAC role assigned at correct scope
--> Access restricted properly
--> No full admin privileges given

---

# Security Principles Applied

* Least Privilege Access
* Role-Based Access Control
* Separation of Duties
* Controlled Resource Scope
* No Over-permissioning

---

# Cost Impact

This task involved only identity and access configuration.
No billable compute or storage resources were created.
No additional cost incurred.

---

# Submission Deliverables

* IAM User screenshots
* Custom Policy JSON file
* Policy attachment proof
* Azure User creation screenshot
* RBAC role assignment screenshot
* Access testing proof

---

# Conclusion

This task successfully demonstrated secure identity and access management in both AWS and Azure environments. By applying the least privilege principle, access was controlled effectively while maintaining operational functionality.

Proper IAM and RBAC configuration is a critical foundation for building secure cloud architectures.

---

