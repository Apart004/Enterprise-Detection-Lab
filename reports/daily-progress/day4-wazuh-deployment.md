# Day 4 – Wazuh SIEM Deployment

## Objectives
- Validate VM resources
- Verify network connectivity
- Download Wazuh installer
- Begin Wazuh SIEM deployment

## Environment Verification

### Network
- Verified IP address using `ip a`
- IP Address: 192.168.10.10
- Verified internet connectivity using:
  - `ping -c 4 8.8.8.8`
  - `ping -c 4 google.com`

### System Resources
- Memory: ~6 GB RAM available
- Disk: 48 GB allocated
- Free Disk Space: ~39 GB

### Host Information
- Hostname: wazuh-siem
- OS: Ubuntu Server 24.04.4 LTS
- Platform: Oracle VirtualBox

## Wazuh Installation

### Installer Download
```bash
curl -sO https://packages.wazuh.com/4.12/wazuh-install.sh
```

### Permission Assignment
```bash
chmod +x wazuh-install.sh
```

### Installation Launch
```bash
sudo ./wazuh-install.sh -a
```

## Progress
- Wazuh repository added
- Certificates generated
- Indexer installation started
- Deployment in progress

## Skills Practiced
- Linux administration
- Network verification
- Resource validation
- Package deployment
- SIEM installation workflow

## Result
Wazuh deployment completed successfully.