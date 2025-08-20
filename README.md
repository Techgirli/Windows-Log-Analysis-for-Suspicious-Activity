# Windows-Log-Analysis-for-Suspicious-Activity
# Introduction
I used this to detect signs of unauthorized access, failed logins, account lookout, etc., through log analysis to check for suspicious activities using Event ID, and to perform a Brute force attack on Kali in my Home Lab.
# Tools used 
1) Windows 10
2) Kali Linux
3) Event Viewer
4) PowerShell
# Steps 
- I used Kali for a brute-force attack
- Opened Event Viewer on Windows (eventvwr.msc)
- Navigate to: Windows Logs > Security
- Filter for Event IDs
    - 4624 (Successful Logon)
    - 4625 (Failed Logon)
    - 4720 (New User Created)
    - 4723 (Password Change)
  - Analyze Patterns
     - Repeated 4625 events? -- Brute Force Attack
     - 4720 event followed by 4624 - Rogue user creation
  - Document Findings
    - Time of Event
    - Source IP address (checking event details)
    - Username used. 
  
