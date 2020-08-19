# Windows Defender Sigma Rules

<p align="center">
  <img src="https://github.com/diskurse/windef-detect/blob/master/images/manually-update-definitions-for-windows-defender-in-windows-10-red-png-windows-300_300.png?raw=true">
</p>

Sigma dev rules for vanilla Windows Defender logs (not ATP).

You can find the full official [Sigma repo here](https://github.com/Neo23x0/sigma).


## The Logs

| EventID | Description |
| --------| ------------- |
| 1000  | MALWAREPROTECTION_SCAN_STARTED      |
| 1001  | MALWAREPROTECTION_SCAN_COMPLETED    |
| 1002  | MALWAREPROTECTION_SCAN_CANCELLED    |
| 1003  | MALWAREPROTECTION_SCAN_PAUSED       |
| 1004  | MALWAREPROTECTION_SCAN_RESUMED      |
| 1005  | MALWAREPROTECTION_SCAN_FAILED.      |
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


## Usage

These rules paired with a free SIEM solution would be useful for small organizations, businesses or NGOs.

In Splunk this logsource is called "WinEventLog:Microsoft-Windows-Windows Defender/Operational".


## License

MIT License

Copyright (c) 2020

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
