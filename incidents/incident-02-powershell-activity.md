# Incident 02 – Suspicious PowerShell Activity

## Alert Summary
An alert was triggered in Splunk indicating execution of a PowerShell command with encoded parameters.

## Detection
Search query used:

index=windows powershell.exe
| search CommandLine="*enc*"

## Investigation Steps
- Reviewed the command line arguments used in the PowerShell execution  
- Checked parent process associated with the execution  
- Verified whether the activity aligned with known administrative tasks  

## Findings
A PowerShell process was executed using encoded command parameters.
The parent process did not clearly match common administrative tools or scheduled tasks.

## Analysis
Encoded PowerShell commands are commonly used to obfuscate script content and may indicate malicious intent.
However, certain legitimate scripts may also use encoding for data handling or automation purposes.
The lack of clear association with expected administrative activity increases the level of suspicion.
If the encoded command were to initiate external communication or download content, this would significantly increase the likelihood of malicious behavior.

## Conclusion

The activity is considered suspicious and warrants further investigation, particularly to decode and review the command content.
