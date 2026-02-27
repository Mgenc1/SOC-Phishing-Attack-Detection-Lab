# Phishing Attack Scenario Description

This document describes the phishing attack scenario simulated in the SOC Phishing Attack Detection Lab.

The purpose of this scenario is to replicate a realistic credential harvesting attack and analyze it from a SOC perspective.

---

## 1. Scenario Overview

An attacker operating from an internal machine (Kali Linux) launches a phishing campaign targeting a Windows user within the same isolated lab network.

The attacker sends a malicious email containing a password reset request.  
The email includes a link that redirects the victim to a fake login page hosted on the attacker’s system.

Once the victim clicks the link, network activity and endpoint logs are generated and forwarded to the SIEM for analysis.

---

## 2. Attack Objective

The objective of the attacker is to:

- Trick the victim into clicking a malicious link  
- Redirect the victim to a phishing landing page  
- Capture credentials (credential harvesting simulation)  
- Establish observable indicators for detection  

From a defensive perspective, the goal is to:

- Detect suspicious outbound connections  
- Identify phishing-related behavior  
- Correlate endpoint logs with network activity  
- Build a complete incident timeline  

---

## 3. Attack Flow Summary

1. Attacker creates phishing campaign using Gophish  
2. Email is delivered to the victim’s mailbox (Thunderbird)  
3. Victim clicks the malicious link  
4. Browser connects to attacker-controlled IP address  
5. Sysmon logs the network connection (Event ID 3)  
6. Logs are forwarded to Splunk  
7. SOC analysis begins  

---

## 4. Attack Characteristics

- **Attack Type:** Phishing (Credential Harvesting)  
- **Initial Access Vector:** Malicious Email  
- **User Interaction Required:** Yes  
- **Payload Type:** Web-based phishing page  
- **Network Communication:** Internal HTTP connection  

---

## 5. Detection Perspective

From a SOC analyst’s point of view, this scenario creates multiple detection opportunities:

- Suspicious email activity  
- Outbound connection to unusual internal host  
- Browser-initiated network traffic  
- Possible credential submission events  

These artifacts allow the analyst to reconstruct the full incident lifecycle.

---

## 6. Lab Scope

This attack simulation is conducted entirely within an isolated lab environment for educational and defensive training purposes.  

No external systems or real users are involved.
