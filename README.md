# 🛡 SOC-Phishing-Attack-Detection-Home Lab

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

[SOC-Phishing-Attack-Detection-Lab](SOC-Phishing-Attack-Detection-Lab)

[01-Architecture](SOC-Phishing-Attack-Detection-Lab/01-Architecture/)
- [01.01 Lab Overview](01-Architecture/01.01-lab-overview.md)
- [01.02 Network Diagram](01-Architecture/01.02-network-diagram.png)

[02-Attack-Simulation](02-Attack-Simulation/)
- [02.01 Scenario Description](02-Attack-Simulation/02.01-scenario-description.md)
- [02.02 Gophish Configuration](02-Attack-Simulation/02.02-gophish-configuration.md)
- [02.03 Phishing Email Template](02-Attack-Simulation/02.03-phishing-email-template.md)

[03-Log-Collection](03-Log-Collection/)
- [03.01 Sysmon Configuration](03-Log-Collection/03.01-sysmon-configuration.md)
- [03.02 Windows Event Analysis](03-Log-Collection/03.02-windows-event-analysis.md)
- [03.03 Log Forwarding to Splunk](03-Log-Collection/03.03-log-forwarding-to-splunk.md)

[04-Detection-Analysis](04-Detection-Analysis/)
- [04.01 Splunk Search Queries](04-Detection-Analysis/04.01-splunk-search-queries.md)
- [04.02 Detection Logic](04-Detection-Analysis/04.02-detection-logic.md)
- [04.03 IOC Extraction](04-Detection-Analysis/04.03-ioc-extraction.md)
- [04.04 MITRE Mapping](04-Detection-Analysis/04.04-mitre-mapping.md)

[05-Incident-Timeline](05-Incident-Timeline/)
- [Timeline Analysis](05-Incident-Timeline/timeline-analysis.md)

[06-Impact-Response](06-Impact-Response/)
- [06.01 Impact Assessment](06-Impact-Response/06.01-impact-assessment.md)
- [06.02 Containment Actions](06-Impact-Response/06.02-containment-actions.md)
- [06.03 Lessons Learned](06-Impact-Response/06.03-lessons-learned.md)

[07-Incident-Report](07-Incident-Report/)
- [Final Incident Report](07-Incident-Report/final-incident-report.md)

[08-Screenshots](08-Screenshots/)
- [VirtualBox Lab Overview](08-Screenshots/1.virtualbox-lab-overview.png)
- [Ubuntu Server - Splunk](08-Screenshots/2.ubuntu-server-splunk.png)
- [Kali - Gophish](08-Screenshots/3.kali-gophish.png)
- [Thunderbird Mail](08-Screenshots/4.thunderbird-mail.png)
- [Phishing Page](08-Screenshots/5.phishing-page.png)
- [Event 3 - Splunk Web](08-Screenshots/6.event3-web.png)
---

> This lab demonstrates a **realistic SOC incident workflow**, from phishing attack simulation to professional incident reporting, and is suitable for portfolio purposes.
