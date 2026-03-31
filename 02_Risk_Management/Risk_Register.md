# NexaCore Risk Register (ISO 27001:2022 Cl. 6.1.2)

| Item | Details |
| :--- | :--- |
| **Document ID** | NX-RISK-001 |
| **Last Updated** | March 2026 |
| **Review Cycle** | Bi-Annual |

---

## 1. Risk Assessment Methodology
Risks are calculated using a **Qualitative $5 \times 5$ Matrix** where:
* **Inherent Risk Score** = Likelihood (1-5) $\times$ Impact (1-5).
* **Likelihood:** 1 (Rare) to 5 (Almost Certain).
* **Impact:** 1 (Insignificant) to 5 (Catastrophic).

## 2. Active Risk Register

| Risk ID | Threat Scenario | Asset Affected | Likelihood | Impact | Inherent Score | Mitigation Strategy (Control) | Residual Risk |
| :--- | :--- | :--- | :---: | :---: | :---: | :--- | :---: |
| **R-101** | Unauthorized S3 bucket access due to misconfiguration. | Customer PII | 3 | 5 | **15 (High)** | Enforce AWS "Block Public Access" & use IAM Roles for EC2/Lambda. | Low |
| **R-102** | Prompt Injection or Data Poisoning of AI models. | OCR/NLP Engine | 3 | 4 | **12 (Med)** | Implement Input Validation Layer & sanitize data before inference. | Med |
| **R-103** | Credential leakage (API Keys) in GitHub Repositories. | Source Code | 4 | 4 | **16 (High)** | Enable GitHub Secret Scanning & use AWS Secrets Manager. | Low |
| **R-104** | Insider threat: Excessive admin privileges for DevOps. | All Cloud Assets | 2 | 5 | **10 (Med)** | Implement Just-In-Time (JIT) access & Quarterly Access Reviews. | Low |
| **R-105** | Service outage in AWS Middle East (me-central-1). | SaaS Availability | 2 | 5 | **10 (Med)** | Multi-Region failover (EU-Central) and automated DB backups. | Low |

## 3. Risk Treatment Plan (RTP) Summary

1. **Avoid:** Terminate any service that processes highly sensitive data without encryption capabilities.
2. **Mitigate:** Deploy technical controls (MFA, Encryption, WAF) to lower likelihood/impact.
3. **Transfer:** Maintain Cyber Insurance and rely on AWS Service Level Agreements (SLAs).
4. **Accept:** Acknowledge low-level operational risks that do not impact PII or AI Intellectual Property.

---
**Approved By:**
*Security Lead & CTO*
