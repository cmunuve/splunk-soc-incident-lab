# Incident 04 – Privilege-Related Activity

## Alert Summary
An alert was triggered indicating execution of commands related to privilege enumeration on a system.

## Detection
Search query used:

index=windows ("whoami" OR "net localgroup administrators")

## Investigation Steps
- Reviewed command execution logs  
- Identified user account associated with the activity  
- Checked whether the account has administrative privileges  
- Verified timing of the activity against expected administrative operations 

## Findings
Commands related to privilege enumeration were executed on the system.
The activity involved commands commonly used to identify user privileges and group memberships.
The account performing the activity did not clearly align with known administrative roles within the environment.

## Analysis
Privilege enumeration commands are often used by attackers after gaining initial access to understand system permissions.
However, similar commands may also be used by administrators during troubleshooting or system checks.
The context of the activity, including user role and timing, is critical in determining intent.

## Conclusion
The activity is considered suspicious but requires further validation to determine whether it is part of legitimate administrative behavior.
