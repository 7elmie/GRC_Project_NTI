# Access Control Policy

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-POL-001 |
| Annex A Controls | A.5.15, A.5.16, A.5.17, A.5.18, A.8.2, A.8.3, A.8.4, A.8.5, A.8.18 |
| Owner | CISO |
| Status | Approved |
| Version | 1.0 |
| Classification | Internal |

## 1. Purpose

Governs how access to MFG's information systems and data is granted, managed, reviewed, and revoked, on the principle of least privilege and need-to-know.

## 2. Access Control Principles

- **Least privilege**: users are granted the minimum access required for their role.
- **Need-to-know**: access to information is restricted to those who require it for legitimate business purposes.
- **Segregation of duties**: no individual has end-to-end control over a sensitive process without independent oversight (see `01-ISMS-Mandatory-Documents/Roles-Responsibilities-Authorities.md` §5).
- **Default deny**: access is denied by default and explicitly granted, not the reverse.

## 3. Identity Management (A.5.16)

- Every user, system, and service account has a unique identifier; shared/generic accounts are prohibited except where technically unavoidable and formally risk-accepted.
- Identity lifecycle (joiner/mover/leaver) is managed via the HR-to-IAM process.

## 4. §Authentication

- Multi-factor authentication (MFA) is required for all access to in-scope systems, including remote access, administrative interfaces, and — per this policy's requirement — **service and legacy accounts** (see FND-01 for current implementation gap and remediation).
- Privileged and executive accounts require hardware-token (phishing-resistant) MFA (target control; see FND-02).
- Passwords, where used, must meet the organizational complexity/length standard and are never shared or reused across systems.
- Authentication information (credentials, tokens, keys) is stored and transmitted only in encrypted form.

## 5. §Least Privilege — Provisioning and Review

- Access requests require manager and system-owner approval before provisioning.
- **User Access Reviews (UAR)** are performed quarterly for all in-scope systems; overdue items beyond 30 days are escalated to the CISO (ref. OBJ-04).
- Privileged access (A.8.2) is granted only where justified, time-bound where feasible, and subject to enhanced logging.
- Access to source code (A.8.4) is restricted to authorized engineering personnel via repository permissions, with all changes attributable to an individual.
- Privileged utility programs (A.8.18) capable of overriding system/application controls are restricted to authorized administrators and independently logged.

## 6. Revocation

- Access is revoked immediately upon termination or role change that removes the need for access (target SLA: within 4 hours of the HR-triggered offboarding event — see RISK-007 remediation).
- Access for contractors/third parties expires automatically at contract end date where technically supported.

## 7. Exceptions

Any deviation from this policy (e.g., a legacy system unable to support MFA) must be formally risk-accepted per `02-Risk-Management/Risk-Assessment-and-Treatment-Methodology.md` §3, with a compensating control and review date.

## 8. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.0 | — | CISO | Approved |
