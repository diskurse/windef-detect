# Microsoft (Windows) Defender Sigma Rules

<p align="center">
  <img src="https://github.com/diskurse/windef-detect/blob/master/images/manually-update-definitions-for-windows-defender-in-windows-10-red-png-windows-300_300.png?raw=true"><br>
  <img src="https://github.com/diskurse/windef-detect/blob/master/images/Sigma_0.3.png?raw=true"><br><br>
</p>

Sigma dev rules for the vanilla Microsoft Defender antivirus logs (not ATP).

You can find the full official [Sigma repo here](https://github.com/Neo23x0/sigma), it covers a lot of ground and is an invaluable resource for blue teamers.


## Usage

These rules paired with sysmon and a free SIEM solution would be useful for small organizations, businesses or NGOs.

## Log Samples

Eventually we'll be providing log samples here.

<p align="center">
<img src="https://github.com/diskurse/windef-detect/blob/master/images/Screenshot%202020-08-21%20at%2009.43.15.png?raw=true"><br><br>


## The Logs

We are looking at the log source "Microsoft-Windows-Windows Defender/Operational".

Below you can find the relevant EventIDs that Windows Defender events will generate.


| EventID | Description |
| --------| ------------- |
| 1000  | MALWAREPROTECTION_SCAN_STARTED      |
| 1001  | MALWAREPROTECTION_SCAN_COMPLETED    |
| 1002  | MALWAREPROTECTION_SCAN_CANCELLED    |
| 1003  | MALWAREPROTECTION_SCAN_PAUSED       |
| 1004  | MALWAREPROTECTION_SCAN_RESUMED      |
| 1005  | MALWAREPROTECTION_SCAN_FAILED      |
| 1006  | MALWAREPROTECTION_MALWARE_DETECTED  |
| 1007  | MALWAREPROTECTION_MALWARE_ACTION_TAKEN |
| 1008  | MALWAREPROTECTION_MALWARE_ACTION_FAILED |
| 1009  | MALWAREPROTECTION_QUARANTINE_RESTORE |
| 1010  | MALWAREPROTECTION_QUARANTINE_RESTORE_FAILED |
| 1011  | MALWAREPROTECTION_QUARANTINE_DELETE |
| 1012  | MALWAREPROTECTION_QUARANTINE_DELETE_FAILED |
| 1013  | MALWAREPROTECTION_MALWARE_HISTORY_DELETE |
| 1014  | MALWAREPROTECTION_MALWARE_HISTORY_DELETE_FAILED |
| 1015  | MALWAREPROTECTION_BEHAVIOR_DETECTED |      
| 1116  | MALWAREPROTECTION_STATE_MALWARE_DETECTED |      
| 1117  | MALWAREPROTECTION_STATE_MALWARE_ACTION_TAKEN |      
| 1118  | MALWAREPROTECTION_STATE_MALWARE_ACTION_FAILED |      
| 1119  | MALWAREPROTECTION_STATE_MALWARE_ACTION_CRITICALLY_FAILED |  
| 1120  | MALWAREPROTECTION_THREAT_HASH |
| 1150  | MALWAREPROTECTION_SERVICE_HEALTHY |
| 1151  | MALWAREPROTECTION_SERVICE_HEALTH_REPORT |
| 2000  | MALWAREPROTECTION_SIGNATURE_UPDATED |
| 2001  | MALWAREPROTECTION_SIGNATURE_UPDATE_FAILED |
| 2002  | MALWAREPROTECTION_ENGINE_UPDATED |
| 2003  | MALWAREPROTECTION_ENGINE_UPDATE_FAILED |
| 2004  | MALWAREPROTECTION_SIGNATURE_REVERSION |
| 2005  | MALWAREPROTECTION_ENGINE_UPDATE_PLATFORMOUTOFDATE |
| 2006  | MALWAREPROTECTION_PLATFORM_UPDATE_FAILED |
| 2007  | MALWAREPROTECTION_PLATFORM_ALMOSTOUTOFDATE |
| 2010  | MALWAREPROTECTION_SIGNATURE_FASTPATH_UPDATED |
| 2011  | MALWAREPROTECTION_SIGNATURE_FASTPATH_DELETED |
| 2012  | MALWAREPROTECTION_SIGNATURE_FASTPATH_UPDATE_FAILED |
| 2013  | MALWAREPROTECTION_SIGNATURE_FASTPATH_DELETED_ALL |
| 2020  | MALWAREPROTECTION_CLOUD_CLEAN_RESTORE_FILE_DOWNLOADED |
| 2021  | MALWAREPROTECTION_CLOUD_CLEAN_RESTORE_FILE_DOWNLOAD_FAILED |
| 2030  | MALWAREPROTECTION_OFFLINE_SCAN_INSTALLED |
| 2031  | MALWAREPROTECTION_OFFLINE_SCAN_INSTALL_FAILED |
| 2040  | MALWAREPROTECTION_OS_EXPIRING |
| 2041  | MALWAREPROTECTION_OS_EOL |
| 2042  | MALWAREPROTECTION_PROTECTION_EOL |
| 3002  | MALWAREPROTECTION_RTP_FEATURE_FAILURE |
| 3007  | MALWAREPROTECTION_RTP_FEATURE_RECOVERED |
| 5000  | MALWAREPROTECTION_RTP_ENABLED |
| 5001  | MALWAREPROTECTION_RTP_DISABLED |
| 5004  | MALWAREPROTECTION_RTP_FEATURE_CONFIGURED |
| 5007  | MALWAREPROTECTION_CONFIG_CHANGED |
| 5008  | MALWAREPROTECTION_ENGINE_FAILURE |
| 5009  | MALWAREPROTECTION_ANTISPYWARE_ENABLED |
| 5010  | MALWAREPROTECTION_ANTISPYWARE_DISABLED |
| 5011  | MALWAREPROTECTION_ANTIVIRUS_ENABLED |
| 5012  | MALWAREPROTECTION_ANTIVIRUS_DISABLED |
| 5100  | MALWAREPROTECTION_EXPIRATION_WARNING_STATE |
| 5101  | MALWAREPROTECTION_DISABLED_EXPIRED_STATE |


## Resources

+ [Microsoft Defender Antivirus Event IDs](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-antivirus/troubleshoot-microsoft-defender-antivirus)
+ [Defender CSP](https://docs.microsoft.com/en-us/windows/client-management/mdm/defender-csp)
+ [Defender PowerShell Functions](https://docs.microsoft.com/en-us/powershell/module/defender/?view=win10-ps)
+ [Windows Defender AV-TEST Product Review and Certification Report – May-Jun/2020](https://www.av-test.org/en/antivirus/home-windows/windows-10/june-2020/microsoft-defender-4.18-202416/)
