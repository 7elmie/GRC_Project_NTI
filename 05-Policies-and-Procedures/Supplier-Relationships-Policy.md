# Supplier Relationships Policy

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-POL-005 |
| Annex A Controls | A.5.19, A.5.20, A.5.21, A.5.22, A.5.23 |
| Owner | CISO / Vendor Risk Manager |
| Status | Approved |
| Version | 1.0 |
| Classification | Internal |

## 1. Purpose

Governs security requirements for suppliers, cloud providers, and the ICT supply chain, given FFG's dependency on its cloud hosting provider and other critical vendors (ref. RISK-006).

## 2. Supplier Risk Tiering

| Tier | Criteria | Due Diligence |
|---|---|---|
| Critical | Access to Restricted data, or hosts in-scope production systems (e.g., cloud provider, payment processor) | Full security questionnaire, SOC 2/ISO 27001 report review, contract security addendum, annual reassessment |
| High | Access to Confidential data or supporting systems | Security questionnaire, evidence review every 2 years |
| Standard | No access to sensitive data or in-scope systems | Standard procurement terms |

## 3. §Onboarding

- Before contract signature, Critical/High-tier suppliers complete a security questionnaire and provide evidence of their control environment (e.g., SOC 2 Type II, ISO 27001 certificate).
- Findings are logged in the Vendor Risk Register with any required remediation as a contract condition.

## 4. Contractual Requirements (A.5.20)

Contracts with Critical/High-tier suppliers include: security requirements proportionate to data sensitivity, breach notification obligations (timeframe defined), right-to-audit clause, data handling/return/deletion obligations at contract termination, and subcontractor (subprocessor) disclosure requirements.

## 5. ICT Supply Chain (A.5.21)

- Software dependencies (open-source and commercial) are subject to the Secure Development Policy's SCA requirements.
- Critical suppliers must disclose their own subprocessors; FFG maps the subprocessor chain for its most critical dependencies (cloud provider, payment processor).

## 6. Cloud Services (A.5.23)

- Use of cloud services follows the shared-responsibility model: FFG is responsible for identity, data, and configuration security within the cloud provider's environment; the provider is responsible for physical/infrastructure security, evidenced by their compliance certifications.
- New cloud services/accounts require CISO approval and inclusion in the CSPM monitoring scope before production use.

## 7. §Outsourced Dev

- Outsourced/contracted development work must follow FFG's Secure Development Policy, including code review and security testing gates, regardless of where development occurs.
- IP and confidentiality terms are included in all outsourced development contracts.

## 8. Ongoing Monitoring (A.5.22)

- Critical suppliers are reassessed annually (or on material change); performance and security incidents involving suppliers are tracked and factored into renewal decisions.
- Material changes to a supplier's service (e.g., new subprocessor, ownership change) trigger a re-review.

## 9. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.0 | — | CISO | Approved |
