# Risk Treatment Plan

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-REC-002 |
| ISO 27001:2022 Clause | 6.1.3(e), 8.3 |
| Owner | CISO |
| Status | Approved (current cycle) |
| Version | 1.0 |
| Classification | Internal — Confidential |

## 1. Purpose

Documents the actions to be taken for each risk selected for treatment (Modify/Share), the resources required, responsibilities, timelines, and the resulting **residual risk**, per Clause 6.1.3(e) and 8.3. Risks accepted without further treatment ("Retain") are documented in the Risk Register with formal sign-off, not repeated here.

## 2. Treatment Plan — High and Critical Risks

| Risk ID | Current Score / Rating | Treatment Action | Target Annex A Control(s) | Owner | Target Date | Expected Residual L×I | Residual Rating | Approval Required |
|---|---|---|---|---|---|---|---|---|
| RISK-003 | 16 / Critical | Enforce MFA for all remaining legacy service accounts; migrate to short-lived credentials where feasible | A.5.17, A.8.5 | IAM Lead | 30 days | 2×4 = 8 | Medium | CISO |
| RISK-001 | 15 / High | Remediate input validation gaps in identified admin module; add to SAST pipeline gating | A.8.28, A.8.29 | Head of Engineering | 60 days | 2×5 = 10 | High (re-review after fix) | CISO |
| RISK-018 | 15 / High | Deploy hardware-token (FIDO2) MFA for all privileged/executive accounts | A.8.2, A.8.5 | CISO | 45 days | 2×5 = 10 | High (re-review after fix) | CEO (given Critical starting rating) |
| RISK-004 | 12 / High | Deploy CSPM tooling across all cloud accounts; remediate public-exposure findings | A.8.9, A.5.23 | Cloud Platform Lead | 90 days | 2×4 = 8 | Medium | CISO |
| RISK-005 | 12 / High | Targeted awareness re-training for lagging department; simulate phishing follow-up campaign | A.6.3, A.8.7 | SOC Manager | 60 days | 2×4 = 8 | Medium | CISO |
| RISK-009 | 12 / High | Integrate SCA tool into CI/CD pipeline; block builds on Critical/High CVEs | A.8.28, A.8.29, A.5.21 | Head of Engineering | 90 days | 2×4 = 8 | Medium | CISO |
| RISK-013 | 12 / High | Segment corporate VLAN by function; deploy internal firewall rules between segments | A.8.20, A.8.22 | Network Eng. Lead | 120 days | 2×4 = 8 | Medium | CISO |
| RISK-014 | 12 / High | Migrate legacy encryption service to centralized KMS with automated rotation | A.8.24 | Security Engineering Lead | 90 days | 2×4 = 8 | Medium | CISO |
| RISK-002 | 10 / High | Redact/mask PAN in all application logs; complete PCI log-scoping review | A.8.12, A.8.15, A.5.34 | Payments Eng. Lead | 45 days | 1×5 = 5 | Medium | CISO |
| RISK-006 | 10 / High | Expand supplier due diligence to full subprocessor mapping; review provider SOC 2 annually with formal sign-off | A.5.19–5.23, A.5.30 | Vendor Risk Manager | 90 days | 2×5 = 10 | High (contractual limits apply — flag for acceptance review) | CISO |
| RISK-008 | 10 / High | Implement immutable/air-gapped backup copy for critical systems | A.8.13, A.5.30 | IT Ops Head | 90 days | 1×5 = 5 | Medium | CISO |
| RISK-017 | 10 / High | Conduct full DR failover test; remediate gaps identified | A.5.29, A.5.30 | BCP/DR Lead | 120 days | 2×5 = 10 | High (re-review after test) | CISO |

## 3. Medium Risks (Treat Within 12 Months)

| Risk ID | Score / Rating | Treatment Action | Owner | Target Date |
|---|---|---|---|---|
| RISK-007 | 9 / Medium | Automate offboarding trigger from HR system to IAM (SLA ≤ 4 hours) | HR / IAM Lead | 6 months |
| RISK-011 | 9 / Medium | Enforce mandatory knowledge-based verification step in support tooling (system-enforced, not verbal-only) | Customer Support Lead | 6 months |
| RISK-016 | 9 / Medium | Establish proactive regulatory horizon-scanning process with Legal | Compliance Lead | 9 months |
| RISK-015 | 8 / Medium | Formalize emergency-change approval path with post-hoc CAB review within 24h | IT Ops Head | 6 months |
| RISK-012 | 6 / Medium | Add runtime application self-protection (RASP) evaluation to mobile roadmap | Mobile Eng. Lead | 12 months |

## 4. Accepted Risks (Retain)

| Risk ID | Score / Rating | Justification | Accepted By | Review Date |
|---|---|---|---|---|
| RISK-010 | 4 / Low | Facility is third-party managed with independently audited (SOC 2 Type II) physical controls; residual exposure within tolerance | CISO | Annual |

## 5. Monitoring of Treatment Plan Execution

- Progress against this plan is reviewed **monthly** by the CISO and **quarterly** by the ISMS Steering Committee.
- Overdue High/Critical treatment actions are escalated to the CEO.
- Upon completion of a treatment action, the risk owner and CISO re-assess the risk and update the Risk Register with the actual (not just expected) residual score, closing the treatment action.
- This plan and the Risk Register are formally reviewed as an input to the annual Management Review (`01-ISMS-Mandatory-Documents/Management-Review-Procedure-and-Minutes-Template.md`).

## 6. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | — | GRC Team | Draft treatment plan from risk workshop |
| 1.0 | — | CISO | Approved for current cycle |
