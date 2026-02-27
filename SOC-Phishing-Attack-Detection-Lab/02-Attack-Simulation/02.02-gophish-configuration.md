# Gophish Campaign Setup

This document explains the configuration of the phishing campaign in the SOC Phishing Attack Lab using **Gophish**.  
It focuses on **campaign creation, email template setup, and testing**.

## 1. Campaign Configuration

- **Campaign Name:** SOC Phishing Lab Campaign  
- **Landing Page URL:** `http://192.168.1.106` (phishing page hosted on Kali)  
- **Template:** See `email-template.md`  
- **Target:** Windows user (`192.168.1.108`)  

> Note: All activities are internal to the lab environment; no external systems are affected.

## 2. Sending Profile

- Use lab-configured SMTP or default Gophish profile  
- From Address: `lab-test-account@gmail.com`  
- Immediate launch for realistic simulation  

## 3. Testing & Verification

1. Send test email to target machine (Windows/Thunderbird)  
2. Click the link to verify redirection to the phishing page  
3. Confirm Sysmon captures the network connection (Event ID 3)  

## 4. References

- For installation and detailed setup, see [Gophish Official Guide](https://github.com/gophish/gophish)

