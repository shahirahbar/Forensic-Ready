# Important Log Sources  
Ensure the following log sources are active and the related files are created in the specified paths. Periodically back up these logs on a separate system.  

| Log Sources | Context |
|-------------|---------|
| Security.evtx | Security-related events |
| System.evtx | Tracks system component events |
| Application.evtx | Logs application-specific events |
| Microsoft-Windows-Sysmon/Operational.evtx | Enhanced process, network, and file monitoring |
| Microsoft-Windows-PowerShell/Operational.evtx | Records PowerShell activity |
| Microsoft-Windows-Windows Defender/Operational.evtx | Logs Windows Defender events |
| Microsoft-Windows-WMI-Activity/Operational.evtx | Logs WMI events |
| Microsoft-Windows-TerminalServices-RemoteConnectionManager/Operational.evtx | Logs RDP session events |
| Microsoft-Windows-TerminalServices-LocalSessionManager/Operational.evtx | Logs RDP session events |
| Microsoft-Windows-TaskScheduler/Operational.evtx | Logs Task Scheduler events |
| Microsoft-Windows-DNS-Server/Operational.evtx | DNS Server Logs |
| Active Directory Server Logs | |
| Directory Service.evtx | Active Directory Server Logs |
| File Replication Service.evtx | Active Directory Server Logs |
| %SystemDrive%\inetpub\logs\LogFiles | IIS Log |
| %SystemRoot%\System32\LogFiles\HTTPERR | IIS Log |
| %ProgramFiles%\Microsoft\Exchange Server\V15\Logging | Exchange Log |
| Panther*.log | Windows Setup Details |
| RPC Client Access*.log | Exchange Server Logs |
| Third-party Antivirus Log | Antivirus Logs |

## Estimating Required Storage Space for Logs  
To plan log storage, estimate the space required for each log type and the total space needed for log storage. Below is a table estimating the required space for each log type:  

| Log Type | Estimated Space Required (MB) |
|----------|-------------------------------|
| Security.evtx | 50-100 |
| System.evtx | 20-50 |
| Application.evtx | 10-30 |
| Microsoft-Windows-Sysmon/Operational.evtx | 100-200 |
| Microsoft-Windows-PowerShell/Operational.evtx | 20-50 |
| Microsoft-Windows-Windows Defender/Operational.evtx | 10-30 |
| Microsoft-Windows-WMI-Activity/Operational.evtx | 10-20 |
| Microsoft-Windows-TerminalServices-RemoteConnectionManager/Operational.evtx | 10-30 |
| Microsoft-Windows-TaskScheduler/Operational.evtx | 5-10 |
| IIS Logs | 0-200 |
| Exchange Logs | 100-500 |
