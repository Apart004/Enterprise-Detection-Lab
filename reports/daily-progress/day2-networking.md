# Day 2 - Ubuntu Server Deployment and Networking

## Objective

Deploy Ubuntu Server and configure enterprise network connectivity.

---

## Tasks Completed

### 1. Ubuntu Server ISO Management

Downloaded:

* Ubuntu Server 24.04.4 LTS

Validated ISO integrity using SHA256 hashing.

---

### 2. Ubuntu Server Installation

Installed Ubuntu Server onto:

* Wazuh-SIEM-Server

Installation Configuration:

* Ubuntu Server edition
* LVM storage layout
* OpenSSH Server enabled
* BIOS firmware mode

---

### 3. Static IP Configuration

Configured static infrastructure addressing:

| Parameter  | Value            |
| ---------- | ---------------- |
| Hostname   | wazuh-siem       |
| IP Address | 192.168.10.10    |
| Gateway    | 192.168.10.1     |
| DNS        | 1.1.1.1, 8.8.8.8 |

---

### 4. SSH Service Deployment

Installed and enabled:

* OpenSSH Server

Validated using:

```bash
systemctl status ssh
```

---

### 5. Connectivity Validation

Tested:

* IP configuration
* Internet connectivity
* DNS resolution
* SSH service availability

Commands used:

```bash
ip a
ping -c 4 8.8.8.8
ping -c 4 google.com
```

---

## Skills Learned

* Ubuntu Server deployment
* Linux networking
* Static IP configuration
* SSH administration
* Network diagnostics

---

## Current Infrastructure State

* Ubuntu Server operational
* Static IP configured
* SSH enabled
* Internet access validated
