# Periodic Commands (KAPE)
To ensure that important forensic information is available, run the KAPE tool periodically (recommended weekly) with the following commands and store the output in a location outside the system.  

### Basic Command 

```bash
.\kape.exe --tsource [DRIVE LETTER] --tdest [DESTINATION INCLUDE FOLDER NAME] --module [MODULE NAME] --quiet
```

```bash
.\kape.exe --msource [DRIVE LETTER] --mdest [DESTINATION INCLUDE FOLDER NAME] --module [MODULE NAME] --quiet
```
### KAPE Target Extraction
```bash
.\kape.exe --tsource E: --tdest D:\KAPE_cases\ --target KapeTriage,MessagingClients,RemoteAdmin,ServerTriage,WebBrowsers,WebServers,WSL,MemoryFiles --quiet
```
### Memory Dump
```bash
.\kape.exe --msource C:\ --mdest D:\KAPE_cases\&m --module MagnetForensics_RAMCapture --quiet
```
### Live Response Command and Scanner
```bash
.\kape.exe --msource E:\ --mdest D:\KAPE_cases\&m --module PowerShell_Get-InjectedThread,Powershell_Get-NetworkConnection,Powershell_Netscan,Powershell_Signed,SIDR_WindowsIndexSearchParser,WiFiPassView,MagnetForensics_EDD,Nirsoft_BluetoothView,Nirsoft_LastActivityView,Nirsoft_OpenedFilesView,Nirsoft_USBDeview,Nirsoft_VideocacheView,Nirsoft_WebBrowserPassView,Nirsoft_WhatInStartup,Nirsoft_WifiHistoryView,Nirsoft_WirelessKeyView,SysInternals_Autoruns,SysInternals_Handle,SysInternals_PsFile,SysInternals_PsInfo,SysInternals_PsList,SysInternals_PsLoggedOn,SysInternals_PsService,SysInternals_PsTree,SysInternals_TcpView,Powershell_LiveResponse_SystemInfo,PowerShell_Arp_Cache_Extraction,Powershell_Bitlocker_Key_Extraction,PowerShell_Bitlocker_Status,PowerShell_Defender_Exclusions,PowerShell_DLL_List,Powershell_Dns_Cache,Powershell_Local_Group_List,Powershell_LocalAdmin,PowerShell_NamedPipes,PowerShell_NetUserAdministrators,PowerShell_Network_Configuration,Powershell_Network_Connections_Status,PowerShell_Network_Share,PowerShell_Process_Cmdline,PowerShell_ProcessList_CimInstance,Powershell_ProcessList_WMI,PowerShell_Services_List,PowerShell_SMBMapping,PowerShell_SMBOpenFile,PowerShell_SMBSession,PowerShell_Startup_Commands,PowerShell_User_List,PowerShell_WMIRepositoryAuditing,Windows_ARPCache,Windows_DNSCache,Windows_GpResult,Windows_IPCConfig,Windows_MsInfo,Windows_nbtsat_NetBIOSCache,Windows_nbtsat_NetBIOSSessions,Windows_Net_Accounts,Windows_Net_File,Windows_Net_LocalGroup,Windows_Net_Session,Windows_Net_Share,Windows_Net_Start,Windows_Net_Use,Windows_Net_User,Windows_netsh_portproxy,Windows_NetStat,Windows_qwinsta_RDPSessions,Windows_RoutingTable,Windows_schtasks,Windows_SystemInfo,RegHunter,hasherezade_HollowsHunter --quiet
```
### All-in-One Artifact Parsing
```bash
.\kape.exe --msource E:\ --mdest D:\KAPE_cases\ --module Loki_Scan,DensityScout,BackstageParser,BitsParser,CCMRUAFinder_RecentlyUsedApps,Chainsaw,DeepblueCLI,DHParser,EvtxHussar,hasherezade_HollowsHunter,INDXRipper,LevelDBDumper,OneDriveExplorer,PowerShell_Get-ChainsawSigmaRules,TeamsParser,ThumbCacheViewer,WMI-Parser,Zircolite_Scan,Zircolite_Update,LogParser_ApacheAccessLogs,LogParser_DetailedNetworkShareAccess,LogParser_LogonLogoffEvents,LogParser_RDPUsageEvents,LogParser_SMBServerAnonymousLogons,Nirsoft_AlternateStreamView,Nirsoft_BrowsingHistoryView,Nirsoft_FullEventLogView_AllEventLogs,Nirsoft_FullEventLogView_Application,Nirsoft_FullEventLogView_PowerShell-Operational,Nirsoft_FullEventLogView_PrintService-Operational,Nirsoft_FullEventLogView_ScheduledTasks,Nirsoft_FullEventLogView_Security,Nirsoft_FullEventLogView_System,Nirsoft_TurnedOnTimesView,Nirsoft_WebBrowserDownloads,Nirsoft_WinLogonView,SysInternals_SigCheck,TZWorks_CARE,Registry_System,Events-Ripper,Hayabusa,LogParser,MTFECmd,NTFSLogTracker,RECmd_AllBatchFiles,RegHunter,RegRipper,AmcacheParser,AppCompatCacheParser,EvtxECmd,EvtxECmd_RDP,IISGeoLocate,JLECmd,LECmd,PECmd,RBCmd,RecentFileCacheParser,SBECmd,SQLECmd,SQLECmd_Hunt,StrumECmd,SumECmd,WxTCmd,Sync_EvtxECmd,Sync_KAPE,Sync_RECmd,Sync_SQLECmd,Windows_ManageBDE_BitLockerKeys,Windows_ManageBDE_BitLockerStatus --quiet
```
### Event Log / Log Scanning and Parsing
```bash
.\kape.exe --msource E:\ --mdest D:\KAPE_cases\ --module !!ToolSync,PowerShell_Get-ChainsawSigmaRule,Chainsaw,DeepblueCLI,EvtxHussar,Zircolite_Update,Zircolite_Scan,Events-Ripper,hayabusa_EventStatistics,hayabusa_OfflineEventLogs,hayabusa_OfflineLogonSummary,hayabusa_UpdateRules,EvtxECmd,EvtxECmd_RDP,LogParser,IISGeoLocate
```
### Program Execution
```bash
.\kape.exe --msource E:\ --mdest D:\KAPE_cases\ --module CCMRUAFinder_RecentlyUsedApps,AmcacheParser,AppCompatCacheParser,PECmd,RecentFileCacheParser --quiet
```
### File Folder Activity
```bash
.\kape.exe --msource E:\ --mdest D:\KAPE_cases\ --module BackstageParser,OneDriveExplorer,ThumbCacheViewer,JLECmd,LECmd,RBCmd,SBECmd,WxTCmd --quiet
```
### NTFS and FileSystem Parsing
```bash
.\kape.exe --msource E:\ --mdest D:\KAPE_cases\ --module !!ToolSync,INDXRipper,MTFECmd,NTFSLogTracker,RegRipper,RECmd_AllBatchFiles --quiet
```
### System Activity
```bash
.\kape.exe --msource E:\ --mdest D:\KAPE_cases\ --module SRUMDump,WMTParser,RECmd_AllBatchFiles,StrumECmd,SumECmd --quiet
```
### Mounted Image Scanner
```bash
.\kape.exe --msource E:\ --mdest D:\KAPE_cases\ --module Loki_Scan --quiet
.\kape.exe --msource E:\ --mdest D:\KAPE_cases\ --module DensityScout --quiet
```





