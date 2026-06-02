# Day 7 – Network Recovery and Wazuh Dashboard Restoration

## Objective

Restore access to the Wazuh dashboard after the environment became unreachable following a VM restart.

## Work Completed

### 1. Service Verification

Verified that all major Wazuh services were running correctly:

* Wazuh Manager
* Wazuh Indexer
* Wazuh Dashboard

Used systemd status checks to confirm service health and identify that the issue was not related to Wazuh components.

### 2. Network Troubleshooting

Investigated connectivity between the Windows host and Ubuntu Wazuh server.

Findings:

* Dashboard service was listening on TCP port 443.
* Windows host could not reach the server.
* NAT interface (`enp0s3`) retained IP address `192.168.10.10`.
* Host-only interface (`enp0s8`) was present but lacked an IPv4 address.

### 3. Host-Only Network Recovery

Performed network diagnostics and discovered that the Host-Only adapter was not receiving an address through DHCP.

Actions:

* Enabled interface `enp0s8`.
* Verified VirtualBox Adapter 2 configuration.
* Manually assigned IP address:

```bash
sudo ip addr add 192.168.56.10/24 dev enp0s8
```

### 4. Connectivity Validation

Confirmed:

* Host-only network connectivity restored.
* Windows host successfully reached `192.168.56.10`.
* HTTPS dashboard became accessible again.

### 5. Dashboard Access Restored

Successfully logged into the Wazuh web interface and verified:

* Wazuh services operational.
* Windows endpoint visible in the platform.
* Vulnerability Detection module functional.
* Existing vulnerability findings displayed for installed software.

## Key Learning Outcomes

* Difference between NAT and Host-Only networking in VirtualBox.
* How Wazuh dashboard availability depends on network configuration, not only service status.
* Basic Linux network troubleshooting using `ip a`, `ip link`, and service verification commands.
* Importance of persistent network configuration for lab environments.

## Result

Wazuh dashboard access successfully restored at:

https://192.168.56.10

The security monitoring environment is operational and ready for further endpoint monitoring and threat detection activities.
