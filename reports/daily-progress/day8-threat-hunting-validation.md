# Day 8 – Threat Hunting and Security Event Validation

## Objectives
- Verify Windows endpoint telemetry collection.
- Generate security-relevant events.
- Validate visibility through Wazuh Threat Hunting.

## Activities Performed
- Confirmed Wazuh Manager, Indexer, and Dashboard services were active.
- Verified Windows agent connectivity.
- Accessed Threat Hunting module.
- Generated a Windows account management event by creating a test user.
- Observed security events in real time within Wazuh.

## Key Events Detected
- User account enabled or created
- User account changed
- Users Group Changed
- Domain Users Group Changed

## Outcome
Successfully validated end-to-end security event collection and analysis pipeline from Windows endpoint to Wazuh Threat Hunting dashboard.

## Skills Practiced
- Endpoint monitoring
- Security event generation
- Threat hunting
- Log analysis
- SOC workflow validation