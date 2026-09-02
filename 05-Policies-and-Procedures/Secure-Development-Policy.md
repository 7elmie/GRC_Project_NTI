# Secure Development Policy

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-POL-006 |
| Annex A Controls | A.8.25, A.8.26, A.8.27, A.8.28, A.8.29, A.8.30, A.8.31, A.8.32, A.8.33 |
| Owner | Head of Engineering / CISO |
| Status | Approved |
| Version | 1.0 |
| Classification | Internal |

## 1. Purpose

Ensures information security is designed into FFG's software (core banking platform, payment gateway, mobile app) throughout the development lifecycle, addressing risks identified in RISK-001, RISK-009, and RISK-012.

## 2. Secure Development Lifecycle (A.8.25)

| Phase | Security Activity |
|---|---|
| Requirements | §Requirements — security/privacy requirements defined alongside functional requirements (A.8.26) |
| Design | Architecture Review Board review against secure architecture principles (A.8.27) — threat modeling for new/high-risk components |
| Build | Secure coding standard enforced (A.8.28); peer code review mandatory for all changes |
| Test | SAST on every build; DAST and penetration testing before major releases (A.8.29); Software Composition Analysis (SCA) for dependencies (planned rollout, ref. RISK-009) |
| Release | Deployment only via CI/CD pipeline with required gates passed; no direct production access for developers |
| Maintain | Vulnerability management and patch cycles per the Vulnerability Management Procedure |

## 3. §Requirements

Every new feature or system handling Restricted data must document: authentication/authorization requirements, data protection requirements (encryption, masking), logging requirements (excluding sensitive data — see FND-03), and abuse-case/threat considerations.

## 4. Secure Coding (A.8.28)

Developers follow the organization's secure coding standard (based on OWASP guidance), covering input validation, output encoding, parameterized queries, and secure error handling. Static analysis findings of High/Critical severity block merge to the main branch.

## 5. Security Testing (A.8.29)

- Automated SAST runs on every pull request.
- DAST and manual penetration testing performed at least annually and before major releases of internet-facing systems.
- Findings are risk-rated and tracked to closure per severity-based SLAs (Critical: 7 days, High: 30 days, Medium: 90 days).

## 6. Environment Separation (A.8.31)

Development, test/staging, and production environments are logically and, where feasible, physically separated, with distinct access controls. Production data is not used in test environments except in masked/tokenized form (A.8.33, see Data Classification and Handling Policy §Masking).

## 7. Change Management (A.8.32)

- All production changes go through the Change Advisory Board (CAB) process: proposed, reviewed, approved, tested, deployed, and post-implementation reviewed.
- Emergency changes follow an expedited path with mandatory post-hoc CAB review within 24 hours (remediation for FND/RISK-015 open item).

## 8. Outsourced Development (A.8.30)

Third-party/outsourced developers are contractually bound to this policy's standards (see Supplier Relationships Policy §Outsourced Dev) and their code is subject to the same review/testing gates as internal development.

## 9. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.0 | — | Head of Engineering | Approved |
