---
layout: default
---

[🏠 home](../)

<h1 style="text-align: center;">SOC L1 Alert Reporting</h1>

[Project reference](https://tryhackme.com/room/socl1alertreporting)

# Scenario
During or after alert triage, L1 analysts may be uncertain about how to classify the alert, requiring senior support or information from the system owner. Also, L1 may deal with real cyberattacks and breaches that need immediate attention and remediation actions. This project covers these cases by introducing three new terms: alert reporting, escalation, and communication.

# Tasks
## Investigate the SOC dashboard to find which user email leaked the sensitive document
<img width="1816" height="695" alt="image" src="https://github.com/user-attachments/assets/eb5899ef-92d4-4cc4-8968-17788ba5fb20" />
The user email that leaked the sensitive document: m.boslan@tryhackme.thm

## Investigate the "sender" of the suspicious, likely phishing email
<img width="1810" height="465" alt="image" src="https://github.com/user-attachments/assets/818ddd29-c7ed-4099-aaeb-c708984ae460" />
The "sender" of the suspicious, likely phishing email: support@microsoft.com

## Using the Five Ws template, write a report to escalate to L2

### Phishing Email Incident Report

**Alert Title**: Email Marked as Phishing after Delivery  
**Severity**: Medium  
**Detection Time**: March 27, 2025 at 19:25 (UTC)  
**Status**: Awaiting Action  
**Verdict**: **Confirmed Phishing Attempt**

---

### Who

- **Sender**: Spoofed identity – *Microsoft Support* `<support@microsoft.com>`
- **Recipient**: Eddie Huffman, IT Manager – `<e.huffman@tryhackme.thm>`

---

### What

An email impersonating Microsoft Support was **delivered successfully** and **later classified as phishing** by automated analysis. The email used urgent language and included a suspicious compressed attachment named `REPORT.rar`.

**Subject**: *Important Update: Microsoft Teams Pricing Increase*  
**Body Keywords**:
- "600% price increase"
- "urgent notice"
- "download the report"
- "read the details"

The email **did not contain embedded URLs**, but did include a potentially malicious file attachment: `REPORT.rar`.

---

### When

- **Detection Timestamp**: March 27, 2025 at 19:25 UTC  
- **Email Delivery Time**: Presumably within minutes prior to detection (exact timestamp should be retrieved from email logs)  
- **Incident Status**: Ongoing – pending user or SOC action

---

### Where

- **Target Device/User**: Eddie Huffman’s corporate email account – domain: `tryhackme.thm`
- **Originating IP / Email Infrastructure**:
  - **SPF Check**: Fail
  - **DKIM Check**: Fail

> _Note: Full email header analysis needed to identify source IP/domain and delivery infrastructure._

---

### Why (Analysis and Final Verdict)

This alert qualifies as a **confirmed phishing attempt**, based on the following indicators:

1. **Spoofed Sender**: Impersonates Microsoft using a generic support address (`support@microsoft.com`) without authentication.
2. **Social Engineering Language**: Uses emotionally triggering phrases such as “600% price increase” and “urgent notice.”
3. **Suspicious Attachment**: `.rar` file attachment is a known phishing and malware delivery method.
4. **Post-Delivery Flagging**: Indicates potential evasion of initial email gateway filtering.
5. **Authentication Failures**: Failing both SPF and DKIM checks suggests spoofed origin.

---

### Recommended Actions

1. **Quarantine** the email from Eddie Huffman’s inbox and scan for additional internal recipients.
2. **Analyze `REPORT.rar`** in a sandbox environment to identify any malicious behavior or phishing lure.
3. **Search Email Logs** to determine scope of exposure within the organization.
4. **Block Sender Domain/IP** at the email gateway.
5. **Notify Eddie Huffman** and reinforce phishing awareness procedures.
6. **Review and Enhance Email Filtering Rules**, especially for spoofing and known-brand impersonations.

---

