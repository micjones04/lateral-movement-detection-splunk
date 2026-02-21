# 🛡️ Lateral Movement Detection Using PsExec & Splunk

## 📌 Executive Summary
This project simulates a real-world lateral movement attack in an enterprise-style Active Directory lab and demonstrates how the activity can be detected, correlated, and investigated using Splunk.

The objective was to validate telemetry ingestion across multiple log sources and reconstruct attacker behavior using a structured SOC investigation workflow.

---

## 🎯 Objectives
- Simulate adversary lateral movement behavior
- Validate Windows and endpoint telemetry ingestion
- Correlate multi-source logs in a SIEM
- Develop an investigation methodology
- Identify detection opportunities

---

## 🧪 Lab Environment

| Component | Details |
|-----------|--------|
| SIEM | Splunk Enterprise (Free License) |
| Domain Controller | ADDC01 |
| Target Workstation | TARGET-PC |
| Attacker System | Kali Linux |
| Telemetry | Windows Security, Sysmon, Defender |

---

## ⚔️ Attack Scenario
A simulated attacker used **Impacket PsExec** to authenticate to a domain workstation and execute a remote service using administrative credentials.

This generated authentication, privilege assignment, execution artifacts, and endpoint detection telemetry.
<img width="975" height="211" alt="image" src="https://github.com/user-attachments/assets/4cd56443-3e75-41c1-8b65-4e0a837af14d" />

---

## 🔎 Key Detection Artifacts

| Event | Description |
|------|------------|
| 4624 | Successful network logon |
| 4672 | Privileged session assigned |
| 7045 | Remote service installed |
| Defender Alerts | Endpoint detection triggered |
<img width="975" height="730" alt="image" src="https://github.com/user-attachments/assets/82fbd311-7e56-46e5-adcf-caef7e2d57a7" />
<img width="461" height="323" alt="image" src="https://github.com/user-attachments/assets/e2d789dc-6d14-4e88-a6cd-1c43ee1cf32e" />

---

## 🧠 Investigation Workflow
1. Identify anomalous authentication  
2. Validate privileged session context  
3. Confirm execution artifact  
4. Correlate endpoint alerts  
5. Trace origin host  
<img width="975" height="723" alt="image" src="https://github.com/user-attachments/assets/a93cecc1-0bde-408a-9c01-b5946ba07f34" />

---

## 🛠 Skills Demonstrated
- SIEM log ingestion & validation  
- Windows event log analysis  
- Detection engineering mindset  
- Attack simulation & adversary emulation  
- Incident investigation workflow  

---

## 📂 Repository Structure
docs/         → Full investigation write-up  
screenshots/  → Splunk queries and evidence  
queries/      → SPL searches used in investigation  
detections/   → Detection logic and ideas  
---

## 🚀 Future Enhancements
- SPL detection rule creation  
- MITRE ATT&CK mapping  
- Investigation playbook  
- Additional attack simulations  

---

## 🧩 Lessons Learned
This lab reinforced the importance of correlating authentication telemetry with execution artifacts.  
It also highlighted how service creation events can provide high-confidence indicators of lateral movement.

---

## 🧠 Why This Matters
Lateral movement is a critical stage in real-world intrusions.  
This project demonstrates how multi-source telemetry can be correlated to detect attacker behavior with high confidence.

---

## 🧠 Key Takeaway
This project demonstrates the ability to design, execute, and investigate a realistic lateral movement scenario while validating detection coverage across multiple telemetry layers.
