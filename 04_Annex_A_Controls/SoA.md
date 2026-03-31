# Statement of Applicability (SoA) - ISO 27001:2022
> **Project:** NexaCore SaaS Platform Implementation  
> **Standard:** ISO/IEC 27001:2022 Annex A Controls

| Item | Details |
| :--- | :--- |
| **Document ID** | NX-SOA-001 |
| **Version** | 1.0 |
| **Status** | Draft for Internal Audit |
| **Last Updated** | March 2026 |

---

## 1. Introduction
This Statement of Applicability (SoA) identifies the controls from ISO 27001:2022 Annex A that are relevant to NexaCore Cloud Solutions (Pvt.) Ltd. 

## 2. Control Selection Summary

| Control ID | Control Name | Status | Justification for Selection / Exclusion |
| :--- | :--- | :--- | :--- |
| **A.5.1** | Policies for Information Security | **Applied** | Essential for defining the governance framework for the AI SaaS platform. |
| **A.5.15** | Control of Supplier Relations | **Applied** | Critical for managing risks associated with AWS, Stripe, and Twilio. |
| **A.5.30** | ICT Readiness for Business Continuity | **Applied** | Necessary to ensure AI document processing remains available during AWS regional outages. |
| **A.7.4** | Physical Security Monitoring | **Excluded** | NexaCore is 100% cloud-native; physical security is managed by AWS (Shared Responsibility). |
| **A.8.3** | Access Rights | **Applied** | Required to enforce MFA and Least Privilege for DevOps and Engineering teams. |
| **A.8.10** | Information Deletion | **Applied** | Required for GDPR compliance (Right to Erasure) and managing SaaS data lifecycle. |
| **A.8.12** | Data Leakage Prevention (DLP) | **Applied** | Critical to prevent the unauthorized export of proprietary AI model weights and customer PII. |
| **A.8.24** | Use of Cryptography | **Applied** | Mandatory for protecting data at rest in S3/RDS and data in transit via TLS. |
| **A.8.28** | Secure Coding | **Applied** | Essential for the FastAPI/React development lifecycle and preventing OWASP Top 10 vulnerabilities. |
| **A.8.32** | Change Management | **Applied** | Required for controlling updates to the AI inference engine and production infrastructure via CI/CD. |

---

## 3. Implementation Status Overview
* **Total Controls Evaluated:** 93 (ISO 27001:2022 Framework)
* **Total Controls Applied:** 82 (Following 10 above are the most critical controls displayed for proof)
* **Total Controls Excluded:** 11 (Primarily physical/facility-related controls)

## 4. Maintenance of the SoA
This document is reviewed annually or upon significant changes to the NexaCore infrastructure (e.g., migrating from AWS to a multi-cloud environment or opening a physical data center).

---
**Approved By:**
*Security Lead & Chief Technology Officer (CTO)*
