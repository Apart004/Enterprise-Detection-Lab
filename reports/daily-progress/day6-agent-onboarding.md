# Day 6 - Windows Endpoint Onboarding and Vulnerability Detection

## Objective

Connect a Windows endpoint to the Wazuh SIEM and verify security monitoring capabilities.

## Tasks Completed

* Started and verified Wazuh Manager, Indexer, and Dashboard services.
* Configured VirtualBox networking for communication between the host and Wazuh server.
* Installed the Wazuh Windows Agent on the host machine.
* Connected the Windows agent to the Wazuh Manager.
* Verified agent registration and communication.
* Accessed the Wazuh Dashboard and confirmed endpoint visibility.
* Collected software inventory from the Windows endpoint.
* Performed vulnerability detection and assessment.

## Results

* Windows endpoint successfully connected to the Wazuh server.
* Agent status changed to Active.
* Software inventory data was collected.
* Multiple CVEs associated with installed software were detected.
* End-to-end SIEM pipeline was successfully validated.

## Skills Learned

* Wazuh agent deployment
* Endpoint onboarding
* SIEM architecture
* Host-only networking
* Vulnerability management
* Security monitoring

## Challenges Faced

* Network connectivity issues between host and Wazuh server.
* Agent registration and communication troubleshooting.
* VirtualBox adapter configuration and routing verification.

## Outcome

A functioning SOC homelab was established with a Windows endpoint actively monitored by Wazuh. The environment is now ready for alert generation, threat detection, and security monitoring exercises.
