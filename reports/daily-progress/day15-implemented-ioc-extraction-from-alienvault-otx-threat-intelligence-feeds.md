Day 15 – Implemented IOC Extraction from AlienVault OTX Threat Intelligence Feeds
Objective

Enhance the Threat Intelligence Platform by progressing from basic threat pulse retrieval to extracting actionable Indicators of Compromise (IOCs) from AlienVault Open Threat Exchange (OTX) feeds. The objective was to validate the complete workflow of authenticated API communication, threat feed parsing, and IOC extraction for future enrichment and correlation with Wazuh alerts.

Activities Performed
Environment Verification
Activated the Python virtual environment for the Threat Intelligence module.
Verified the correct Python interpreter and project directory.
Confirmed all required project files were available and accessible.
AlienVault OTX Integration Validation
Verified successful authentication with the AlienVault OTX API using the configured API key.
Confirmed stable communication with the subscribed threat pulse endpoint.
Retrieved the latest threat intelligence feeds from OTX.
Threat Feed Parsing
Parsed JSON responses returned by the AlienVault OTX API.
Validated the structure of threat pulse objects.
Examined pulse metadata including title, author, and creation timestamp.
IOC Extraction

Developed a dedicated IOC extraction script capable of parsing threat indicators from OTX pulses.

Successfully extracted multiple IOC categories including:

MD5 file hashes
SHA1 file hashes
SHA256 file hashes
Domain indicators

Verified that each indicator was successfully associated with its corresponding IOC type.

Script Validation and Debugging

Resolved multiple implementation issues encountered during development, including:

Python command invocation errors
Variable naming inconsistencies
API request formatting mistakes
JSON parsing issues
Python syntax and output formatting errors

After debugging, the IOC extraction pipeline executed successfully and produced structured indicator output.

Results
Successfully authenticated with AlienVault OTX.
Retrieved live threat intelligence feeds.
Parsed threat pulse metadata.
Extracted actionable Indicators of Compromise from threat intelligence feeds.
Verified support for multiple IOC types including hashes and domains.
Established the foundation for future IOC normalization, enrichment, database storage, and SIEM correlation.
Knowledge Gained
Structure of AlienVault OTX threat pulse objects.
Threat intelligence feed parsing using Python.
JSON data processing and traversal.
Indicator of Compromise extraction techniques.
Practical debugging of Python-based API integrations.
Foundations of automated Threat Intelligence Platform development.
Next Steps
Normalize extracted IOCs into a standardized schema.
Store normalized indicators for future enrichment.
Prepare IOC data for MongoDB integration.
Correlate threat intelligence indicators with Wazuh security alerts.
Automate periodic threat feed collection and processing.
Status

Day 15 successfully completed. The Threat Intelligence Platform now progresses beyond simple threat feed retrieval and is capable of extracting structured Indicators of Compromise from live AlienVault OTX threat intelligence feeds, providing the foundation for advanced threat enrichment and automated detection workflows.