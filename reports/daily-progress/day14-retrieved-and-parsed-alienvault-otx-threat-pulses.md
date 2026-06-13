# Day 14 – Retrieved and Parsed AlienVault OTX Threat Pulses

## Objective

Establish authenticated communication with the AlienVault Open Threat Exchange (OTX) platform and validate the ability to retrieve live threat intelligence data for future IOC processing and enrichment.

## Activities Performed

### OTX Environment Troubleshooting

* Resolved Python virtual environment configuration issues.
* Installed and verified the AlienVault OTX SDK (OTXv2).
* Corrected package management and dependency issues within the Ubuntu Server environment.
* Validated API key loading through a separate configuration file.

### API Connectivity Validation

* Established authenticated communication with the AlienVault OTX API using a personal API key.
* Verified successful HTTPS communication between the Wazuh SIEM server and the OTX cloud platform.
* Confirmed that API authentication was functioning correctly through successful HTTP responses.

### Threat Pulse Retrieval

* Developed a Python-based retrieval script using the Requests library.
* Queried the OTX subscribed pulses endpoint.
* Successfully received live threat intelligence data in JSON format.
* Verified the presence of active threat intelligence records from AlienVault.

### Threat Feed Parsing

* Parsed the JSON response returned by the OTX API.
* Extracted pulse metadata including:

  * Pulse Name
  * Author
  * Creation Timestamp
* Enumerated multiple threat intelligence pulses for analysis.

### Sample Threat Intelligence Retrieved

Examples of retrieved threat intelligence pulses included:

* ClickFix Evolves with PySoxy Proxying
* Python Backdoor Threat Analysis Following an AI Deepfake Impersonation Campaign
* LBIOC-20260071 – The Gentlemens Leak
* Targeted Espionage Against Cambodian Government Entities
* From External Espionage to Domestic Targeting

## Results

* AlienVault OTX integration successfully authenticated.
* Live threat intelligence feeds successfully retrieved.
* JSON threat feed parsing validated.
* Multiple threat pulses successfully enumerated and displayed.
* Environment prepared for IOC extraction and normalization.

## Challenges Encountered

* Python virtual environment setup issues on Ubuntu.
* SDK installation and dependency troubleshooting.
* Variable naming and script debugging errors during API testing.
* VirtualBox terminal copy/paste limitations while editing scripts.

## Knowledge Gained

* Threat Intelligence Platform architecture fundamentals.
* AlienVault OTX API authentication workflow.
* JSON feed retrieval and parsing techniques.
* Python-based threat intelligence collection methods.
* Troubleshooting API integrations within Linux environments.

## Next Steps

* Extract Indicators of Compromise (IOCs) from retrieved threat pulses.
* Identify IP addresses, domains, URLs, and file hashes.
* Normalize IOC data into a standardized schema.
* Prepare threat intelligence records for MongoDB storage and enrichment workflows.

## Status

Day 14 successfully completed. Live threat intelligence retrieval and pulse parsing have been validated. The platform is ready to begin IOC extraction and normalization.
