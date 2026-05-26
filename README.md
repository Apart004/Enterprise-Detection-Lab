# Enterprise Detection Lab

## Overview
Enterprise-style blue-team cybersecurity lab focused on:
- SIEM engineering
- Endpoint telemetry
- Threat detection
- Detection engineering
- Threat simulation
- SOC workflows

---

## Infrastructure Stack

| Component | Technology |
|---|---|
| Hypervisor | VirtualBox |
| SIEM | Wazuh |
| Endpoint | Windows 10 Enterprise |
| Attack Platform | Kali Linux |
| Telemetry | Sysmon |

---

## Planned Network

192.168.10.0/24

| Host | Role |
|---|---|
| 192.168.10.10 | Wazuh SIEM |
| 192.168.10.20 | Windows Endpoint |
| 192.168.10.30 | Kali Linux |

---

## Project Goals
- Build operational SOC environment
- Develop detection engineering skills
- Simulate enterprise attack scenarios
- Create portfolio-grade blue-team lab