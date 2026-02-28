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

# SOC-Phishing-Attack-Detection-Lab

Contents
Introduction (Not: Buraya ana README başlığınıza bir çapa linki verebilirsiniz)

01-Architecture

1. Lab Overview

2. Network Diagram

02-Attack-Simulation

1. Scenario Description

2. Gophish Configuration

3. Phishing Email Template

03-Log-Collection

1. Sysmon Configuration

2. Windows Event Analysis

3. Log Forwarding to Splunk

04-Detection-Analysis

1. Splunk Search Queries

2. Detection Logic

3. IOC Extraction

4. MITRE Mapping

05-Incident-Timeline

1. Timeline Analysis

06-Impact-Response

1. Impact Assessment

2. Containment Actions

3. Lessons Learned

07-Incident-Report

1. Final Incident Report

08-Screenshots

1. VirtualBox Lab Overview

2. Ubuntu Server - Splunk

3. Kali - Gophish

4. Thunderbird Mail

5. Phishing Page

6. Event 3 - Splunk Web
---

> This lab demonstrates a **realistic SOC incident workflow**, from phishing attack simulation to professional incident reporting, and is suitable for portfolio purposes.
