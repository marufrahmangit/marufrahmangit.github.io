---
layout: default
---

[🏠 home](../)

<h1 style="text-align: center;">Risk Assessment and Prioritization in a Commercial Bank</h1>

# Scenario
You've joined a new cybersecurity team at a commercial bank. The team is conducting a risk assessment of the bank's current operational environment. As part of the assessment, they are creating a risk register to help them focus on securing the most vulnerable risks.

A risk register is a central record of potential risks to an organization's assets, information systems, and data. Security teams commonly use risk registers when conducting a risk assessment.

[Project Reference](https://www.coursera.org/learn/assets-threats-and-vulnerabilities)

Your supervisor asks you to evaluate a set of risks that the cybersecurity team has recorded in the risk register. For each risk, you will first determine how likely that risk is to occur. Then, you will determine how severely that risk may impact the bank. Finally, you will calculate a score for the severity of that risk. You will then compare scores across all risks so your team can determine how to prioritize their attention for each risk.

# Operational environment:
The bank is located in a coastal area with low crime rates. Many people and systems handle the bank's data—100 on-premise employees and 20 remote employees. The customer base of the bank includes 2,000 individual accounts and 200 commercial accounts. The bank's services are marketed by a professional sports team and ten local businesses in the community. There are strict financial regulations that require the bank to secure their data and funds, like having enough cash available each day to meet Federal Reserve requirements.

| Asset                     | Risk(s)                     | Description                                                  | Likelihood | Severity | Priority |  
|---------------------------|-----------------------------|--------------------------------------------------------------|------------|----------|----------|
| Funds | Business email compromise   | An employee is tricked into sharing confidential information. |     2      |     3     |     6    |
|  | Compromised user database  | Customer data is poorly encrypted.  |     2       |     3     |   6   |
|     |Financial records leak |A database server of backed up data is publicly accessible.  |      1      |     3     |     3     |
|                      | Theft |The bank's safe is left unlocked. |      1      |    3      |     3     |
|    |Supply chain disruption  | Delivery delays due to natural disasters. |     1       |     3     |     3     |

**Notes:** How are security events possible considering the risks the asset faces in its operating environment?
Doing business with other companies might increase the risks to data since it presents other avenues for the information to be compromised. The risk of theft is important, but might not be a priority because the bank is in an area with low crime rates.

**Asset:** The asset at risk of being harmed, damaged, or stolen.

**Risk(s):** A potential risk to the organization's information systems and data.

**Description:** A vulnerability that might lead to a security incident.

**Likelihood:** Score from 1-3 of the chances of a vulnerability being exploited. 
- A 1 means there's a low likelihood.
- A 2 means there's a moderate likelihood.
- A 3 means there's a high likelihood.

**Severity:** Score from 1-3 of the potential damage the threat would cause to the business. 
- A 1 means a low severity impact.
- A 2 is a moderate severity impact.
- A 3 is a high severity impact.

**Priority:** How quickly a risk should be addressed to avoid the potential incident. Use the following formula to calculate the overall score: `Likelihood x Impact Severity = Risk`.

## Sample Risk Matrix:
![image](https://github.com/user-attachments/assets/cbdc5c33-c9f4-441c-9f2a-d4230a67c724)
