# Day 1 - Enterprise Lab Infrastructure Setup

## Objective

Establish the foundational infrastructure for the Enterprise Detection Lab.

---

## Tasks Completed

### 1. GitHub Repository Initialization

Created public repository:

* Enterprise-Detection-Lab

Configured:

* README.md
* MIT License
* Enterprise folder structure

---

### 2. VirtualBox Installation

Installed:

* Oracle VM VirtualBox 7.2.8
* VirtualBox Extension Pack

Validated installation using:

```powershell
VBoxManage --version
```

---

### 3. Enterprise NAT Network Deployment

Created isolated NAT network:

* Detection-Lab-Net
* Network Range: 192.168.10.0/24

Configuration:

* DHCP Enabled
* IPv6 Disabled
* NAT isolation enabled

Validated using:

```powershell
VBoxManage list natnetworks
```

---

### 4. Wazuh SIEM VM Provisioning

Created:

* Wazuh-SIEM-Server

Hardware Allocation:

* 4 vCPUs
* 6144 MB RAM
* 100 GB dynamically allocated VDI

Additional Configuration:

* Audio disabled
* USB 3.0 enabled
* NAT Network mapped to Detection-Lab-Net

---

## Skills Learned

* Virtualization basics
* Virtual network segmentation
* Enterprise VM provisioning
* NAT networking concepts
* Infrastructure organization

---

## Current Infrastructure State

* Hypervisor operational
* NAT network operational
* Ubuntu SIEM VM shell created
* GitHub project structure initialized
