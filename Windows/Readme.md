# What are the best practices to ensure a Windows OS is forensic-ready?
Forensic experts require specific information from the target system to perform their analysis. The absence of this information can disrupt their work. Therefore, the following must be available either live or logged and stored in a secure location for future use:  

- Log sources  
- Important security and system Event IDs  
- Registry keys  
- Memory information  
- User and file activities  

## Table of Contents  
##### 1.1 Important Log Sources
##### 1.2 Important Event IDs  
      1.2.1 Important Logon Types for Event IDs 4624 and 4625  
      1.2.2 Other Important Event IDs  
##### 1.3 Logging Changes and Backing Up Important Artifacts  
      1.3.1 File Records  
      1.3.2 Registry Keys and Paths Related to System and User Information  
      1.3.3 Registry Keys and Paths Related to Application Execution  
      1.3.4 Information Related to Opening Files and Folders  
      1.3.5 Information Related to Deleted Files  
      1.3.6 Browser Information  
      1.3.7 Network Activities  
      1.3.8 USB Activities  
      1.3.9 Antivirus Logs  
      1.3.10 Other Information  
##### 1.4 Periodic Commands (KAPE)
