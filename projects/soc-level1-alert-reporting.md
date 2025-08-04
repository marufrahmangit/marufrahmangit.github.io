---
layout: default
---

[🏠 home](../)

<h1 style="text-align: center;">SOC L1 Alert Reporting, Escalation, and Communication</h1>

[Project reference](https://tryhackme.com/room/socl1alertreporting)

# Scenario
During or after alert triage, L1 analysts may be uncertain about how to classify the alert, requiring senior support or information from the system owner. Also, L1 may deal with real cyberattacks and breaches that need immediate attention and remediation actions. This project covers these cases by introducing three new terms: alert reporting, escalation, and communication.

## Investigate the SOC dashboard to find which user email leaked the sensitive document
<img width="1816" height="695" alt="image" src="https://github.com/user-attachments/assets/eb5899ef-92d4-4cc4-8968-17788ba5fb20" />

The user email that leaked the sensitive document: m.boslan@tryhackme.thm

## Investigate the "sender" of the suspicious, likely phishing email
<img width="1810" height="465" alt="image" src="https://github.com/user-attachments/assets/818ddd29-c7ed-4099-aaeb-c708984ae460" />

The "sender" of the suspicious, likely phishing email: support@microsoft.com

## Reporting
### Phishing Email Incident Report
**Report**: The email to e.huffman@tryhackme.thm was spoofed using a fake Microsoft domain and failed both SPF and DKIM checks. It contained phishing language and a .rar attachment named REPORT.rar, which may contain a malicious payload. User interaction is not yet confirmed, but delivery and spoofing indicators justify classifying this as a phishing attempt requiring sandbox analysis and mailbox sweep.

<img width="824" height="569" alt="image" src="https://github.com/user-attachments/assets/bf73784c-b26a-4b06-b9be-9ed1b0f113d1" />

## Escalate to L2
Escalate to L2 Analyst and set the status to In Progress for further analysis.
<img width="823" height="570" alt="image" src="https://github.com/user-attachments/assets/f98e16e6-af3d-47b5-b6d5-e4244e5e6ba7" />

##  Investigation and escalation of a new alert in queue
<img width="1812" height="682" alt="image" src="https://github.com/user-attachments/assets/fd20e2c5-2d55-4383-b31e-7a2dfac23451" />
**Severity**: High 
**Detection Time**: March 27, 2025 at 19:56 (UTC)  
**Status**: In Progress 
**Verdict**: True Positive
**Report**: Multiple domain discovery commands (e.g., whoami, net group, nltest) were executed on DMZ-MSEXCHANGE-2013 under the SYSTEM account. These commands were run via cmd.exe, which was spawned by a suspicious binary (revshell.exe) located in the public user directory. The parent process of the reverse shell was w3wp.exe (IIS), indicating likely initial access via a web server vulnerability. This behavior is consistent with post-exploitation activity, not legitimate administrative use, and strongly suggests the host has been compromised. Immediate containment and forensic analysis are recommended.
