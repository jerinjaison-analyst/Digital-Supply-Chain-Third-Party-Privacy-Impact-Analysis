# Third-Party Privacy Impact Assessment 

## Executive Summary
**Business Problem:**
A high-growth Fintech organization integrated over 20+ third-party processors (APIs/SDKs) to scale operations. This rapid expansion introduced significant "Shadow IT" risks, with sensitive customer data (PII/PCI) flowing to external servers without centralized oversight. Manual spreadsheet audits were insufficient to track the volume of 500+ daily data transfer logs.

**Solution Implemented:**
Designed and deployed an **Automated Risk Scoring Engine** in Microsoft Excel. The tool models the entire digital supply chain, automatically flags encryption failures against GDPR/SOC2 standards, and calculates a quantitative risk score for every data flow in real-time.

---

## Strategic Insights & Dashboard
*The Executive Dashboard serves as the primary artifact for C-Level security decision-making.*

Executive Dashboard <img width="1833" height="733" alt="Screenshot 2026-02-09 230529" src="https://github.com/user-attachments/assets/4e0834f0-fe62-4075-abaf-20b420624290" />


**Key Risk Indicators (KRIs):**
* **18% Compliance Failure Rate:** The audit revealed that nearly one-fifth of all data transfers involve "Restricted" data types moving without adequate encryption protocols.
* **Vendor Concentration Risk:** **Stripe** was identified as the single highest point of failure. Despite SOC2 compliance, the aggregate volume of financial data flowing to this single endpoint necessitates a dedicated Business Continuity Plan (BCP).
* **Cross-Border Data Risks:** Identified low-volume transfers to **Israel** and **Australia**. While currently low-risk, these require immediate review of Standard Contractual Clauses (SCCs) to ensure GDPR adequacy.

---

## Technical Architecture & Methodology

### 1. Automated Risk Logic (The Engine)
*Automated detection of security non-compliance using conditional logic.*

Risk Engine Logic  <img width="1906" height="889" alt="Screenshot 2026-02-10 171911" src="https://github.com/user-attachments/assets/287b5e61-3ac6-4f07-9bcc-9f025b4541cd" />


**Logic Configuration:**
* **Gap Analysis Module (Column J):** Utilized nested `IF/AND` functions to audit every row against a security matrix.
    * *Logic:* `IF(Data="Restricted" AND Encryption="None", "CRITICAL GAP", "COMPLIANT")`
* **Quantitative Scoring Model (Column K):** Implemented a weighted risk formula to prioritize remediation.
    * *Formula:* `(Asset Value * Vulnerability Factor) = Risk Score`
    * *Impact:* This ensures high-value assets (Biometrics) trigger higher alerts than low-value assets (Public info).

### 2. Data Simulation & Modeling
*Construction of a realistic "Big Data" environment for stress-testing.*


**Data Architecture:**
* **Simulation:** leveraged Excel randomization algorithms (`INDEX`, `MATCH`, `RANDBETWEEN`) to generate a dataset of **500 unique data flows**, mimicking live API logs.
* **Relational Schema:** The tool interconnects three distinct datasets:
    1.  **Vendor Inventory:** (Attributes: SOC2 Status, Server Geolocation).
    2.  **Risk Standards:** (Attributes: Data Sensitivity Weights).
    3.  **Data Map:** (The transactional ledger of all API calls).

**[The Full Excel Project File](https://1drv.ms/x/c/675045b6b1d41b99/IQAGllsuaVOxTZaO5U-tjHH8AROP3Zi0Mg5OybfJLmhOtGk?e=ezXmWZ)**

---

## Core Competencies Demonstrated

| Competency Area | Application in Project |
| :--- | :--- |
| **GRC Frameworks** | Applied GDPR (Article 32) and SOC2 principles to define logic checks. |
| **Data Analytics** | Transformed raw log data into actionable risk intelligence. |
| **Advanced Excel** | `VLOOKUP`, `INDEX/MATCH`, Pivot Tables, Conditional Formatting. |
| **Risk Modeling** | Developed a quantitative scoring model based on NIST guidelines. |

---

##  Author
**[Jerin Jaison T]**
* [LinkedIn Profile](https://www.linkedin.com/in/jerin-jaison-t)
