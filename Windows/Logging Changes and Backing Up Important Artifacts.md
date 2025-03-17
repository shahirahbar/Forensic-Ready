# Logging Changes and Backing Up Important Artifacts  
One of the most important aspects of forensic analysis is the use of important activity information in Windows, which is stored in registry keys, file paths, and other locations. Ensure that changes to these items are logged and periodically backed up using various tools.  

## File Records  

| Filesystem | Location | Tools or Commands |
|------------|----------|-------------------|
| MFT | C:\ | MFTECmd.exe -f "C:\Temp\SomeMFT" --csv "c:\temp\out" --csvf MyOutputFile.csv |
| UsnJrnl | C:\$Extend | MFTECmd.exe -f "C:\Temp\SomeJ" --csv "c:\temp\out" --csvf MyOutputFile.csv |

## Registry Keys and Paths Related to System and User Information  

| Filesystem | Location |
|------------|----------|
| Operating System Version | SOFTWARE\Microsoft\Windows NT\CurrentVersion |
| System Boot & Autostart Programs | Run Registries |
| Computer Name | SYSTEM\CurrentControlSet\Control\ComputerName\ComputerName |
| System Last Shutdown Time | SYSTEM\CurrentControlSet\Control\Windows |
| User Accounts | SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList |
| Last Login and Password Change | SAM\Domains\Account\Users |

## Registry Keys and Paths Related to Application Execution  
Back up the following paths using the mentioned tools and ensure changes are logged.  

| Filesystem | Location | Tools or Commands |
|------------|----------|-------------------|
| Shimcache | SYSTEM\CurrentControlSet\Control\SessionManager\AppCompatCache | RegRipper |
| Amcache.hve | C:\Windows\AppCompat\Programs\Amcache.hve | Registry Explorer |
| UserAssist | NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\UserAssist | Registry Explorer |
| Win10 Timeline | C:\%USERPROFILE%\AppData\Local\ConnectedDevicesPlatform\L.Administrator\ActivitiesCache.db | WxTCmd.exe -f "ActivitiesCache.db" --csv D:\Hands-On |
| SRUM | C:\Windows\System32\sru\SRUDB.dat | srum-dump |
| BAM / DAM | SYSTEM\ControlSet001\Services\bam\State\UserSettings | Registry Explorer |
| Prefetch, MFT, USNJ | C:\Windows\prefetch | PECmd.exe -d D:\Windows\Prefetch, MFT, USNJ --csv "D:\Hands-On" --csvf prefetch.csv or WinPrefetch, MFT, USNJ |
| Task Bar Feature Usage | NTUSER\Software\Microsoft\Windows\CurrentVersion\Explorer\FeatureUsage | Registry Explorer |
| Jumplist | C:\%USERPROFILE%\AppData\Roaming\Microsoft\Windows\Recent\AutomaticDestinations | Jumplist Explorer |
| Last Visited MRU | NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\ComDlg32\LastVisitedPidlMRU | RegRipper |
| CapabilityAccess Manager | NTUSER\Software\Microsoft\Windows\CurrentVersion\CapabilityAccessManager\ConsentStore | Registry Explorer |
| Commands Executed in the Run Dialog | NTUSER\Software\Microsoft\Windows\CurrentVersion\Explorer\RunMRU | Registry Explorer |
| Services | System\CurrentControlSet\Services | Registry Explorer |

## Information Related to Opening Files and Folders  
Back up the following paths using the mentioned tools and ensure changes are logged.  

| Filesystem | Location | Tools or Commands |
|------------|----------|-------------------|
| Shellbag | NTUSER.dat\Software\Microsoft\Windows\Shell\Bags | Shellbags Explorer |
| Open/Save MRU | NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\ComDlg32\OpenSavePidlMRU | Registry Explorer |
| Shortcut (LNK) Files | %USERPROFILE%\AppData\Roaming\Microsoft\Windows\Office\Recent | Autopsy |
| Jumplist | C:\%USERPROFILE%\AppData\Roaming\Microsoft\Windows\Recent\AutomaticDestinations | Jumplist Explorer |
| Recent Files | NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\RecentDocs | Registry Explorer |
| Office Recent Files | NTUSER.DAT\Software\Microsoft\Office\Version>\<AppName> | Registry Explorer |
| Office Trust Records | NTUSER\Software\Microsoft\Office\Version>\<AppName>\Security\Trusted Documents\TrustRecords | Registry Explorer |
| MS Word Reading Locations | NTUSER\Software\Microsoft\Office\Version>\Word\Reading Locations | Registry Explorer |
| Office OAlerts | OAlerts.evtx | Event Log Explorer |
| Last Visited MRU | NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\ComDlg32\LastVisitedPidlMRU | Registry Explorer |
| Internet Explorer file:/// | %USERPROFILE%\AppData\Local\Microsoft\Windows\WebCache\WebCacheV*.dat | Text Editor |

