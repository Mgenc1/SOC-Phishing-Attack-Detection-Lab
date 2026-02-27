\# 🛡 SOC Phishing Attack Detection Lab



This project demonstrates an \*\*end-to-end phishing attack simulation\*\* and analysis from a SOC perspective.  

The lab environment consists of \*\*attacker (Kali Linux)\*\*, \*\*victim (Windows 10)\*\*, and \*\*SIEM (Splunk)\*\* machines.



---



\## 📂 Repository Structure



\- `01-Architecture/` → Lab architecture and network diagram  

\- `02-Attack-Simulation/` → Phishing scenario and Gophish configuration  

\- `03-Log-Collection/` → Sysmon logs and Splunk forwarding  

\- `04-Detection-Analysis/` → Detection queries, IOC extraction, MITRE mapping  

\- `05-Incident-Timeline/` → Timeline of the incident  

\- `06-Impact-Response/` → Risk assessment and containment actions  

\- `07-Incident-Report/` → Professional incident report  

\- `screenshots/` → Screenshots and visual evidence  



---



\## 🌐 Lab Network Overview



\- \*\*Attacker (Kali Linux)\*\* – `192.168.1.106`  

\- \*\*Victim (Windows 10)\*\* – `192.168.1.108`  

\- \*\*SIEM (Splunk, Ubuntu Server)\*\* – `192.168.1.102`  



For the network setup and log flow, see the \[network diagram](01-Architecture/network-diagram.png).



---



\## 🔗 Important Links



\- \[Scenario Description](02-Attack-Simulation/scenario-description.md)  

\- \[Sysmon Configuration](03-Log-Collection/sysmon-configuration.md)  

\- \[Detection Logic \& MITRE Mapping](04-Detection-Analysis/detection-logic.md)  

\- \[Final Incident Report](07-Incident-Report/final-incident-report.md)  



---



\## 🎯 Project Objectives



1\. Create a realistic phishing scenario  

2\. Collect and analyze endpoint logs  

3\. Perform SOC-level detection and IOC extraction  

4\. Produce a professional incident report



---



> This lab serves as a \*\*practical portfolio project\*\* for SOC analysts.

