# ISMS Roles, Responsibilities and Authorities

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-DOC-004 |
| ISO 27001:2022 Clause | 5.3 |
| Owner | CISO |
| Status | Approved |
| Version | 1.0 |
| Classification | Internal |

## 1. Purpose

Assigns and communicates responsibilities and authorities for roles relevant to information security, per Clause 5.3, ensuring the ISMS conforms to ISO/IEC 27001:2022 requirements and reports on ISMS performance to top management.

## 2. ISMS Governance Structure

```
CEO (Top Management)
  └── ISMS Steering Committee (quarterly)
        ├── CISO (ISMS Owner)
        │     ├── Information Security Team (Engineering, SOC, GRC)
        │     ├── IAM Lead
        │     └── Vendor Risk Manager
        ├── Head of IT Operations
        ├── Head of Engineering
        ├── Head of HR
        └── Internal Audit Function (independent reporting line to CEO/Audit Committee)
```

## 3. RACI Matrix (Key ISMS Activities)

| Activity | CEO | CISO | Steering Committee | Internal Audit | Process/Asset Owners |
|---|---|---|---|---|---|
| Approve Information Security Policy | A | R | C | I | I |
| Approve ISMS Scope | A | R | C | I | I |
| Risk assessment execution | I | A | I | I | R |
| Risk acceptance (above defined threshold) | A | R | C | I | C |
| Statement of Applicability approval | A | R | C | I | I |
| Internal audit programme approval | A | C | I | R | I |
| Internal audit execution | I | I | I | R | C |
| Corrective action ownership | I | A | I | C | R |
| Management review | R | R | C | I | I |
| Incident response (major incident) | I | A | I | I | R |
| Security awareness training | I | A | I | I | R (HR delivers) |

*R = Responsible, A = Accountable, C = Consulted, I = Informed*

## 4. Role Descriptions

### 4.1 Top Management (CEO)
- Ultimate accountability for the ISMS and its outcomes.
- Approves the Information Security Policy and ISMS scope.
- Chairs or delegates chairing of the annual Management Review.
- Ensures resources are available for the ISMS.

### 4.2 CISO
- Owns day-to-day operation and continual improvement of the ISMS.
- Reports ISMS performance, risk posture, and audit results to top management.
- Has authority to mandate remediation of identified nonconformities within agreed timelines.
- Approves the Risk Register and Statement of Applicability, subject to top management sign-off for risk acceptances above the defined threshold.

### 4.3 Internal Audit Function
- Independent of the areas it audits (reports functionally to CEO or an Audit Committee, not to the CISO, to preserve independence per Clause 9.2.2).
- Plans and executes the internal audit programme (`04-Internal-Audit-Execution`).
- Reports findings directly to top management and the CISO.

### 4.4 Process/Asset Owners
- Implement and operate controls relevant to their systems/processes.
- Provide evidence during internal/external audits.
- Own remediation of findings related to their area.

### 4.5 All Personnel
- Comply with the Information Security Policy and supporting policies.
- Report suspected security events/incidents without delay (see Incident Management Policy).

## 5. Segregation of Duties

The following segregations are mandated to avoid conflicts of interest:

- The Internal Audit function does not report to the CISO.
- Individuals who design/implement a control do not solely approve its own audit evidence.
- Risk acceptance above the defined threshold requires CEO/top management approval, not the CISO alone.

## 6. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | — | ISMS Team | Initial draft |
| 1.0 | — | CISO | Approved |
