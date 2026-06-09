# Day 10 - File Integrity Monitoring

## Objective
Configure and validate Wazuh File Integrity Monitoring (FIM) on the Windows endpoint and verify that file changes are detected in real time.

## Tasks Performed
- Investigated why file monitoring events were not appearing in Wazuh.
- Located and edited the Windows agent ossec.conf configuration file.
- Added C:\Desktop as a custom monitored directory with realtime monitoring enabled.
- Restarted the Wazuh agent service using PowerShell.
- Verified agent connectivity and checked agent logs.
- Created, modified, and deleted test files in the monitored directory.
- Observed generated alerts inside the Wazuh Threat Hunting dashboard.

## Results
- Successfully enabled real-time File Integrity Monitoring.
- Wazuh detected file creation events.
- Wazuh detected file modification events.
- Wazuh detected file deletion events.
- Confirmed that the Windows endpoint was sending FIM events to the Wazuh manager.

## Skills Learned
- Wazuh Agent Configuration
- File Integrity Monitoring (FIM)
- Windows Endpoint Monitoring
- PowerShell Service Management
- Threat Hunting and Event Analysis

## Conclusion
Successfully configured and validated Wazuh File Integrity Monitoring on the Windows endpoint. The SIEM was able to detect and log file creation, modification, and deletion activities in real time, demonstrating a key endpoint security monitoring capability.