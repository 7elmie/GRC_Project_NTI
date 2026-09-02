# Internal Audit Programme

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-PRO-002 |
| ISO 27001:2022 Clause | 9.2.1 |
| Owner | Head of Internal Audit |
| Status | Approved |
| Version | 1.0 |
| Classification | Internal |

## 1. Purpose

Establishes the programme for planning, conducting, reporting, and maintaining internal ISMS audits, including frequency, methods, responsibilities, and reporting, per Clause 9.2.1.

## 2. Audit Programme Principles

The programme is designed with regard to:

- The **importance** of the processes concerned (e.g., core banking, payment processing, and access management audited more frequently than lower-risk support functions)
- **Changes affecting the organization** (new systems, regulatory changes, prior audit results)
- Results of **previous audits**

## 3. Three-Year Audit Cycle (Full Annex A + Clause 4–10 Coverage)

| Year | Focus Areas | Rationale |
|---|---|---|
| Year 1 (current) | Full-scope audit: ISMS clauses 4–10, all Annex A themes, with emphasis on access control (A.5.15–5.18, A.8.2–8.5), cryptography (A.8.24), logging/monitoring (A.8.15–8.16), and supplier management (A.5.19–5.23) | Highest-risk domains per Risk Register; first certification-readiness audit |
| Year 2 | Follow-up on Year 1 corrective actions; deep-dive: secure development lifecycle (A.8.25–8.34), network security (A.8.20–8.23), business continuity (A.5.29–5.30, A.8.14) | Verify closure of open items; DR failover retest |
| Year 3 | Follow-up on Year 2 CAPAs; deep-dive: physical security (A.7), people controls (A.6), supplier/cloud (A.5.19–5.23, A.8.9) | Full-cycle closure ahead of recertification audit |

Each annual cycle also includes: (a) a rolling sample of all Annex A controls not otherwise deep-dived that year, and (b) 100% follow-up verification of prior open corrective actions.

## 4. Audit Methods

- Document review (policies, procedures, records)
- Interviews with process/control owners
- Technical verification (configuration review, sampling of logs, access review testing)
- Walkthroughs of key processes (e.g., onboarding/offboarding, incident response, change management)
- Sampling of evidence (e.g., sample of access requests, sample of patched vulnerabilities)

## 5. Roles and Independence

| Role | Responsibility |
|---|---|
| Head of Internal Audit | Owns the programme; reports directly to CEO/Audit Committee |
| Lead Auditor (per cycle) | Plans and executes the specific audit; must be independent of the area audited |
| Auditee / Process Owner | Provides access to evidence, personnel, and systems; responds to findings |
| CISO | Receives findings; owns overall CAPA tracking (but does not audit their own function — a peer or external auditor covers ISMS governance controls owned by the CISO) |

## 6. Audit Criteria

Each audit is conducted against: ISO/IEC 27001:2022 (Clauses 4–10 and Annex A), the current Statement of Applicability, FFG's own ISMS policies/procedures, and applicable legal/regulatory/contractual requirements (per `03-SoA-and-AnnexA` control 5.31 reference).

## 7. Reporting

- Audit findings are reported in the Internal Audit Findings Report for each cycle (this folder).
- A summary is presented to the CISO immediately (closing meeting) and formally to top management at the next Management Review or sooner for Critical findings.
- The Head of Internal Audit maintains a CAPA tracker with status visible to the CISO and top management.

## 8. Programme Review

This programme is reviewed annually and adjusted based on prior audit results, risk register changes, and organizational change, consistent with Clause 9.2.1.

## 9. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | — | Internal Audit | Initial draft |
| 1.0 | — | Head of Internal Audit | Approved |
