# Lab Overview – SOC Phishing Attack Detection

This document provides an overview of the **SOC Phishing Attack Detection Lab** architecture.  
The purpose of this lab is to simulate a real-world phishing attack in a controlled environment and demonstrate **SOC-level monitoring, detection, and analysis**.

---

## 🖥️ Lab Components

The lab consists of **three virtual machines**, each serving a specific role:

1. **Attacker Machine – Kali Linux**
   - Runs **GoPhish** to simulate phishing campaigns.
   - IP Address: `192.168.1.106`
   - Responsible for sending malicious emails and hosting phishing landing pages.

2. **Victim Machine – Windows 11**
   - Runs **Sysmon** and **Universal Forwarder** to generate and forward logs.
   - IP Address: `192.168.1.108`
   - Represents the end-user targeted by phishing attacks.

3. **SIEM – Ubuntu Server**
   - Runs **Splunk Enterprise** to collect, index, and visualize logs.
   - IP Address: `192.168.1.102`
   - Provides dashboards, alerts, and detection analysis.

---

## 🌐 Network Overview

The lab network is **isolated** and designed for safe simulation:

- Attacker communicates with Victim via email (SMTP) and web (HTTP/HTTPS)  
- Victim logs are forwarded to SIEM for detection and analysis  
- All traffic is internal; **no connection to the Internet** is required

You can view the lab network diagram here: [network-diagram.png](network-diagram.png)

---

## 📝 Lab Objectives

1. Simulate a realistic phishing attack scenario  
2. Monitor and analyze endpoint activity using Sysmon  
3. Collect and visualize logs in Splunk  
4. Map attack activities to the **MITRE ATT&CK framework**  
5. Generate a professional incident response report

---

> This lab is designed for **SOC analysts, cybersecurity students, and security enthusiasts** to practice end-to-end phishing detection and incident response.

