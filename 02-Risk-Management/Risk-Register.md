# Risk Register

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-REC-001 |
| ISO 27001:2022 Clause | 6.1.2, 8.2 |
| Owner | CISO |
| Status | Approved (current cycle) |
| Version | 1.0 |
| Classification | Internal — Confidential (contains risk exposure detail) |
| Methodology Reference | `Risk-Assessment-and-Treatment-Methodology.md` |

> Scores use Likelihood (1–5) × Impact (1–5) = Risk Score (1–25). Rating bands: Low 1–4, Medium 5–9, High 10–15, Critical 16–25.

## Risk Register — Current Cycle

| ID | Asset | Threat | Vulnerability | Existing Controls | L | I | Score | Rating | Treatment | Related Annex A Control(s) | Related Objective | Owner | Status |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RISK-001 | Core Banking Platform (prod DB) | External attacker — SQL injection / unauthorized data access | Legacy input validation gaps in one internal admin module | WAF, code review for new code, DB activity monitoring | 3 | 5 | 15 | High | Modify | A.8.28 (Secure Coding), A.8.9 (Config Mgmt), A.8.16 (Monitoring) | OBJ-02 | Head of Engineering | Open — remediation in progress |
| RISK-002 | Payment Gateway | Cardholder data exposure via misconfigured logging | Verbose logging captures PAN in application logs on one service | Log redaction on primary services; PCI scoping review | 2 | 5 | 10 | High | Modify | A.8.12 (Data Leakage Prevention), A.8.15 (Logging), A.5.34 (Privacy/PII) | OBJ-02 | Payments Eng. Lead | Open |
| RISK-003 | Corporate IT — Identity Provider | Credential compromise via phishing | No enforced MFA for a subset of legacy service accounts | MFA enforced for standard user accounts; SSO in place | 4 | 4 | 16 | Critical | Modify | A.5.17 (Authentication Info), A.8.5 (Secure Authentication), A.6.3 (Awareness Training) | OBJ-01, OBJ-03 | IAM Lead | Open — 30-day remediation |
| RISK-004 | Cloud Production Environment | Misconfiguration leading to public exposure of storage bucket | No automated cloud security posture management (CSPM) coverage on newly onboarded accounts | Manual quarterly cloud config review | 3 | 4 | 12 | High | Modify | A.8.9 (Config Mgmt), A.5.23 (Cloud Services Security) | OBJ-02 | Cloud Platform Lead | Open |
| RISK-005 | Employee Endpoints | Malware/ransomware via phishing email | Awareness training completion below target in one department | EDR deployed fleet-wide; email filtering | 3 | 4 | 12 | High | Modify | A.8.7 (Malware Protection), A.6.3 (Awareness Training) | OBJ-03 | SOC Manager | Open |
| RISK-006 | Third-Party Cloud Hosting Provider | Provider-side outage or breach affecting shared infrastructure | Limited visibility into subprocessor chain | Contractual SLA, provider SOC 2 report reviewed annually | 2 | 5 | 10 | High | Modify + Share | A.5.19–5.23 (Supplier Relationships), A.5.30 (ICT Readiness for BC) | OBJ-05 | Vendor Risk Manager | Open |
| RISK-007 | HR Onboarding/Offboarding Process | Delayed access revocation for terminated employees | Manual offboarding checklist, occasional delay > 24h | HR-IT handoff process; quarterly UAR | 3 | 3 | 9 | Medium | Modify | A.5.16 (Identity Mgmt), A.6.5 (Termination Responsibilities) | OBJ-04 | HR / IAM Lead | Open |
| RISK-008 | Backup Systems | Ransomware encrypting backups alongside production | Backups on separate network segment; not yet fully immutable | Nightly backups, quarterly restore test | 2 | 5 | 10 | High | Modify | A.8.13 (Backup), A.5.30 (BC Readiness) | OBJ-07 | IT Ops Head | Open |
| RISK-009 | Software Supply Chain | Malicious/vulnerable open-source dependency introduced into codebase | No automated SCA (software composition analysis) in CI pipeline | Manual dependency review at major releases | 3 | 4 | 12 | High | Modify | A.8.28 (Secure Coding), A.8.29 (Security Testing), A.5.21 (ICT Supply Chain) | OBJ-02 | Head of Engineering | Open |
| RISK-010 | Physical Data Center | Unauthorized physical access | Provider-managed facility with badge + biometric access | Third-party audit (SOC 2 Type II) reviewed annually | 1 | 4 | 4 | Low | Retain (Accept) | A.7.2 (Physical Entry), A.7.4 (Physical Monitoring) | — | Facilities/CISO | Accepted — reviewed annually |
| RISK-011 | Customer Support Systems | Social engineering of support staff to reset customer credentials | Verbal ID verification process, inconsistent adherence | Call scripts, spot-check QA | 3 | 3 | 9 | Medium | Modify | A.6.3 (Awareness Training), A.5.17 (Authentication Info) | OBJ-03 | Customer Support Lead | Open |
| RISK-012 | Mobile Banking App | Reverse engineering exposing API keys / business logic | Basic obfuscation; no runtime application self-protection | Code signing, app store review process | 2 | 3 | 6 | Medium | Modify | A.8.28 (Secure Coding), A.8.29 (Security Testing) | OBJ-02 | Mobile Eng. Lead | Open |
| RISK-013 | Internal Network | Lateral movement following initial endpoint compromise | Flat network segments in corporate (non-payment) VLAN | Core banking/payment segments already isolated | 3 | 4 | 12 | High | Modify | A.8.20 (Network Security), A.8.22 (Segregation of Networks) | OBJ-01 | Network Eng. Lead | Open |
| RISK-014 | Encryption Key Management | Weak key rotation practice for a legacy encryption service | Manual rotation, last performed > 12 months ago on one system | KMS used for newer systems | 3 | 4 | 12 | High | Modify | A.8.24 (Use of Cryptography) | OBJ-02 | Security Engineering Lead | Open |
| RISK-015 | Change Management Process | Unauthorized/untested change causing production outage | Change Advisory Board (CAB) process exists but emergency-change path lightly controlled | CAB for standard changes; post-implementation review | 2 | 4 | 8 | Medium | Modify | A.8.32 (Change Management) | OBJ-07 | IT Ops Head | Open |
| RISK-016 | Regulatory Environment | New data protection regulation increasing compliance obligations | Compliance monitoring is reactive rather than proactive | Legal/Compliance function tracks major regulatory bodies | 3 | 3 | 9 | Medium | Modify | A.5.31 (Legal, Statutory, Regulatory Requirements), A.5.34 (Privacy) | — | Compliance Lead | Open |
| RISK-017 | Disaster Recovery Site | DR site fails to meet RTO/RPO under real failover conditions | Untested assumptions since last full failover test (18 months) | Documented DR plan; partial component tests | 2 | 5 | 10 | High | Modify | A.5.29 (Security During Disruption), A.5.30 (ICT Readiness for BC) | OBJ-07 | BCP/DR Lead | Open |
| RISK-018 | Executive/Privileged Accounts | Targeted spear-phishing / business email compromise | Privileged accounts not on separate hardware-token MFA | Standard MFA in place | 3 | 5 | 15 | High | Modify | A.8.2 (Privileged Access Rights), A.8.5 (Secure Authentication) | OBJ-01 | CISO | Open |

## Legend

- **L** = Likelihood (1–5), **I** = Impact (1–5)
- Risks rated **High/Critical** feed directly into the Risk Treatment Plan (`Risk-Treatment-Plan.md`) with mandated treatment timelines per the methodology.
- Risk-001 through Risk-018 above are illustrative of the assessment population for this audit cycle; the full register in production would extend to all assets in the Asset Inventory.

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | — | GRC Team | Initial risk identification workshop |
| 1.0 | — | CISO | Reviewed and approved for current cycle |
