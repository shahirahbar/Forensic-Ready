# Important Event IDs  
Ensure the following Event IDs are logged:  

| Event ID | Event Log | Context |
|----------|-----------|---------|
| 4624 | Security | Successful Login |
| 4625 | Security | Failed Login |
| 4634/4647 | Security | User Initiated Logoff/An Account was Logged Off |
| 4648 | Security | A Logon was Attempted Using Explicit Credentials |
| 4662 | Security | An Operation was Performed on an Object |
| 4663 | Security | An Attempt was Made to Access an Object |
| 4672 | Security | Special Logon |
| 4688 | Security | Process Creation |
| 4689 | Security | Process Termination |
| 4697 | Security | Service Installed |
| 4698/4702/4700 | Security | Scheduled Task Created or Updated |
| 4699 | Security | Scheduled Task Deleted |
| 4701 | Security | Scheduled Task Enabled |
| 4702 | Security | Service Removed |
| 4720 | Security | A User Account was Created |
| 4722 | Security | A User Account was Enabled |
| 4723 | Security | An Attempt was Made to Change an Account’s Password |
| 4724 | Security | An Attempt was Made to Reset an Account’s Password |
| 4725 | Security | A User Account was Disabled |
| 4726 | Security | A User Account was Deleted |
| 4728 | Security | A Member was Added to a Security-Enabled Global Group |
| 4729 | Security | A Member was Removed from a Security-Enabled Global Group |
| 4732 | Security | A Security-Enabled Local Group was Created |
| 4733 | Security | A Security-Enabled Local Group was Changed |
| 4734 | Security | A Security-Enabled Local Group was Deleted |
| 4741 | Security | A Computer Account was Created |
| 4742 | Security | A Computer Account was Changed |
| 4768 | Security (DC) | Kerberos TGT Request |
| 4769 | Security (DC) | Kerberos Service Ticket Request |
| 4771 | Security | Locked Out Account |
| 4776 | Security | NTLM Authentication |
| 4778 | Security | Session Reconnected |
| 4779 | Security | Session Disconnected by User |
| 4794 | Security | An Attempt was Made to Set the Directory Services Restore Mode Administrator Password |
| 5136 | Security | Directory Service Changes |
| 5140 | Security | A Network Share Object was Accessed |
| 5141 | Security | A Directory Service Object was Deleted |
| 5145 | Security | Network Share Object was Checked |
| 5376 | Security | Credential Manager Credentials Submitted |
| 5377 | Security | Credential Manager Credentials Auto-Logon |
| 1102 | Security | Event Log Cleared |
| 1100 | Security | Event Log Service Shutdown |

## Important Logon Types  
Ensure that successful and failed logon attempts are logged with their types and methods.  

| Logon Type | Explanation |
|------------|-------------|
| 2 | Logon via Console |
| 3 | Network Logon. A user or computer logged on to this computer from the network |
| 4 | Batch Logon (Task Scheduler and AT) |
| 5 | Windows Service Logon |
| 7 | Credentials Used to Unlock Screen |
| 8 | Network Logon Sending Credentials (Cleartext) |
| 9 | Different Credentials Used Than Logon User |
| 10 | Remote Interactive Logon (RDP) |
| 11 | Cached Credentials Used to Logon |
| 12 | Cached Remote Interactive (RDP) |
| 13 | Cached Unlock (Similar to Logon Type 7) |

## Other Important Event IDs  
In addition to the Event IDs listed in the Security log, ensure the following Event IDs are logged and stored in important log sources:  

| Event ID | Event Log |
|----------|-----------|
| 7045 | System |
| 7034 | System |
| 7035 | System |
| 7036 | System |
| 7040 | System |
| 7001 | System |
| 1001 | System |
| 6005 | System |
| 6006 | System |
| 104 | System |
| 59 | Microsoft-Windows-Bits-Client/Operational |
| 2004 | Microsoft-Windows-Windows Firewall with Advanced Security |
| 2006 | Microsoft-Windows-Windows Firewall with Advanced Security |
| 1116 | Microsoft-Windows-Windows Defender/Operational |
| 1117 | Microsoft-Windows-Windows Defender/Operational |
| 1006 | Microsoft-Windows-Windows Defender/Operational |
| 4103 | Microsoft-Windows-PowerShell/Operational |
| 4104 | Microsoft-Windows-PowerShell/Operational |
| 4105 | Microsoft-Windows-PowerShell/Operational |
| 4688 | Microsoft-Windows-PowerShell/Operational |
| 400 | Windows PowerShell |
| 403 | Windows PowerShell |
| 800 | Windows PowerShell |
| 91 | WinRM |
| 168 | WinRM |
| 1000 | Application |
| 1001 | Application |
| 1002 | Application |
| 1024 | Application |
| 1040 | Application |
| 1033 | Application |
| 1034 | Application |
| 11707 | Application |
| 11708 | Application |
| 11724 | Application |
| 1 | Microsoft-Windows-Sysmon/Operational |
| 2 | Microsoft-Windows-Sysmon/Operational |
| 3 | Microsoft-Windows-Sysmon/Operational |
| 6 | Microsoft-Windows-Sysmon/Operational |
| 7 | Microsoft-Windows-Sysmon/Operational |
| 8 | Microsoft-Windows-Sysmon/Operational |
| 10 | Microsoft-Windows-Sysmon/Operational |
| 11 | Microsoft-Windows-Sysmon/Operational |
| 12 | Microsoft-Windows-Sysmon/Operational |
| 1149 | Microsoft-Windows-TerminalServices-RemoteConnectionManager/Operational |
| 21 | Microsoft-Windows-TerminalServices-RemoteConnectionManager/Operational |
| 24 | Microsoft-Windows-TerminalServices-RemoteConnectionManager/Operational |
| 25 | Microsoft-Windows-TerminalServices-RemoteConnectionManager/Operational |
| 131 | RDPCoreTS |
| 106 | Task Scheduler |
| 140 | Task Scheduler |
| 141 | Task Scheduler |
| 200 | Task Scheduler |
| 201 | Task Scheduler |
| 5857 | WMI-Activity Operational |
| 5858 | WMI-Activity Operational |
| 5859 | WMI-Activity Operational |
| 5860 | WMI-Activity Operational |
| 5861 | WMI-Activity Operational |
| 31001 | SMBClient-Security |
