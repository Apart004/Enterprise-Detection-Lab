# Day 9 - Authentication Monitoring and Threat Hunting Validation

## Objectives
- Generate security-relevant Windows events.
- Validate authentication monitoring capabilities.
- Verify end-to-end log collection and detection.

## Activities Performed
- Confirmed Windows-PC agent connectivity.
- Accessed Wazuh Threat Hunting dashboard.
- Created a temporary Windows test account.
- Simulated multiple failed login attempts using incorrect credentials.
- Investigated generated events within Wazuh.

## Results
- Successfully detected multiple authentication failures.
- Observed "Logon Failure - Unknown user or bad password" events.
- Verified Windows Security Event Log collection.
- Confirmed real-time visibility of endpoint authentication activity.

## Skills Learned
- Threat Hunting workflow.
- Authentication event analysis.
- Windows Security Log monitoring.
- Detection validation techniques.

## Status
Threat Hunting environment fully operational. Authentication-related security events are successfully detected and visible within Wazuh.