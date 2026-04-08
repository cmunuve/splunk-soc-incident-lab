# Lab Architecture
This lab simulates a simplified enterprise environment for security monitoring and investigation.

## Components
- Splunk (SIEM platform) – used for log aggregation and analysis  
- Windows system logs – used to simulate authentication and system activity  
- Manually generated test activity – used to generate alert scenarios  

## Data Flow
Logs are ingested into Splunk where they are queried and analyzed to identify suspicious activity.

## Notes
The environment is intentionally simplified to focus on the investigation workflow rather than infrastructure complexity.
