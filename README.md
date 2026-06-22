# Enterprise Detection Lab - Wazuh SIEM & Threat Intelligence Platform

## Overview

Enterprise Detection Lab is a hands-on Security Operations Center (SOC) and Threat Intelligence Platform built to simulate real-world enterprise security monitoring, threat detection, incident investigation, and threat intelligence integration.

The project combines endpoint monitoring, host-based intrusion detection, automated security responses, and external threat intelligence feeds to demonstrate how modern SOC environments detect and respond to security events.

---

## Objectives

* Build an enterprise-grade Security Operations Center (SOC) lab.
* Deploy and configure the Wazuh SIEM platform.
* Monitor Windows endpoints for security events.
* Implement host-based intrusion detection.
* Detect authentication anomalies and privilege escalation.
* Monitor critical file integrity changes.
* Configure automated security responses.
* Integrate external Threat Intelligence using AlienVault Open Threat Exchange (OTX).
* Build the foundation for automated IOC enrichment and threat correlation.

---

# Lab Architecture

```
                        +---------------------------+
                        | AlienVault OTX Platform   |
                        |  Threat Intelligence API  |
                        +------------+--------------+
                                     |
                                     |
                              REST API (HTTPS)
                                     |
                                     v
                         +------------------------+
                         | Threat Intel Scripts   |
                         | Python / Requests      |
                         +-----------+------------+
                                     |
                                     |
                                     v
+--------------------------------------------------------------+
|                      Ubuntu SOC Server                        |
|--------------------------------------------------------------|
| Wazuh Manager                                                 |
| Wazuh Indexer                                                 |
| Wazuh Dashboard                                               |
| Active Response                                               |
| File Integrity Monitoring                                     |
| Threat Intelligence Module                                    |
+--------------------------------------------------------------+
                     ^
                     |
             Wazuh Agent
                     |
                     |
+----------------------------------------------+
|          Windows Endpoint                    |
|----------------------------------------------|
| Windows Security Events                      |
| Authentication Logs                          |
| Privilege Escalation Events                  |
| File Integrity Events                        |
+----------------------------------------------+
```

---

# Technology Stack

## Operating Systems

* Ubuntu Server 24.04 LTS
* Windows 10 Enterprise

## Security Platform

* Wazuh Manager
* Wazuh Dashboard
* Wazuh Indexer
* Wazuh Agent

## Programming

* Python 3
* Bash

## Threat Intelligence

* AlienVault OTX API
* OTXv2 SDK
* Requests Library
* JSON Processing

## Virtualization

* Oracle VirtualBox

---

# Project Features

## SIEM Deployment

* Wazuh Manager deployment
* Wazuh Dashboard configuration
* Wazuh Indexer deployment
* Windows agent enrollment
* Agent health validation

---

## Endpoint Monitoring

* Windows Security Event monitoring
* Authentication monitoring
* User account monitoring
* Privilege escalation detection
* Administrative group modification detection

---

## File Integrity Monitoring

* Syscheck configuration
* Critical file monitoring
* File creation detection
* File modification detection

---

## Active Response

Configured Wazuh Active Response framework capable of automated defensive actions.

Current capabilities include:

* Host deny
* Firewall drop
* Account disable
* Wazuh service restart

---

## Threat Intelligence Platform

Implemented an external Threat Intelligence module using AlienVault Open Threat Exchange (OTX).

Current capabilities include:

* API authentication
* Threat pulse retrieval
* JSON parsing
* Threat metadata extraction
* IOC extraction

Extracted Indicator Types:

* MD5 Hashes
* SHA1 Hashes
* SHA256 Hashes
* Domains

Future roadmap includes:

* IOC normalization
* MongoDB storage
* IOC enrichment
* Threat correlation with Wazuh alerts
* Automated feed synchronization

---

# Detection Use Cases

## Authentication Monitoring

* Successful logons
* Failed logons
* Brute-force attempts

---

## User Account Monitoring

* User account creation
* User deletion
* Account modification

---

## Privilege Escalation

* Local administrator additions
* Group membership changes
* Privileged account monitoring

---

## File Integrity Monitoring

* Critical file creation
* File modification
* File deletion

---

## Threat Intelligence

* Live threat feed retrieval
* IOC extraction
* Threat indicator parsing

---

# Project Structure

```
Enterprise-Detection-Lab/

├── reports/
│   └── daily-progress/
│
├── threat-intel/
│   ├── config.py
│   ├── extract_iocs.py
│   ├── inspect_pulse.py
│   ├── list_iocs.py
│   ├── test_otx.py
│   ├── test_otx_api.py
│   └── venv/
│
├── screenshots/
│
├── docs/
│
└── README.md
```

---

# Skills Demonstrated

* Security Operations Center (SOC)
* SIEM Deployment
* Wazuh Administration
* Linux Administration
* Windows Security Monitoring
* Threat Detection Engineering
* Active Response Configuration
* File Integrity Monitoring
* Threat Intelligence Integration
* REST API Integration
* Python Automation
* JSON Parsing
* Security Event Analysis
* Threat Hunting Fundamentals

---

# Current Progress

## Completed

* Wazuh deployment
* Dashboard configuration
* Windows agent onboarding
* Authentication monitoring
* Privilege escalation detection
* File Integrity Monitoring
* Active Response configuration
* AlienVault OTX integration
* Threat pulse retrieval
* IOC extraction

## In Progress

* IOC normalization
* Threat intelligence enrichment
* IOC database storage
* Threat correlation engine

---

# Future Enhancements

* MongoDB integration
* Elasticsearch threat enrichment
* Automated IOC synchronization
* IOC reputation scoring
* Scheduled threat feed ingestion
* Threat correlation with Wazuh alerts
* Custom detection rules
* Security dashboards

---

# Learning Outcomes

This project provided practical experience in:

* Enterprise SIEM deployment
* Endpoint security monitoring
* Security event analysis
* Incident detection
* Threat intelligence integration
* Security automation
* Linux system administration
* Python security scripting
* API integration
* Threat hunting workflows

---

# Disclaimer

This project is intended for educational and research purposes only. All testing was performed within an isolated virtual lab environment.
