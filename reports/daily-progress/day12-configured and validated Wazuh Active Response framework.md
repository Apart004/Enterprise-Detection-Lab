#Day 12 Report

Title: Active Response Configuration and Validation

Today I configured Wazuh Active Response on the SIEM server. The Wazuh manager configuration was modified to enable automatic response actions for alerts with severity level 10 and above. After updating the configuration, syntax validation was performed successfully using the Wazuh analysis daemon testing utility.

The Wazuh manager service was restarted and log verification confirmed that the Active Response and execution queues were initialized correctly. A high-severity privilege escalation event was generated through a successful sudo execution, producing a level 13 alert within Wazuh. This verified that the alerting pipeline and threshold configuration were functioning correctly.

Further validation included inspection of the Active Response framework and available response scripts such as host-deny, firewall-drop, disable-account, and route-null. While detection and response infrastructure were confirmed operational, no response action was executed because the tested event did not contain the network attributes required by the configured host-deny action.

The exercise demonstrated successful deployment and validation of Wazuh Active Response components and prepared the environment for automated containment testing during later threat detection exercises.