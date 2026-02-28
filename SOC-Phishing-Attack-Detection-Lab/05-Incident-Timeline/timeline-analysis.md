# Timeline Analysis – SOC Phishing Simulation

This document provides a chronological overview of events observed during the phishing simulation lab.  
The timeline is based on Sysmon logs collected from the Windows workstation (`umut`).

---

## Event Timeline

### 1️. Process Creation – System Operations
**Timestamp:** 02/26/2026 11:34:36 PM  
**EventCode:** 1 – Process Creation  
**Process:** `C:\Windows\System32\MpSigStub.exe`  
**User:** NT AUTHORITY\SYSTEM  
**Details:**  
- Parent Process: `C:\Windows\UUS\Packages\Preview\amd64\wuaucltcore.exe`  
- Command Line: `C:\Windows\system32\MpSigStub.exe /stub 1.1.24010.2001 /payload 1.445.264.0 /MpWUStub /program C:\Windows\SoftwareDistribution\Download\Install\AM_Delta.exe WD /q`  
- SHA256 Hash: `071B0D3A08503A8B88AEEDA1D20F371A563377028F6E252DC66CCE60AB8F823E`  

**Observation:**  
System processes related to Windows update and malware protection started.  
No user interaction required for these events.

---

### 2️. User Clicked Phishing Link
**Timestamp:** 02/26/2026 11:35:10 PM  
**EventCode:** 3 – Network Connection Detected  
**Process:** `C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe`  
**User:** UMUT\User  
**Source:** 192.168.1.108 → **Destination:** 192.168.1.106 (attacker-machine)  
**Protocol:** TCP, Port 80  

**Observation:**  
- Outbound HTTP connection initiated by browser.  
- Sysmon Event ID 3 captured the network activity.  
- Confirms phishing link click by the user.  

---

### 3️. Process Termination
**Timestamp:** 02/26/2026 11:36:15 PM  
**EventCode:** 5 – Process Terminated  
**Process:** `C:\Windows\System32\dllhost.exe`  
**Parent Process:** `C:\Windows\UUS\Packages\Preview\amd64\wuaucltcore.exe`  
**User:** UMUT\User  

**Observation:**  
- Termination of dllhost.exe was logged.  
- Indicates cleanup or system-related process termination, not malicious.  

---

## Timeline Summary

| Time (PM)       | EventCode | Event Type                  | Process / Action                               | Notes                                           |
|-----------------|-----------|-----------------------------|-----------------------------------------------|------------------------------------------------|
| 11:34:36        | 1         | Process Creation            | MpSigStub.exe                                 | Windows update/malware protection process     |
| 11:35:10        | 3         | Network Connection Detected | msedge.exe → 192.168.1.106                   | Phishing link click detected                   |
| 11:36:15        | 5         | Process Termination         | dllhost.exe                                   | Normal process termination                     |

**Key Takeaways:**  
- User interaction confirmed at 11:35:10 PM via Sysmon Event ID 3.  
- No payload execution, reverse shell, or lateral movement observed.  
- Timeline aligns with early-stage SOC detection for phishing events.

---

# Analyst Notes

- Focus: Initial Access detection and user-driven network activity.  
- Detection Artifact: Sysmon Event ID 3 provides primary evidence of the click.  
- SOC Monitoring: Track user-initiated outbound web traffic, correlate with email delivery time.

