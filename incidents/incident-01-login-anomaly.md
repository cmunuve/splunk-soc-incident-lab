# Incident 01 – Authentication Anomaly

## Alert Summary
An alert was triggered in Splunk indicating multiple failed login attempts for a user account within a short time period.

## Detection
Search query used:
index=windows EventCode=4625
| stats count by user, src_ip

## Investigation Steps
- Reviewed failed login events associated with the account  
- Checked frequency and timing of login attempts  
- Examined source IP address for consistency  

## Findings
Multiple failed login attempts were observed within a short timeframe, followed by a successful login.
The source of the login attempts appeared consistent across events.

## Analysis
While this pattern may suggest credential guessing or brute-force activity, it may also result from normal user behavior such as repeated incorrect password entry.
No additional suspicious activity (such as unusual processes or network connections) was observed immediately after the login.

## Conclusion
The activity is considered suspicious but not conclusively malicious.  
Further monitoring of the account is recommended.
