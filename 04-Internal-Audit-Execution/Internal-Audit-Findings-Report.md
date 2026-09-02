# Internal Audit Findings Report — IA-2026-01

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-REC-004 |
| ISO 27001:2022 Clause | 9.2.2, 10.1, 10.2 |
| Audit ID | IA-2026-01 |
| Lead Auditor |  |
| Report Date | [ |
| Distribution | CEO, CISO, Steering Committee, Audit Committee |
| Classification | Internal — Confidential |

## 1. Executive Summary

FFG's ISMS is **substantially implemented and operating**, with a documented policy framework, an approved Statement of Applicability covering all 93 Annex A:2022 controls, an active risk management process, and functioning governance (Steering Committee, Management Review). However, the audit identified **5 Major Nonconformities** and **6 Minor Nonconformities**, concentrated in the operational execution of previously identified High/Critical risk treatments (authentication hardening, data-leakage controls, and disaster-recovery testing).

**Conclusion on the compliance claim:** FFG's existing claim of ISO 27001:2022 compliance is **not yet fully substantiated** by objective evidence at the time of this audit. The ISMS structure and documentation meet requirements; however, the Major Nonconformities below represent gaps that would need to be closed, with objective evidence of effectiveness, before an external certification audit could be expected to succeed without significant findings. This is a normal and expected outcome for a first full-cycle internal audit and is not indicative of a fundamentally deficient ISMS — the risks were already known and being tracked (Risk Treatment Plan), which is itself evidence the ISMS is functioning as intended (Clause 9.1 monitoring feeding into Clause 10.1 improvement).

## 2. Finding Classification Definitions

- **Major Nonconformity**: Absence or failure to implement a required control, or a situation which, on the basis of objective evidence, raises significant doubt as to conformity of the ISMS or as to the capability of the process to achieve its intended results.
- **Minor Nonconformity**: A single observed lapse or isolated incident that does not indicate systemic failure.
- **Observation / OFI (Opportunity for Improvement)**: Not a nonconformity, but an area where the ISMS could be strengthened.

## 3. Detailed Findings

### FND-01 — Major Nonconformity
**Ref**: A.5.17, A.8.5 | **Related Risk**: RISK-003
**Finding**: 6 of 20 sampled legacy service accounts do not have MFA or an equivalent strong authentication mechanism enforced, contrary to the Access Control Policy requirement that all accounts, including service accounts, use strong authentication.
**Root Cause**: Legacy service accounts were provisioned before the current Access Control Policy was enforced via automated tooling; no compensating control (e.g., network-level restriction) was applied as an interim measure, and no exception/risk-acceptance was formally logged.
**Corrective Action**: Enforce MFA or migrate to short-lived/certificate-based credentials for all remaining legacy service accounts; where technically infeasible within the timeline, log a formal time-bound risk acceptance with compensating controls.
**Owner**: IAM Lead | **Due Date**: 30 days from report date | **Status**: Open (tracked in Risk Treatment Plan, RISK-003)

### FND-02 — Major Nonconformity
**Ref**: A.8.2 | **Related Risk**: RISK-018
**Finding**: Privileged and executive accounts use standard MFA rather than the hardware-token (phishing-resistant) authentication specified as the target control for high-value accounts.
**Root Cause**: Hardware-token rollout was scoped but not prioritized ahead of other initiatives; no interim compensating monitoring control (e.g., enhanced anomaly detection on privileged sessions) was implemented to offset the gap.
**Corrective Action**: Complete hardware-token MFA deployment for all privileged/executive accounts; implement enhanced session monitoring as an interim compensating control.
**Owner**: CISO | **Due Date**: 45 days | **Status**: Open

### FND-03 — Major Nonconformity
**Ref**: A.8.12, A.8.15, A.5.34 | **Related Risk**: RISK-002
**Finding**: Unredacted cardholder PAN data was observed in application logs for 1 of 5 sampled services, contrary to the Data Classification and Handling Policy and PCI-relevant logging requirements.
**Root Cause**: A recent feature release introduced additional logging without a security review gate to check for sensitive-data exposure in log output (gap in A.8.25 SDLC security review step).
**Corrective Action**: Immediately redact/mask PAN in the affected service's logs; add automated sensitive-data-in-logs scanning to the CI/CD pipeline for all services; complete PCI log-scoping review.
**Owner**: Payments Engineering Lead | **Due Date**: 45 days (immediate redaction within 7 days) | **Status**: Open — interim redaction in progress

### FND-04 — Minor Nonconformity
**Ref**: A.8.20, A.8.22 | **Related Risk**: RISK-013
**Finding**: Core payment/banking network segments are properly isolated; however, the corporate (non-payment) VLAN remains flat, increasing lateral-movement risk following an endpoint compromise.
**Root Cause**: Network segmentation project prioritized regulated (payment/banking) segments first; corporate segmentation was deprioritized in the original roadmap.
**Corrective Action**: Implement corporate VLAN segmentation by function with internal firewall rules, per the Risk Treatment Plan timeline.
**Owner**: Network Engineering Lead | **Due Date**: 120 days | **Status**: Open

### FND-05 — Minor Nonconformity
**Ref**: Clause 9.3
**Finding**: The prior Management Review did not explicitly document Risk Treatment Plan status as a discrete input, though it was discussed verbally per meeting attendee interviews.
**Root Cause**: Management Review minutes template did not, at the time, include a dedicated Risk Treatment Plan status section (this has since been added — see `01-ISMS-Mandatory-Documents/Management-Review-Procedure-and-Minutes-Template.md` §4).
**Corrective Action**: Use the updated Management Review minutes template for all future reviews; confirm at the next review that this section is completed.
**Owner**: CISO | **Due Date**: Next scheduled Management Review | **Status**: Closed — template updated

### FND-06 — Minor Nonconformity
**Ref**: Clause 10.1
**Finding**: Two prior informal findings (identified outside a formal audit cycle) were remediated but lack documented root cause analysis in the CAPA tracker.
**Root Cause**: Informal findings raised via ad hoc channels (e.g., Steering Committee discussion) were not always routed through the same CAPA process as formal audit findings.
**Corrective Action**: Route all identified nonconformities, regardless of source, through the formal CAPA tracker with mandatory root cause fields.
**Owner**: Head of Internal Audit | **Due Date**: 30 days | **Status**: Open

### FND-07 — Major Nonconformity
**Ref**: A.5.29, A.5.30 | **Related Risk**: RISK-017
**Finding**: The Disaster Recovery site has not undergone a full failover test in 18 months; only partial component tests have been performed, so RTO/RPO capability under realistic conditions is unverified.
**Root Cause**: Full failover testing requires a maintenance window with business sign-off that has been repeatedly deprioritized against feature delivery timelines.
**Corrective Action**: Schedule and execute a full DR failover test within the current cycle; formally document RTO/RPO results against targets; remediate any gaps identified.
**Owner**: BCP/DR Lead | **Due Date**: 120 days | **Status**: Open

### FND-08 — Minor Nonconformity
**Ref**: A.6.3, A.6.5 | **Related Risk**: RISK-007, RISK-011
**Finding**: (a) Security awareness training completion in Customer Support is below the 95% target; (b) 2 of 10 sampled terminations had access removed more than 24 hours after the employee's last working day.
**Root Cause**: (a) Training reminders are not escalated to department managers when overdue; (b) HR-to-IT offboarding handoff remains a manual, non-SLA-bound process.
**Corrective Action**: (a) Implement manager escalation for overdue training; (b) automate the HR-to-IAM offboarding trigger with a 4-hour SLA.
**Owner**: HR / IAM Lead | **Due Date**: 6 months | **Status**: Open

### FND-09 — Minor Nonconformity
**Ref**: A.8.24 | **Related Risk**: RISK-014
**Finding**: One legacy encryption service has not had its keys rotated in over 12 months, exceeding the cryptography standard's rotation interval.
**Root Cause**: Legacy service predates centralized KMS adoption and relies on manual rotation, which was not tracked with an automated reminder.
**Corrective Action**: Migrate the legacy service to centralized KMS with automated rotation.
**Owner**: Security Engineering Lead | **Due Date**: 90 days | **Status**: Open

### FND-10 — Observation (OFI)
**Ref**: A.5.21, A.8.29 | **Related Risk**: RISK-009
**Finding**: No automated Software Composition Analysis (SCA) is currently integrated into the CI/CD pipeline; dependency review is manual and only performed at major releases.
**Recommendation**: Integrate an SCA tool with build-blocking on Critical/High CVEs, consistent with the Risk Treatment Plan action already scoped for RISK-009.
**Owner**: Head of Engineering | **Status**: Tracked as planned improvement, not a nonconformity (no evidence of an actual incident to date)

### FND-11 — Observation (OFI)
**Ref**: A.5.23, A.8.9 | **Related Risk**: RISK-004
**Finding**: Cloud Security Posture Management (CSPM) tooling is not yet deployed to all cloud accounts; current control relies on manual quarterly review.
**Recommendation**: Complete CSPM rollout per the existing Risk Treatment Plan timeline; consider real-time alerting rather than quarterly-only review.
**Owner**: Cloud Platform Lead | **Status**: Tracked as planned improvement

## 4. Summary Table

| Finding | Severity | Clause/Control | Related Risk | Owner | Due Date | Status |
|---|---|---|---|---|---|---|
| FND-01 | Major | A.5.17, A.8.5 | RISK-003 | IAM Lead | 30 days | Open |
| FND-02 | Major | A.8.2 | RISK-018 | CISO | 45 days | Open |
| FND-03 | Major | A.8.12, A.8.15 | RISK-002 | Payments Eng. Lead | 45 days | Open |
| FND-04 | Minor | A.8.20, A.8.22 | RISK-013 | Network Eng. Lead | 120 days | Open |
| FND-05 | Minor | Clause 9.3 | — | CISO | Next review | Closed |
| FND-06 | Minor | Clause 10.1 | — | Head of Internal Audit | 30 days | Open |
| FND-07 | Major | A.5.29, A.5.30 | RISK-017 | BCP/DR Lead | 120 days | Open |
| FND-08 | Minor | A.6.3, A.6.5 | RISK-007, RISK-011 | HR / IAM Lead | 6 months | Open |
| FND-09 | Minor | A.8.24 | RISK-014 | Security Eng. Lead | 90 days | Open |
| FND-10 | OFI | A.5.21, A.8.29 | RISK-009 | Head of Engineering | — | Planned |
| FND-11 | OFI | A.5.23, A.8.9 | RISK-004 | Cloud Platform Lead | — | Planned |

## 5. Follow-Up

Per the Internal Audit Programme, closure of all Major Nonconformities will be independently verified before any recommendation to proceed with external certification. Minor Nonconformities and OFIs are tracked to closure via the CAPA tracker and reviewed at each quarterly Steering Committee meeting and the next Management Review.

## 6. Auditor Sign-off

| Role | Name | Date |
|---|---|---|
| Lead Auditor |  |  |
| Head of Internal Audit |  |  |

## 7. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.0 | — | Lead Auditor | Final findings report for IA-2026-01 |
