---

# Final Incident Report – Phishing Click Simulation

This document provides a comprehensive summary of the SOC Home Lab phishing simulation, consolidating all investigation, detection, impact, containment, and lessons learned. The objective is to produce a single reference report for SOC review and documentation.

---

1️. Executive Summary

* Phishing email delivered via Gophish.
* User clicked malicious link at 02/26/2026 11:35:10 PM.
* No payload execution, reverse shell, or lateral movement observed.
* Outbound connection to attacker-controlled lab machine detected and contained.
* SOC team implemented immediate containment and monitoring actions.

---

2️. Timeline of Events

| Time (PM) | EventCode | Event Type                  | Process / Action           | Notes                                     |
| --------- | --------- | --------------------------- | -------------------------- | ----------------------------------------- |
| 11:34:36  | 1         | Process Creation            | MpSigStub.exe              | Windows update/malware protection process |
| 11:35:10  | 3         | Network Connection Detected | msedge.exe → 192.168.1.106 | Phishing link click detected              |
| 11:36:15  | 5         | Process Termination         | dllhost.exe                | Normal process termination                |

**Key Takeaways:**

* User-driven interaction confirmed via Sysmon Event ID 3.
* No malicious execution observed.
* Timeline validated SOC detection capability.

---

3️. IOC Summary

| IOC Type         | Value                  | Source Event   |
| ---------------- | ---------------------- | -------------- |
| Attacker IP      | 192.168.1.106          | Sysmon Event 3 |
| Phishing URL     | /?rid=TWUdkmw          | Network Log    |
| Destination Port | 80 / 443               | Sysmon Event 3 |
| Process Image    | msedge.exe             | Sysmon Event 3 |
| Source Host      | 192.168.1.108          | Sysmon         |
| Hash (Demo)      | SHA256 (MpSigStub.exe) | Sysmon Event 1 |

---

4️. Impact Assessment

* Risk Level: Low – Medium
* User workstation and browser processes were the only impacted assets.
* Network exposure limited to observed HTTP click traffic.
* Operational impact minimal in lab environment.

---

5️. Containment Actions

* Workstation isolated and network traffic restricted.
* Outbound connection to attacker IP blocked at host and network firewall.
* SOC monitored browser and user processes.
* Temporary SIEM alerting rules implemented for unusual outbound HTTP connections.
* User notified and guided on phishing awareness.

---

6️. Lessons Learned

* Early detection via endpoint logging is effective.
* SOC detection rules updated to monitor browser outbound connections.
* Regular phishing simulations improve user readiness and SOC response.
* Continuous monitoring, documentation, and user training are essential.

---

7️. Recommendations

* Maintain enhanced logging for all workstations.
* Implement automated alerts for unusual outbound network traffic.
* Conduct periodic phishing awareness training.
* Review SOC processes and update incident response playbooks based on lab observations.

---

**End of Final Incident Report**
