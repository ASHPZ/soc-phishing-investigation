# 🛡️ Phishing Alert Investigation: SOC Level 1

## 📝 Project Overview
This project is a simulated cybersecurity investigation conducted from the perspective of a **Level 1 Security Operations Center (SOC) Analyst**. The scenario involves responding to a phishing alert concerning a potentially malicious file downloaded by an employee.

## 🎯 Objective
To evaluate a **High-severity phishing alert** (Ticket ID: A-2703), investigate the email artifacts, analyze the attached file for malicious properties, and follow organizational procedures outlined in the **Phishing Incident Response Playbook**.

## 🔍 Investigation Steps
Based on the Phishing Playbook (Version 1.0), the following steps were executed:
1. **Receive Alert:** Initiated investigation for an alert indicating a possible malware download (SERVER-MAIL).
2. **Evaluate Alert:** Analyzed sender and receiver details. Discovered that the email contained grammatical errors and originated from a suspicious address outside the organization's IP pool.
3. **Attachment Analysis:** Identified a password-protected attachment named `bfsvc.exe`.
4. **Threat Intelligence:** Utilized VirusTotal to evaluate the file hash. The attachment was confirmed as malicious malware classified as **Trojan.Flag Pro/Fragtor**.
5. **Ticket Escalation:** Updated the alert ticket with findings and changed the status to **Escalated**, forwarding it to SOC Level 2 in accordance with Step 3.2 of the playbook.

## 🚨 Indicators of Compromise (IoCs)
| Type | Value | Note |
|---|---|---|
| **Sender Email** | `76tguyhh6tgftrt7tg.su` | Suspicious/temporary domain |
| **Sender IP** | `114.114.114.114` | Outside organizational pool |
| **File Name** | `bfsvc.exe` | Password-protected archive |
| **SHA256 Hash** | `54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b` | Identified as Trojan |

## 🛠️ Tools & Processes
* **Threat Intelligence:** VirusTotal
* **Documentation:** Alert Ticketing System
* **Procedures:** Phishing Incident Response Playbook

## 💡 Conclusion
The investigation successfully identified a malicious payload attempting to compromise the infrastructure. By adhering to the established SOC playbook, the threat was swiftly analyzed, documented, and escalated to Level 2 analysts for remediation.
