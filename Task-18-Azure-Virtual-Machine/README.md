# Task 18 – Azure Virtual Machine

## Objective
To launch and configure a basic Azure Virtual Machine and access it using SSH from Command Prompt.

## Services Used
- Azure Resource Group
- Azure Virtual Machine
- Azure Virtual Network
- Network Security Group
- Public IP Address

## Steps Performed
1. Logged in to Azure Portal.
2. Created a Resource Group named ppt-rg.
3. Created a Virtual Machine named ppt-vm.
4. Selected Image: Ubuntu Server 24.04 LTS.
5. Selected VM Size: Standard B2ats v2 (Free eligible).
6. Configured SSH authentication using key pair.
7. Clicked Review + Create and deployed the VM.
8. Verified VM status as Running.
9. Connected to the VM using SSH from Windows CMD.

## SSH Command Used
```bash
ssh -i ppt-vm_key.pem azureuser@4.154.32.230
