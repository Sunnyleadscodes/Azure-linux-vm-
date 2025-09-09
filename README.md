# Azure Red Hat Linux VM Lab

## 📖 Overview
This project demonstrates how to create and configure a Red Hat Enterprise Linux (RHEL) Virtual Machine on Microsoft Azure.  
The lab covers:
- Creating a Resource Group and Virtual Machine
- Connecting to the VM over SSH
- Running a system-wide package update to ensure the machine is secure and up to date

## 🛠 Steps Taken

### 1. Created Resource Group
- **Name:** 11160027d2716-creating -your first-azure-linux-virt
- **Region:** East US 

### 2. Configured Virtual Network
- Used a **preconfigured VNet** as provided by the lab.
- Confirmed a default subnet was available for the VM.

### 3. Deployed Red Hat Linux VM
- **Name:** `rhel-lab-vm`
- **Size:** B1s (small, cost-effective VM)
- **Image:** Red Hat Enterprise Linux 8.x
- **Authentication:** SSH Key (auto-generated in the lab)

### 4. Connected to VM via SSH
- Used the VM’s **public IP address** to connect:

```bash
ssh azureuser@<public-ip-address>

Once inside the VM, I updated all installed software to the latest versions using:
sudo dnf update -y
