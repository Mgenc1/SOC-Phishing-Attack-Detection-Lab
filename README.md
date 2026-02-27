# 🛡 SOC Home Lab – Phishing Attack Simulation & Detection

## 📌 Project Overview
This project simulates a **real-world phishing attack** in a controlled SOC home lab environment.  
The objective is to **detect, analyze, and report malicious activity** using Sysmon and Splunk, while mapping findings to the **MITRE ATT&CK framework**.

The lab environment consists of three virtual machines:

- 🐉 **Kali Linux (Attacker – GoPhish)**  
- 🐧 **Ubuntu Server (SIEM – Splunk Enterprise)**  
- 🪟 **Windows 10 (Victim – Sysmon + Universal Forwarder)**  

---

## 📚 Contents

- [Introduction](#introduction)  
- [Lab Architecture](#lab-architecture)  
- [Attack Scenario](#attack-scenario)  
- [Log Collection & Analysis](#log-collection--analysis)  
- [MITRE ATT&CK Mapping](#mitre-attack-mapping)  
- [Indicators of Compromise (IOCs)](#indicators-of-compromise-iocs)  
- [Incident Timeline](#incident-timeline)  
- [Final Incident Report](#final-incident-report)  

---

## Introduction
This document provides a step-by-step simulation of a phishing attack scenario.  
The goal is to demonstrate **SOC-level detection**, **log analysis**, and **incident reporting** capabilities.

---

## Lab Architecture
The lab environment was built using VirtualBox and consists of:

- **Kali Linux** – Attacker machine  
- **Windows 10** – Victim machine with Sysmon & Universal Forwarder  
- **Ubuntu Server** – SIEM running Splunk Enterprise  

All logs from the Windows machine are forwarded to Splunk for real-time monitoring and analysis.  
For the full network overview, see the [network diagram](01-Architecture/network-diagram.png).

---

## Attack Scenario
A phishing email was sent to the victim machine using **GoPhish**.  
The victim interacted with the malicious content, which triggered suspicious activities logged by **Sysmon**:

- Process creation  
- Network connections  
- File modifications  

---

## Log Collection & Analysis
- **Log Source:** Sysmon (Windows 10)  
- **SIEM:** Splunk Enterprise  
- **Event IDs analyzed:** 1 (Process Creation), 3 (Network Connection), 11 (File Creation)  
- **Detection:** Custom SPL queries in Splunk were used to detect abnormal behavior and potential threats.

---

## MITRE ATT&CK Mapping
The observed techniques were mapped to MITRE ATT&CK:

- **T1566.001 – Phishing**  
- **T1059.001 – PowerShell**  
- **T1071 – Application Layer Protocol**  

---

## Indicators of Compromise (IOCs)
Extracted IOCs include:

- Malicious IP addresses  
- Suspicious process execution  
- Abnormal network connections  

---

## Incident Timeline
A detailed attack timeline was created, documenting each stage from initial access to detection.  

- Email delivery → User click → Malicious payload execution → Sysmon log capture → Splunk alert → IOC extraction  

---

## Final Incident Report
A professional incident report was prepared including:

- Executive Summary  
- Technical Analysis  
- MITRE Mapping  
- IOC List  
- Remediation Recommendations  

---

> This lab serves as a **practical portfolio project** for SOC analysts and demonstrates real-world phishing attack detection and incident response workflow.