## Information Related to Deleted Files  

| Filesystem | Location | Tools or Commands |
|------------|----------|-------------------|
| Recycle Bin | C:\$Recycle.Bin | Reebin |
| Thumbcache | %USERPROFILE%\AppData\Local\Microsoft\Windows\Explorer | Thumbcache Viewer |
| User Typed Paths | NTUSER\Software\Microsoft\Windows\CurrentVersion\Explorer\TypedPaths | Registry Explorer |
| Search – WordWheelQuery | NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\WordWheelQuery | Registry Explorer |
| Internet Explorer file:/// | %USERPROFILE%\AppData\Local\Microsoft\Windows\WebCache\WebCacheV*.dat | Text Editor |
| Windows Search Database | C:\ProgramData\Microsoft\Search\Data\Applications\Windows\Windows.edb | LostPassword's Search Index Examiner |

## Browser Activity  

| Filesystem | Location | Tools or Commands |
|------------|----------|-------------------|
| Browser Activity | C:\Users\%user%\AppData\Local\Roaming\BrowserName | DBBrowser |

## Network Activities  

| Filesystem | Location | Tools or Commands |
|------------|----------|-------------------|
| Network History | SOFTWARE\Microsoft\Windows NT\CurrentVersion\Network* | Registry Explorer |
| Timezone | SYSTEM\CurrentControlSet\Control\TimeZoneInformation | Registry Explorer |
| WLAN Event Log | Microsoft-Windows-WLAN-AutoConfig/Operational.evtx | Event Log Viewer |
| Network Interfaces | SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\Interfaces | Registry Explorer |
| SRUM | C:\Windows\System32\sru\SRUDB.dat | srum-dump |

## USB Activities  

| Filesystem | Location | Tools or Commands |
|------------|----------|-------------------|
| USB Device Identification | SYSTEM\CurrentControlSet\Enum\* | Registry Explorer |
| Drive Letter and Volume Name | SOFTWARE\Microsoft\Windows Portable Devices\Devices and SYSTEM\MountedDevices | Registry Explorer |
| User Information | SYSTEM\MountedDevices and NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\MountPoints2 | Registry Explorer |
| Connection Timestamps | SYSTEM\CurrentControlSet\Enum\USBSTOR\Disk&Ven_#Prod_USBSerial | Registry Explorer |
| Volume Serial Number (VSN) | SOFTWARE\Microsoft\WindowsNT\CurrentVersion\EMDMgmt | Registry Explorer |
| Shortcut (LNK) Files | %USERPROFILE%\AppData\Roaming\Microsoft\Windows\Office\Recent\ | Autopsy |
| Event Logs | System.evtx | Event Log Viewer |

## Antivirus Logs  

| Filesystem | Location |
|------------|----------|
| WinDefender | C:\ProgramData\Microsoft\Windows Defender\* or C:\ProgramData\Microsoft\Microsoft AntiMalware\Support\ or MpCmdRun.log | 

Other Information  

| Filesystem | Location | Tools or Commands |
|------------|----------|-------------------|
| Task Scheduler | SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\TaskCache\Tasks or Windows\Tasks or Windows\System32\Tasks | Registry Explorer |
| Startup Folder | C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Startup | Autopsy |
| Startup Folder User | C:\%USERPROFILE%\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup | Autopsy |
| Copy |  |Explorer|
| hiberfil.sys | C:\ | Hibernation Recon |
| pagefile.sys | C:\ | strings |
| Unalloc File | - | Autopsy |
| AnyDesk | C:\Users\%user%\AppData\Roaming\AnyDesk\* or C:\ProgramData\AnyDesk\* | Autopsy |
| WMI Persistence | C:\WINDOWS\system32\wbem\Repository\OBJECTS.DATA | WMI_Forensics |
| WMI Persistence | C:\WINDOWS\system32\wbem\Repository\FS\OBJECTS.DATA | WMI_Forensics |
| RDP Cache | C:\%USERPROFILE%\AppData\Local\Microsoft\Terminal Server Client\Cache | BMC-Tools |
