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

---

## 🔎 Key Detection Artifacts

| Event | Description |
|------|------------|
| 4624 | Successful network logon |
| 4672 | Privileged session assigned |
| 7045 | Remote service installed |
| Defender Alerts | Endpoint detection triggered |

---

## 🧠 Investigation Workflow
1. Identify anomalous authentication  
2. Validate privileged session context  
3. Confirm execution artifact  
4. Correlate endpoint alerts  
5. Trace origin host  

---

## 🛠 Skills Demonstrated
- SIEM log ingestion & validation  
- Windows event log analysis  
- Detection engineering mindset  
- Attack simulation & adversary emulation  
- Incident investigation workflow  

---

## 📂 Repository Structure
