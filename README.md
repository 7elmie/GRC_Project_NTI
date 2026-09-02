# Team 4 — ISO 27001:2022 / ISO 27002 Internal Audit Documentation & Compliance Project

**NTI GRC Graduation Project**

## Scenario

A company already has an Information Security Management System (ISMS) and claims ISO/IEC 27001:2022 compliance. This project performs a full internal audit and produces the complete ISMS documentation set needed to test — and support — that claim, at a senior GRC practitioner level.

To keep every document internally consistent, all deliverables reference a single fictional client:

> **Felex Financial Group (FFG)** — a mid-sized digital banking and payments company (~450 employees) operating a core banking platform, a payment gateway, corporate IT, and hybrid on-prem/cloud infrastructure.

## Audit Outcome (Summary)

The internal audit found FFG's ISMS to be **substantially implemented and operating**, with a complete policy framework, an approved Statement of Applicability covering all 93 Annex A:2022 controls, an active risk management process, and functioning governance. It also identified **5 Major Nonconformities** and **6 Minor Nonconformities**, concentrated in the operational execution of previously identified high-risk treatments (authentication hardening, data-leakage prevention, and disaster-recovery testing). Full detail is in `04-Internal-Audit-Execution/Internal-Audit-Findings-Report.md`.

## Repository Structure

| Folder | Contents | Key ISO 27001:2022 Clauses |
|---|---|---|
| [`01-ISMS-Mandatory-Documents`](./01-ISMS-Mandatory-Documents) | ISMS Scope, Information Security Policy, Objectives, Roles/RACI, Document Control Procedure, Management Review Procedure | 4.3, 5.2, 5.3, 6.2, 7.5, 9.3 |
| [`02-Risk-Management`](./02-Risk-Management) | Risk Assessment & Treatment Methodology, Risk Register (18 assessed risks), Risk Treatment Plan | 6.1.2, 6.1.3, 8.2, 8.3 |
| [`03-SoA-and-AnnexA`](./03-SoA-and-AnnexA) | Statement of Applicability — all 93 Annex A:2022 controls, applicability justification, and implementation status | 6.1.3(d) |
| [`04-Internal-Audit-Execution`](./04-Internal-Audit-Execution) | Internal Audit Programme, Audit Plan & Checklist, Findings Report (nonconformities, root cause, corrective actions) | 9.2, 10.1, 10.2 |
| [`05-Policies-and-Procedures`](./05-Policies-and-Procedures) | 9 supporting topic-specific policies (Access Control, Data Classification, Incident Management, Supplier Relationships, Secure Development, Physical Security, Business Continuity, Cryptography, Acceptable Use) | Annex A (various) |

## How the Documents Connect

```
Information Security Objectives (01)
        │
        ▼
   Risk Register (02) ──► Risk Treatment Plan (02)
        │                          │
        ▼                          ▼
Statement of Applicability (03) ◄──┘
        │
        ▼
Internal Audit Checklist & Findings (04)
        │
        ▼
Corrective Actions ──► referenced back into Risk Register (02) & SoA (03)

Policies (05) implement the Annex A controls declared applicable in (03)
```

Every risk, control, finding, and policy carries cross-reference IDs (e.g., `RISK-003`, `FND-01`, `A.8.5`) so an auditor — or a grader — can trace a requirement from the top-level policy all the way through to audit evidence and back.

## Suggested Reading Order

1. `01-ISMS-Mandatory-Documents/ISMS-Scope-Statement.md` — establishes what's in scope
2. `01-ISMS-Mandatory-Documents/Information-Security-Policy.md` — top-level commitment
3. `02-Risk-Management/Risk-Register.md` — what could go wrong
4. `03-SoA-and-AnnexA/Statement-of-Applicability.md` — which controls address it, and their status
5. `04-Internal-Audit-Execution/Internal-Audit-Findings-Report.md` — what the audit actually found
6. `05-Policies-and-Procedures/` — the detailed rules behind each control area

## Document Conventions

- **Status**: Draft / Under Review / Approved
- **Classification**: Internal (all ISMS documents in this project are treated as Internal unless stated otherwise)
- **Owner**: assigned by role, not individual name
- **Review cycle**: Annually, or on significant change
- Full conventions are defined in `01-ISMS-Mandatory-Documents/Document-Control-Procedure.md`

## Status

Documentation set complete for the current audit cycle (IA-2026-01). Open corrective actions are tracked in `04-Internal-Audit-Execution/Internal-Audit-Findings-Report.md` §4 and are due for follow-up verification per `04-Internal-Audit-Execution/Internal-Audit-Programme.md`.