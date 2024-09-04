---
layout: default
---

[🏠 home](../)

<h1 style="text-align: center;">Controls and Compliance Assessment</h1>

[Project reference](https://www.coursera.org/learn/manage-security-risks?specialization=google-cybersecurity) 

# Scenario

This is based on a fictional company:

Botium Toys is a small U.S. business that develops and sells toys. The business has a single physical location, which serves as their main office, a storefront, and warehouse for their products. However, Botium Toy’s online presence has grown, attracting customers in the U.S. and abroad. As a result, their information technology (IT) department is under increasing pressure to support their online market worldwide. 

The manager of the IT department has decided that an internal IT audit needs to be conducted. She expresses concerns about not having a solidified plan of action to ensure business continuity and compliance, as the business grows. She believes an internal audit can help better secure the company’s infrastructure and help them identify and mitigate potential risks, threats, or vulnerabilities to critical assets. The manager is also interested in ensuring that they comply with regulations related to internally processing and accepting online payments and conducting business in the European Union (E.U.).   

The IT manager starts by implementing the National Institute of Standards and Technology Cybersecurity Framework (NIST CSF), establishing an audit scope and goals, listing assets currently managed by the IT department, and completing a risk assessment. The goal of the audit is to provide an overview of the risks and/or fines that the company might experience due to the current state of their security posture.

Your task is to review the IT manager’s scope, goals, and risk assessment report. Then, perform an internal audit by completing a controls and compliance checklist.

## Scope and goals of the audit

### Scope 
The scope of this audit is defined as the entire security program at Botium Toys. This includes their assets like employee equipment and devices, their internal network, and their systems. You will need to review the assets Botium Toys has and the controls and compliance practices they have in place.

### Goals
Assess existing assets and complete the controls and compliance checklist to determine which controls and compliance best practices need to be implemented to  improve Botium Toys’ security posture.

### Current assets
Assets managed by the IT Department include: 
* On-premises equipment for in-office business needs
* Employee equipment: end-user devices (desktops/laptops, smartphones), remote workstations, headsets, cables, keyboards, mice, docking stations, surveillance cameras, etc.
* Storefront products available for retail sale on site and online; stored in the company’s adjoining warehouse
* Management of systems, software, and services: accounting, telecommunication, database, security, ecommerce, and inventory management
* Internet access
* Internal network
* Data retention and storage
* Legacy system maintenance: end-of-life systems that require human monitoring 

### Risk assessment

#### Risk description
Currently, there is inadequate management of assets. Additionally, Botium Toys does not have all of the proper controls in place and may not be fully compliant with U.S. and international regulations and standards. 

#### Control best practices
The first of the five functions of the NIST CSF is Identify. Botium Toys will need to dedicate resources to identify assets so they can appropriately manage them. Additionally, they will need to classify existing assets and determine the impact of the loss of existing assets, including systems, on business continuity.

#### Risk score
On a scale of 1 to 10, the risk score is 8, which is fairly high. This is due to a lack of controls and adherence to compliance best practices.

#### Additional comments
The potential impact from the loss of an asset is rated as medium because the IT department does not know which assets would be at risk. The risk to assets or fines from governing bodies is high because Botium Toys does not have all of the necessary controls in place and is not fully adhering to best practices related to compliance regulations that keep critical data private/secure. Review the following bullet points for specific details:

#### Additional Info 

In Cybersecurity, control types can be classified in three ways: 
1. Administrative/Managerial controls
2. Technical controls
3. Physical/Operational controls

Control types (providing defense and protecting assets) include, but are not limited to:
1. Preventative (preventing an incident from occurring in the first place)
2. Corrective (restoring an asset after an incident)
3. Detective (Determining whether an incident has occurred or is in progress)
4. Deterrent (Discouraging attacks)

## Controls Assessment Checklist

Does Botium Toys currently have this control in place? 

| Yes / No | Control | Note |
|:---:|-------|-------------------|
| No | Least Privilege | All employees have access to data including customer credit card information. A least privilege policy needs to be implemented to avoid possible breaches. |
| No | Disaster Recovery Plan | There is no plan for handling the disaster. Implementing this ensures business continuity. |
| Yes* | Password policies | Password policy exists but its requirements are nominal and not in line with current minimum password complexity requirements. |
| No | Separation of Duties |  |
| Yes | Firewall | |
| No | Intrusion Detection System (IDS) | Required to identify possible intrusions by threat actors. |
| No | Backups | Unprepared for a breach. Implementation of a backup plan, such as incremental, full, or partial is required. |
| Yes | Antivirus software |  |
| Yes* | Manual monitoring, maintenance, and intervention for legacy systems | Legacy systems are monitored and maintained but there is no regular schedule in place for these tasks, and intervention methods are unclear. |
| No | Encryption | Required for confidentiality of data. |
| Yes | Locks (Storefront) | |
| Yes | CCTV |  |
| Yes | Fire detection |  |

**has condition*

## Compliance Checklist
Does Botium Toys currently adhere to this compliance best practice? 

* Payment Card Industry Data Security Standard (PCI DSS)

| Yes/ No | Best Practice | Note |
|:---:|-------|-------------------|
| No | Only authorized users have access to customers’ credit card information. | At the moment, all employees have access to data.  |
| No | Credit card information is stored, accepted, processed, and transmitted internally, in a secure environment. |  |
| No | Implement data encryption procedures to better secure credit card transaction touchpoints and data. |  | 
| No | Adopt secure password management policies. |  | 

**has condition*

* GDPR
  
| Yes/ No | Best Practice | Note |
|:---:|-------|-------------------|
| No* | E.U. customers’ data is kept private/secured. | All employees have access to customer data. |
| Yes | There is a plan in place to notify E.U. customers within 72 hours if their data is compromised/there is a breach.| |
| No | Ensure data is properly classified and inventoried. | |
| Yes | Enforce privacy policies, procedures, and processes to properly document and maintain data. | |

**has condition*

* System and Organizations Controls 

| Yes/ No | Best Practice | Note |
|:---:|-------|-------------------|
| No | User access policies are established | Employees have access to internally stored data which means the access policy has not been applied. |
| No | Sensitive data (PII/SPII) is confidential/private. | Employees have access to data which means the access to sensitive data is not confidential. |
| Yes | Data integrity ensures the data is consistent, complete, accurate, and has been validated. |  | 
| No | Data is available to authorized users | Currently, all employees have access to all of the data. |

## Recommendations (optional)

Botium Toys's security practice is far from the expected best practices and security standards. It lacks protection of confidentiality of sensitive information. The following implementations are required:
1. Least privilege
2. Disaster recovery plan
3. Password policies
4. Encryption
5. Password management system

To address gaps in compliance, Botium needs to implement and establish policies that can address the above. Botium also needs to update its assets to identify additional controls as soon as possible to improve its security practices.
