# 🛡 SOC Home Lab – Phishing Attack Simulation & Detection

## 📌 Project Overview
This lab demonstrates a **full SOC incident workflow** in a home lab phishing attack scenario.  
The objective is to **simulate, detect, analyze, and report malicious activity** using Sysmon, Splunk, and MITRE ATT&CK mapping.

The lab environment consists of three virtual machines:

- 🐉 **Kali Linux (Attacker – GoPhish)**  
- 🐧 **Ubuntu Server (SIEM – Splunk Enterprise)**  
- 🪟 **Windows 10 (Victim – Sysmon + Universal Forwarder)**  

---

## 📚 Full SOC Incident Workflow

1️⃣ **Scenario Creation** – Define realistic phishing attack scenario  
2️⃣ **Attack Execution** – Send phishing emails via GoPhish, capture victim interactions  
3️⃣ **Log Collection** – Sysmon logs collected, forwarded to Splunk  
4️⃣ **Detection & Analysis** – Use Splunk queries to detect suspicious activity  
5️⃣ **MITRE ATT&CK Mapping** – Map detected techniques to ATT&CK framework  
6️⃣ **IOC Extraction** – Extract IPs, processes, and network anomalies  
7️⃣ **Timeline Creation** – Document each stage from attack to detection  
8️⃣ **Impact Assessment** – Evaluate risks and potential damages  
9️⃣ **Containment & Recommendations** – Suggest mitigation and containment steps  
🔟 **Detection Engineering Notes** – Document detection rules and logic  
1️⃣1️⃣ **Lessons Learned** – Summarize key takeaways from the incident  
1️⃣2️⃣ **Executive Summary (Management Overview)** – High-level summary for stakeholders  

---

## Lab Architecture
The lab environment was built using VirtualBox and consists of:

- Kali Linux – Attacker machine  
- Windows 10 – Victim machine with Sysmon  
- Ubuntu Server – SIEM running Splunk Enterprise  

All logs from the Windows machine are forwarded to Splunk using the Universal Forwarder.  
See [network diagram](01-Architecture/network-diagram.png) for lab topology.

---

## 📂 Contents / Links

- [Scenario Creation & Attack Execution](02-Attack-Simulation/scenario-description.md)  
- [Log Collection](03-Log-Collection/sysmon-configuration.md)  
- [Detection & MITRE Mapping](04-Detection-Analysis/detection-logic.md)  
- [Incident Timeline](05-Incident-Timeline/timeline-analysis.md)  
- [Impact & Response](06-Impact-Response/impact-assessment.md)  
- [Final Incident Report](07-Incident-Report/final-incident-report.md)  

---

> This lab demonstrates a **realistic SOC incident workflow**, from phishing attack simulation to professional incident reporting, and is suitable for portfolio purposes.
