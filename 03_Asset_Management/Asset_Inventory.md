# NexaCore Information Asset Inventory (ISO 27001:2022 Cl. 5.9)

| Item | Details |
| :--- | :--- |
| **Document ID** | NX-AST-001 |
| **Last Updated** | March 2026 |
| **Owner** | IT Operations / DevOps Lead |

---

## 1. Classification Schema
Assets are classified based on the potential impact of their loss or compromise:

* **Restricted:** Most sensitive data/systems (e.g., Customer PII, Admin Credentials).
* **Confidential:** Proprietary data (e.g., AI Model weights, Source Code).
* **Internal:** General business data (e.g., Internal wikis, HR policies).
* **Public:** Information intended for external use (e.g., Marketing website).

---

## 2. Asset Register

### 2.1 Information & Data Assets
| Asset ID | Asset Name | Description | Format | Owner | Classification |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **NC-DAT-01** | Customer PII | Identity docs & Personal Info. | RDS/S3 | CTO | **Restricted** |
| **NC-DAT-02** | AI Model Weights | Proprietary NLP/OCR parameters. | S3 | Head of AI | **Confidential** |
| **NC-DAT-03** | Financial Records | Invoices and transaction logs. | RDS | Finance Mgr | **Restricted** |
| **NC-DAT-04** | Source Code | GitHub Repositories. | Digital | Head of Eng | **Confidential** |

### 2.2 Software & Cloud Assets
| Asset ID | Asset Name | Description | Environment | Owner | Classification |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **NC-SOF-01** | NexaCore SaaS Platform | Main FastAPI/React Application. | AWS EKS | DevOps Lead | **Confidential** |
| **NC-SOF-02** | Terraform Scripts | Infrastructure as Code (IaC). | GitHub | DevOps Lead | **Internal** |
| **NC-SOF-03** | AWS IAM Roles | Identity and Access Management. | AWS | Security Lead | **Restricted** |

### 2.3 Physical & Endpoint Assets
| Asset ID | Asset Name | Description | Location | Owner | Classification |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **NC-HW-01** | Corporate Laptops | Macbook/Windows developer machines. | Remote/Hybrid | IT Lead | **Internal** |
| **NC-HW-02** | Office Networking | Router, Firewall, Access Points. | Karachi HQ | IT Lead | **Internal** |

---

## 3. Asset Lifecycle Management
1.  **Onboarding:** All new assets must be tagged and assigned an owner upon procurement.
2.  **Maintenance:** Critical software assets (AWS EKS, RDS) are patched monthly.
3.  **Offboarding:** Upon employee exit, all local data on **NC-HW-01** must be wiped, and access to **NC-SOF-03** revoked within 24 hours.
4.  **Disposal:** Physical media containing **Restricted** data must be shredded or cryptographically erased.

---
**Approved By:**
*Security Lead & IT Manager*
