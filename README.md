# NexaCore-ISO27001-Compliance
Full ISO 27001 pre-audit simulation for a cloud SaaS entity, focusing on Annex A controls for cloud-native environments.

OBJECTIVE: Establishing a formal Information Security Management System (ISMS) for an AI-powered SaaS platform.
# Project Overview
NexaCore Cloud Solutions (Pvt.) Ltd. is a privately held technology company headquartered in Karachi, Pakistan. Founded in 2021, the company operates in the Software-as-a-Service (SaaS) domain, specializing in AI-powered document processing and workflow automation solutions for small and medium-sized enterprises (SMEs) and mid-market organizations.

The company employs approximately 120 personnel distributed across engineering, product, operations, and support functions. NexaCore serves clients across Pakistan, the Gulf Cooperation Council (GCC) region, and select European markets.

The organization is currently in a scale-up phase, transitioning from early-stage product-market fit to enterprise-grade service delivery, with increasing emphasis on security, compliance, and operational maturity.
## Key Deliverables
Risk Management: Developed a $5 \times 5$ Risk Matrix identifying 15+ high-impact cloud risks.

Compliance Mapping: Mapped existing AWS technical controls to Annex A (ISO 27001:2022).

Policy Framework: Authored 5 core security policies tailored for a hybrid DevOps workforce.
## Technical Environment
Infrastructure: AWS (EC2, S3, RDS, Lambda)

CI/CD: GitHub Actions (Secure coding workflows)

Tools Used: Excel (Risk Register), LucidChart (Network Diagrams), Markdown (Policies).

---

### 1. Risk Assessment & Treatment (ISO 27001:2022 Cl. 6.1.2)
I developed a $5 \times 5$ Risk Matrix to quantify threats to the AI processing pipeline.

| Risk ID | Threat Scenario | Likelihood | Impact | Score | Treatment |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **R-01** | Unauthorized S3 Access (PII Leak) | 3 | 5 | **15** | **Mitigate:** IAM Role Hardening |
| **R-02** | Prompt Injection / AI Model Bias | 2 | 4 | **8** | **Mitigate:** Input Validation Layer |
| **R-03** | Credential Leakage in CI/CD | 3 | 4 | **12** | **Mitigate:** GitHub Secret Scanning |

---

### 2. Gap Analysis (Annex A Mapping)
A detailed audit of the current environment against ISO controls.

| Control Area | Current State | Identified Gap | Priority |
| :--- | :--- | :--- | :--- |
| **A.5.15** | Use of AWS/Stripe | No formal Vendor Risk Assessment | High |
| **A.8.10** | Manual data deletion | No automated Data Retention Policy | Medium |
| **A.8.3** | Loose IAM permissions | Lack of Quarterly Access Reviews | High |

---

### 3. Policy Framework (Governance)
I authored the following enterprise-level policies (Available in `/01_Governance_Policies`):
* **Information Security Policy (ISP):** The foundational "憲法" (Constitution) of the ISMS.
* **Access Control Policy:** Enforcing Principle of Least Privilege (PoLP) and MFA.
* **Secure Development Policy:** Integrating security into the SDLC and AI training phases.

---

## Audit Simulation & Remediation Roadmap
To prepare for **Stage 1 Certification**, I established a 90-day roadmap:
1.  **Phase 1 (Days 1-30):** Policy Approval & Global MFA Enforcement.
2.  **Phase 2 (Days 31-60):** Asset Inventory Finalization & Technical Vulnerability Scanning.
3.  **Phase 3 (Days 61-90):** Internal Audit & Management Review Meeting.

---

## Skills Demonstrated
* **Standards:** ISO 27001:2022, NIST CSF, GDPR.
* **Risk Management:** Qualitative Risk Analysis, Treatment Plans.
* **Cloud Security:** AWS IAM, VPC Security Groups, S3 Encryption.
* **Documentation:** Policy Writing, Statement of Applicability (SoA) drafting.

---

## Repository Structure
* `01_Governance_Policies/`: Formal PDF versions of security policies.
* `02_Risk_Management/`: The master Risk Register and Heat Map.
* `03_Asset_Management/`: Inventory of Hardware, Software, and Information assets.
* `04_Annex_A_Controls/`: The Statement of Applicability (SoA).
* `05_Audit_Evidence/`: Evidence logs (e.g., sample IAM policies, backup logs).

---
**Contact:** Muhammad Usman | www.linkedin.com/in/muhammad-usman-abu-bakar-a9283b263 


