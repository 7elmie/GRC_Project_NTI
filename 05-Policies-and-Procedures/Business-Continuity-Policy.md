# Business Continuity Policy

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-POL-008 |
| Annex A Controls | A.5.29, A.5.30, A.8.14 |
| Owner | BCP/DR Lead / CISO |
| Status | Approved |
| Version | 1.0 |
| Classification | Internal |

## 1. Purpose

Ensures information security is maintained during disruption and that ICT services can be restored within defined targets, addressing RISK-008 (backup/ransomware) and RISK-017 (untested DR).

## 2. Business Continuity Objectives

| System | RTO (Recovery Time Objective) | RPO (Recovery Point Objective) |
|---|---|---|
| Core Banking Platform | 4 hours | 15 minutes |
| Payment Gateway | 2 hours | 5 minutes |
| Corporate IT (email, collaboration) | 24 hours | 24 hours |

## 3. Redundancy (A.8.14)

- Core banking and payment gateway systems are deployed across redundant infrastructure (primary + DR site) with automated or documented manual failover procedures.
- Single points of failure identified through architecture review are logged in the Risk Register.

## 4. Backup (A.8.13, referenced)

- Nightly backups of production data, with quarterly restore testing.
- Backups stored on a separate network segment; an immutable/air-gapped backup copy for critical systems is being implemented per the RISK-008 treatment action, to protect against ransomware encrypting both production and backup data.

## 5. Security During Disruption (A.5.29)

- Security controls (access control, logging, monitoring) remain in effect during a DR invocation; the incident response and BC teams coordinate to avoid security gaps opening during the crisis (e.g., emergency access grants are still logged and time-bound).
- Any temporary control relaxation during an emergency requires CISO sign-off and is reverted and reviewed post-event.

## 6. ICT Readiness Testing (A.5.30)

- A full DR failover test is performed **at least annually**; partial/component tests may supplement but do not replace the full test.
- Test results (actual RTO/RPO achieved vs. target) are documented and gaps are remediated with tracked corrective actions (ref. FND-07).
- Tabletop exercises are conducted semi-annually per Information Security Objective OBJ-07.

## 7. Business Continuity Plan Activation

A documented BC Plan defines activation criteria, roles (BC Team, Incident Commander), communication protocols, and stand-down criteria. The BC Plan is reviewed annually and after every activation or major test.

## 8. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.0 | — | BCP/DR Lead | Approved |
