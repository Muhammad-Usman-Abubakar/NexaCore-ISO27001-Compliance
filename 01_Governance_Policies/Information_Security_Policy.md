# Information Security Policy (ISP) - NexaCore Cloud Solutions

| Item | Details |
| :--- | :--- |
| **Document ID** | NX-POL-001 |
| **Version** | 1.0 |
| **Classification** | Internal |
| **Effective Date** | March 2026 |
| **Approval** | Chief Technology Officer (CTO) |

---

## 1. Purpose
The purpose of this policy is to provide the high-level governance framework for the Information Security Management System (ISMS) at NexaCore. It ensures the **Confidentiality, Integrity, and Availability (CIA)** of customer document data, AI models, and cloud infrastructure.

## 2. Scope
This policy applies to all NexaCore employees, contractors, and third-party partners. It covers all information assets within the NexaCore SaaS platform hosted on **Amazon Web Services (AWS)** and all development activities within the GitHub environment.

## 3. Information Security Objectives
NexaCore is committed to:
* Protecting Customer PII and financial data from unauthorized access.
* Ensuring 99.9% availability of the AI Document Processing engine.
* Maintaining compliance with **ISO 27001:2022**, GDPR, and regional GCC data regulations.
* Minimizing security incidents through continuous risk assessment.

## 4. Policy Statements

### 4.1 Access Control (Annex A 8.3)
* Access to production environments (AWS/EKS) is granted based on the **Principle of Least Privilege (PoLP)**.
* Multi-Factor Authentication (MFA) is mandatory for all administrative and developer accounts.
* Quarterly access reviews must be conducted by the Security Lead.

### 4.2 Data Protection & Encryption (Annex A 8.24)
* All sensitive data (PII) must be encrypted at rest using **AES-256**.
* All data in transit must be protected using **TLS 1.2** or higher.
* Proprietary AI model weights must be stored in restricted S3 buckets with logging enabled.

### 4.3 Secure Development (Annex A 8.28)
* Security must be integrated into the SDLC (Software Development Life Cycle).
* Automated secret scanning (GitHub Actions) must be active on all repositories to prevent credential leakage.
* Code reviews are mandatory before merging to the `main` branch.

### 4.4 Asset Management (Annex A 5.9)
* An up-to-date inventory of all hardware, software, and information assets must be maintained.
* All assets must be classified (e.g., Public, Internal, Confidential, Restricted).

### 4.5 Incident Management (Annex A 5.24)
* All employees are required to report suspected security weaknesses or incidents to the Security Lead immediately.
* A documented Incident Response Plan (IRP) must be tested annually.

## 5. Compliance and Enforcement
Failure to comply with this policy may result in disciplinary action, including termination of employment or contract. NexaCore reserves the right to monitor all systems for compliance with these standards.

---
**Approved By:**
*NexaCore Executive Leadership Team*
