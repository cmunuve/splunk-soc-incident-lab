# Incident 03 – Suspicious File Download

## Alert Summary
An alert was triggered indicating that a user downloaded an executable file from an external source.

## Detection
Search query used:

index=proxy OR index=web
| search file_type="exe"

## Investigation Steps
- Reviewed the URL from which the file was downloaded  
- Checked file type and naming pattern  
- Compared activity with normal user behavior  

## Findings
The user downloaded an executable file from an external website.
The domain did not match commonly used or trusted sources within the environment.
No prior history of similar downloads was observed for this user account.

## Analysis
Executable downloads from external sources may indicate phishing or delivery of malicious payloads.
However, some legitimate software installations also involve downloading executable files.
The unfamiliar domain and lack of clear business justification increase the level of concern.

## Conclusion
The activity is considered suspicious and may represent a potential phishing or malware delivery attempt.  
Further verification of the file source and user intent is recommended.
