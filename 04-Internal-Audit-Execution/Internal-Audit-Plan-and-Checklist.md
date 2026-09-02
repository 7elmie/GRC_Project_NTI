# Internal Audit Plan and Checklist — Year 1 (Full-Scope Certification-Readiness Audit)

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-REC-003 |
| ISO 27001:2022 Clause | 9.2.2 |
| Audit ID | IA-2026-01 |
| Lead Auditor |  — Internal Audit Function (independent of CISO reporting line) |
| Audit Dates |  |
| Audit Type | Full-scope internal audit — Clauses 4–10 + sampled Annex A controls |
| Status | Complete — see Findings Report |

## 1. Audit Objectives

1. Determine whether the ISMS conforms to FFG's own requirements and to ISO/IEC 27001:2022.
2. Determine whether the ISMS is effectively implemented and maintained.
3. Test FFG's existing claim of ISO 27001:2022 compliance against objective evidence.

## 2. Audit Scope

Full ISMS scope as defined in `01-ISMS-Mandatory-Documents/ISMS-Scope-Statement.md`: Core Banking Platform, Payment Gateway, Corporate IT, Cloud Environments, and supporting business functions.

## 3. Audit Criteria

ISO/IEC 27001:2022 Clauses 4–10; Annex A controls per the current Statement of Applicability; FFG's internal ISMS policies/procedures.

## 4. Schedule

| Day | Activity |
|---|---|
| Day 1 AM | Opening meeting; document review (Clauses 4–7) |
| Day 1 PM | Interviews — CISO, IAM Lead, HR |
| Day 2 AM | Technical verification — access control sampling, logging/monitoring, cryptography (A.8.15, A.8.16, A.8.24) |
| Day 2 PM | Technical verification — network segmentation, change management, supplier oversight |
| Day 3 AM | Clause 8–10 review (operational planning, risk treatment execution, prior corrective actions, management review) |
| Day 3 PM | Closing meeting — preliminary findings presented to CISO |

## 5. Checklist — Clauses 4–10 (Management System)

| Clause | Audit Question | Evidence Reviewed | Result | Comments |
|---|---|---|---|---|
| 4.1/4.2 | Are external/internal issues and interested party requirements documented and current? | Context register | Conforming | Reviewed and current |
| 4.3 | Is the ISMS scope documented, justified, and approved? | ISMS Scope Statement | Conforming | Exclusions justified |
| 5.1/5.2 | Is the Information Security Policy approved by top management and communicated? | Policy doc, intranet publication log | Conforming | Approved and published |
| 5.3 | Are roles/responsibilities/authorities assigned and communicated? | RACI document, org chart | Conforming | — |
| 6.1.2/6.1.3 | Is there a documented, consistently applied risk methodology, and is it followed? | Methodology doc, Risk Register, sample risk assessments | Conforming | Methodology applied consistently across sampled risks |
| 6.2 | Are information security objectives measurable and tracked? | Objectives doc, quarterly Steering Committee minutes | Conforming | OBJ-01 through OBJ-07 tracked |
| 7.1/7.2 | Are resources and competence adequate and evidenced? | Training records, staffing plan | Minor Nonconformity | Training completion below 95% target in Customer Support (linked A.6.3) |
| 7.4 | Is internal/external communication relevant to the ISMS defined? | Communication plan | Conforming | — |
| 7.5 | Is documented information controlled per the Document Control Procedure? | Repository review, version history | Conforming | Git-based version control functioning as designed |
| 8.1–8.3 | Is operational planning/control, risk assessment, and risk treatment being executed as planned? | Risk Treatment Plan status tracker | Major Nonconformity | Multiple High/Critical treatment actions past target date (see Findings Report FND-01) |
| 9.1 | Is monitoring/measurement of ISMS performance occurring and are results used? | SOC metrics, KPI dashboards | Conforming | — |
| 9.2 | Is the internal audit programme being executed as planned, with independence maintained? | This audit itself; prior audit history | Conforming | First full-cycle audit; independence confirmed |
| 9.3 | Has a management review occurred with all required inputs/outputs? | Management review minutes | Minor Nonconformity | Prior management review did not formally document risk treatment plan status as an input (see FND-05) |
| 10.1 | Are nonconformities from prior periods tracked to closure with root cause analysis? | CAPA tracker | Minor Nonconformity | Two prior informal findings lack documented root cause analysis (see FND-06) |
| 10.2 | Is there a functioning continual improvement process? | Steering Committee minutes, objective revisions | Conforming | — |

## 6. Checklist — Sampled Annex A Controls (Highest-Risk Domains)

| Control | Audit Question | Evidence Reviewed | Result | Comments |
|---|---|---|---|---|
| A.5.17/A.8.5 | Is MFA enforced for all account types, including service/legacy accounts? | IAM configuration export, sample of 20 service accounts | Major Nonconformity | 6 of 20 sampled legacy service accounts lack MFA/strong auth (see FND-01, ties to RISK-003) |
| A.8.2 | Are privileged accounts subject to enhanced authentication controls? | PAM configuration, exec account sample | Major Nonconformity | Hardware-token MFA not yet deployed for privileged/exec accounts (see FND-02, ties to RISK-018) |
| A.8.15/A.8.12 | Is sensitive data (PAN) excluded from application logs? | Log sample from 5 services | Major Nonconformity | PAN observed unredacted in logs of 1 of 5 sampled services (see FND-03, ties to RISK-002) |
| A.8.20/A.8.22 | Is the corporate network segmented from payment/banking systems? | Network diagrams, firewall rule review | Minor Nonconformity | Core payment/banking segments isolated; corporate VLAN segmentation incomplete (see FND-04, ties to RISK-013) |
| A.8.24 | Is cryptographic key rotation performed per policy? | KMS rotation logs, legacy system key age check | Minor Nonconformity | One legacy encryption service last rotated >12 months ago (ties to RISK-014) |
| A.5.23/A.8.9 | Are cloud configurations continuously monitored for misconfiguration? | CSPM tool coverage report | Minor Nonconformity | CSPM not yet deployed to all cloud accounts (ties to RISK-004) |
| A.5.30 | Has DR/BC readiness been tested under realistic conditions? | Last DR test report | Major Nonconformity | Full DR failover not tested in 18 months (ties to RISK-017) |
| A.6.5/A.5.16 | Is access revoked promptly upon termination? | Sample of 10 terminations, access removal timestamps | Minor Nonconformity | 2 of 10 sampled terminations had access removed >24h after last working day (ties to RISK-007) |
| A.8.28/A.8.29 | Is secure coding enforced and verified before release? | SAST results, sample of 3 recent releases | Minor Nonconformity | SCA not yet integrated into CI/CD; one identified injection-risk module not yet remediated (ties to RISK-001, RISK-009) |

## 7. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.0 | — | Lead Auditor | Final audit plan and checklist for IA-2026-01 |
