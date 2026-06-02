For your internship repository:

# Day 7 Progress Report – Persistent Network Configuration & Connectivity Troubleshooting

## Objective

Resolve the issue where the Wazuh dashboard became unreachable after restarting the virtual machine and ensure network settings persist across reboots.

## Work Completed

* Investigated dashboard connectivity failure after system reboot.
* Verified status of Wazuh Manager, Wazuh Indexer, and Wazuh Dashboard services.
* Identified that the Host-Only network interface (`enp0s8`) was not retaining its IP configuration.
* Configured a persistent static IP address using Netplan.
* Added Host-Only Adapter configuration:

  * `enp0s8 → 192.168.56.10/24`
* Validated the configuration using:

  * `netplan generate`
  * `netplan apply`
  * `ip a`
* Rebooted the Wazuh server VM to verify persistence.
* Confirmed that the Host-Only IP address remained assigned after reboot.
* Successfully restored reliable access to the Wazuh web dashboard.

## Challenges Faced

* Wazuh services were running, but the dashboard remained inaccessible.
* Initial troubleshooting focused on service status before identifying the networking issue.
* Encountered YAML indentation errors while editing the Netplan configuration file and corrected them.

## Outcome

The Wazuh SIEM server now maintains a persistent Host-Only IP address across reboots, ensuring stable communication between the Windows host and the Wazuh server. Dashboard accessibility issues were permanently resolved.

## Skills Learned

* Linux network configuration
* Netplan administration
* Static IP assignment
* VirtualBox Host-Only networking
* Connectivity troubleshooting and validation
* Service verification in Linux environments

