---
layout: default
---

[🏠 home](../)

<h1 style="text-align: center;">SOC L1 Alert Reporting</h1>

[Project reference](https://tryhackme.com/room/socl1alertreporting)

# Scenario
During or after alert triage, L1 analysts may be uncertain about how to classify the alert, requiring senior support or information from the system owner. Also, L1 may deal with real cyberattacks and breaches that need immediate attention and remediation actions. This project covers these cases by introducing three new terms: alert reporting, escalation, and communication.

## Investigate the SOC dashboard to find which user email leaked the sensitive document
<img width="1816" height="695" alt="image" src="https://github.com/user-attachments/assets/eb5899ef-92d4-4cc4-8968-17788ba5fb20" />

The user email that leaked the sensitive document: m.boslan@tryhackme.thm

## Investigate the "sender" of the suspicious, likely phishing email
<img width="1810" height="465" alt="image" src="https://github.com/user-attachments/assets/818ddd29-c7ed-4099-aaeb-c708984ae460" />

The "sender" of the suspicious, likely phishing email: support@microsoft.com

## Using the Five Ws template, write a report to escalate to L2
### Phishing Email Incident Report
<img width="830" height="565" alt="image" src="https://github.com/user-attachments/assets/6378eb5b-71ab-4e27-a875-db61cd778692" />

The email to e.huffman@tryhackme.thm was spoofed using a fake Microsoft domain and failed both SPF and DKIM checks. It contained phishing language and a .rar attachment named REPORT.rar, which may contain a malicious payload. User interaction is not yet confirmed, but delivery and spoofing indicators justify classifying this as a phishing attempt requiring sandbox analysis and mailbox sweep.


