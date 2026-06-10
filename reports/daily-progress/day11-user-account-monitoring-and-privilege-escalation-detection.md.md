# Day 11 - User Account Monitoring and Privilege Escalation Detection

## Objective

Validate Wazuh's ability to detect account creation, account modification, failed authentication attempts, and privilege escalation activities on a monitored Windows endpoint.

## Activities Performed

### User Account Creation

A new local user account named `socuser` was created using PowerShell.

```powershell
net user socuser Password123! /add