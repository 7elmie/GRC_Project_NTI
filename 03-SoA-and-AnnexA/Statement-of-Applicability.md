# Statement of Applicability

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-DOC-007 |
| ISO 27001:2022 Clause | 6.1.3(d) |
| Owner | CISO |
| Approved by | CEO / Top Management |
| Status | Approved |
| Version | 1.0 |
| Classification | Internal — Confidential |

All 93 Annex A:2022 controls are assessed below. **Applicable** = Yes for all controls (justified in `00-Index.md`). Status values: **Implemented**, **Partially Implemented** (open item tracked in Risk Treatment Plan / Internal Audit), **Planned**.

## A.5 — Organizational Controls (37)

| ID | Control | Justification for Inclusion | Status | Evidence / Owning Document | Related Risk(s) |
|---|---|---|---|---|---|
| 5.1 | Policies for information security | Mandatory ISMS foundation; regulatory expectation for financial services | Implemented | `01-ISMS-Mandatory-Documents/Information-Security-Policy.md` | — |
| 5.2 | Information security roles and responsibilities | Required for accountability and segregation of duties | Implemented | `01-ISMS-Mandatory-Documents/Roles-Responsibilities-Authorities.md` | — |
| 5.3 | Segregation of duties | Prevents fraud/error in banking and payment processing | Implemented | `01-ISMS-Mandatory-Documents/Roles-Responsibilities-Authorities.md` §5 | RISK-001 |
| 5.4 | Management responsibilities | Reinforces top management commitment | Implemented | Information Security Policy §2 | — |
| 5.5 | Contact with authorities | Required for breach notification (regulators, law enforcement, card networks) | Implemented | Incident Management Policy (`05-Policies-and-Procedures`) | — |
| 5.6 | Contact with special interest groups | Threat intelligence sharing (FS-ISAC / national CERT membership) | Implemented | SOC operating procedure | RISK-003, RISK-005 |
| 5.7 | Threat intelligence | Informs risk assessment and detection engineering | Partially Implemented | SOC intel feed subscribed; formal intel-to-detection process being formalized | RISK-001, RISK-003 |
| 5.8 | Information security in project management | Ensures security is built into new initiatives | Partially Implemented | Secure Development Policy; project security gate being rolled out | RISK-009 |
| 5.9 | Inventory of information and other associated assets | Foundation for risk assessment (Clause 6.1.2) | Implemented | Asset Inventory (`02-Risk-Management`, referenced) | All risks |
| 5.10 | Acceptable use of information and other associated assets | Governs employee use of FFG systems and data | Implemented | Acceptable Use Policy (`05-Policies-and-Procedures`) | — |
| 5.11 | Return of assets | Part of termination process | Implemented | HR Offboarding Checklist | RISK-007 |
| 5.12 | Classification of information | Required to apply proportionate controls (esp. cardholder/PII data) | Implemented | Data Classification and Handling Policy | RISK-002 |
| 5.13 | Labelling of information | Supports classification enforcement | Partially Implemented | Manual labelling in place; automated DLP labelling planned | RISK-002 |
| 5.14 | Information transfer | Governs secure transfer internally/externally (incl. to processors) | Implemented | Data Classification and Handling Policy §Transfer | RISK-006 |
| 5.15 | Access control | Core control for banking/payment systems | Implemented | Access Control Policy | RISK-003, RISK-018 |
| 5.16 | Identity management | Lifecycle management of identities | Implemented | Access Control Policy; IAM platform | RISK-007 |
| 5.17 | Authentication information | Password/credential management standards | Implemented | Access Control Policy §Authentication | RISK-003, RISK-018 |
| 5.18 | Access rights | Provisioning, review, and revocation of access | Partially Implemented | Quarterly UAR process; automation for offboarding pending | RISK-007 |
| 5.19 | Information security in supplier relationships | Cloud provider and critical vendor dependency | Implemented | Supplier Relationships Policy | RISK-006 |
| 5.20 | Addressing information security within supplier agreements | Contractual security clauses (SLA, right-to-audit, breach notice) | Implemented | Supplier Relationships Policy; contract templates | RISK-006 |
| 5.21 | Managing information security in the ICT supply chain | Open-source/dependency risk, subcontracted development | Partially Implemented | SCA tooling rollout in progress (RISK-009 treatment) | RISK-009 |
| 5.22 | Monitoring, review and change management of supplier services | Ongoing oversight of cloud/critical suppliers | Implemented | Annual supplier risk assessment | RISK-006 |
| 5.23 | Information security for use of cloud services | Cloud is core to production architecture | Partially Implemented | CSPM rollout in progress (RISK-004 treatment) | RISK-004 |
| 5.24 | Information security incident management planning and preparation | Required for banking regulatory obligations | Implemented | Incident Management Policy | — |
| 5.25 | Assessment and decision on information security events | Triage process for SOC | Implemented | Incident Management Policy §Triage | RISK-003, RISK-005 |
| 5.26 | Response to information security incidents | IR runbooks | Implemented | Incident Response Playbooks | — |
| 5.27 | Learning from information security incidents | Post-incident review process | Implemented | Incident Management Policy §Post-Incident Review | — |
| 5.28 | Collection of evidence | Forensic readiness for incidents/investigations | Implemented | Incident Management Policy §Evidence Handling | — |
| 5.29 | Information security during disruption | Maintaining security during BC/DR invocation | Partially Implemented | BC Policy exists; full DR failover test overdue (RISK-017) | RISK-017 |
| 5.30 | ICT readiness for business continuity | Core to banking resilience regulatory expectations | Partially Implemented | Business Continuity Policy; DR test remediation open | RISK-006, RISK-008, RISK-017 |
| 5.31 | Legal, statutory, regulatory and contractual requirements | Banking/payments is a highly regulated sector | Partially Implemented | Legal register exists; proactive horizon-scanning being formalized | RISK-016 |
| 5.32 | Intellectual property rights | Protects proprietary banking platform code | Implemented | Acceptable Use Policy; IP clauses in contracts | — |
| 5.33 | Protection of records | Financial records retention obligations | Implemented | Document Control Procedure §7 (Retention) | — |
| 5.34 | Privacy and protection of PII | Customer PII central to banking operations | Partially Implemented | Data Classification and Handling Policy; PAN log exposure open item (RISK-002) | RISK-002 |
| 5.35 | Independent review of information security | Objectivity requirement for ISMS assurance | Implemented | Internal Audit Programme (`04-Internal-Audit-Execution`) | — |
| 5.36 | Compliance with policies, rules and standards for information security | Ongoing policy compliance verification | Implemented | Internal Audit Programme; compliance checks | — |
| 5.37 | Documented operating procedures | Operational consistency and knowledge retention | Partially Implemented | Core procedures documented; some IT Ops runbooks pending formalization | RISK-015 |

## A.6 — People Controls (8)

| ID | Control | Justification for Inclusion | Status | Evidence / Owning Document | Related Risk(s) |
|---|---|---|---|---|---|
| 6.1 | Screening | Pre-employment background checks, esp. for privileged/finance roles | Implemented | HR Recruitment Procedure | — |
| 6.2 | Terms and conditions of employment | Contractual security obligations for staff | Implemented | Employment Contract template §Security | — |
| 6.3 | Information security awareness, education and training | Directly mitigates phishing/social engineering risk | Partially Implemented | Annual training programme; one department below completion target | RISK-003, RISK-005, RISK-011 |
| 6.4 | Disciplinary process | Consequence for policy violation | Implemented | Information Security Policy §6; HR Disciplinary Procedure | — |
| 6.5 | Responsibilities after termination or change of employment | Prevents unauthorized post-termination access | Partially Implemented | Offboarding checklist; automation pending (RISK-007) | RISK-007 |
| 6.6 | Confidentiality or non-disclosure agreements | Protects customer and proprietary data | Implemented | Employment contract; third-party NDA templates | — |
| 6.7 | Remote working | Hybrid workforce requires secured remote access | Implemented | Acceptable Use Policy §Remote Work; VPN/Zero Trust access | — |
| 6.8 | Information security event reporting | Enables timely detection via staff reporting | Implemented | Incident Management Policy §Reporting Channels | — |

## A.7 — Physical Controls (14)

*Note: FFG's primary data center is a third-party managed co-location facility (see RISK-010). Physical controls below are implemented via a combination of direct FFG control (head office) and supplier oversight/contractual assurance (data center), evidenced by the provider's SOC 2 Type II report reviewed annually.*

| ID | Control | Justification for Inclusion | Status | Evidence / Owning Document | Related Risk(s) |
|---|---|---|---|---|---|
| 7.1 | Physical security perimeters | Protects head office and data center facilities | Implemented | Physical Security Policy; provider SOC 2 report | RISK-010 |
| 7.2 | Physical entry | Badge/biometric access control | Implemented | Physical Security Policy; provider SOC 2 report | RISK-010 |
| 7.3 | Securing offices, rooms and facilities | Server rooms, executive offices | Implemented | Physical Security Policy | — |
| 7.4 | Physical security monitoring | CCTV, intrusion detection | Implemented | Physical Security Policy; provider SOC 2 report | RISK-010 |
| 7.5 | Protecting against physical and environmental threats | Fire suppression, flood protection at DC | Implemented | Provider SOC 2 report; DR site assessment | RISK-017 |
| 7.6 | Working in secure areas | Controls for staff working in server/ops rooms | Implemented | Physical Security Policy | — |
| 7.7 | Clear desk and clear screen | Reduces exposure of sensitive info at workstations | Implemented | Acceptable Use Policy §Clear Desk | — |
| 7.8 | Equipment siting and protection | Server placement, environmental controls | Implemented | Provider SOC 2 report | — |
| 7.9 | Security of assets off-premises | Laptops, mobile devices used remotely | Implemented | Acceptable Use Policy §Remote Work; MDM enrollment | — |
| 7.10 | Storage media | Handling of removable media (largely restricted) | Implemented | Data Classification and Handling Policy §Media | — |
| 7.11 | Supporting utilities | Power, cooling redundancy at DC | Implemented | Provider SOC 2 report; DC contract SLA | RISK-017 |
| 7.12 | Cabling security | Protection of power/data cabling | Implemented | Provider SOC 2 report | — |
| 7.13 | Equipment maintenance | Scheduled maintenance of physical infrastructure | Implemented | Provider SOC 2 report; internal asset maintenance log | — |
| 7.14 | Secure disposal or re-use of equipment | Prevents data leakage via decommissioned hardware | Implemented | IT Asset Disposal Procedure (certified data destruction) | — |

## A.8 — Technological Controls (34)

| ID | Control | Justification for Inclusion | Status | Evidence / Owning Document | Related Risk(s) |
|---|---|---|---|---|---|
| 8.1 | User endpoint devices | Fleet-wide device security baseline | Implemented | Endpoint hardening standard; MDM/EDR deployment | RISK-005 |
| 8.2 | Privileged access rights | Critical for banking system integrity | Partially Implemented | PAM in place; hardware-token MFA rollout for execs open (RISK-018) | RISK-018 |
| 8.3 | Information access restriction | Least-privilege enforcement | Implemented | Access Control Policy §Least Privilege | RISK-003 |
| 8.4 | Access to source code | Protects proprietary banking platform IP | Implemented | Source control access policy; code repo permissions | — |
| 8.5 | Secure authentication | MFA, SSO across systems | Partially Implemented | MFA enforced broadly; legacy service accounts open (RISK-003) | RISK-003, RISK-018 |
| 8.6 | Capacity management | Prevents availability degradation | Implemented | Infrastructure capacity monitoring/alerting | — |
| 8.7 | Protection against malware | EDR fleet-wide, email filtering | Implemented | Endpoint hardening standard | RISK-005 |
| 8.8 | Management of technical vulnerabilities | Patch management, vulnerability scanning | Implemented | Vulnerability Management Procedure | RISK-001 |
| 8.9 | Configuration management | Baseline configs for servers/cloud | Partially Implemented | Baselines defined; CSPM automation for cloud open (RISK-004) | RISK-001, RISK-004 |
| 8.10 | Information deletion | Secure deletion per retention schedule | Implemented | Data Classification and Handling Policy §Deletion | — |
| 8.11 | Data masking | Protects sensitive test/production data | Partially Implemented | Applied in select environments; standardization in progress | RISK-002 |
| 8.12 | Data leakage prevention | Prevents unauthorized data exfiltration | Partially Implemented | DLP on primary channels; log redaction gap open (RISK-002) | RISK-002 |
| 8.13 | Information backup | Business continuity requirement | Partially Implemented | Nightly backups; immutability upgrade pending (RISK-008) | RISK-008 |
| 8.14 | Redundancy of information processing facilities | Availability for core banking | Implemented | DR site; redundant infrastructure design | RISK-017 |
| 8.15 | Logging | Supports detection and forensic investigation | Partially Implemented | Centralized logging; PAN-redaction gap on one service (RISK-002) | RISK-002, RISK-001 |
| 8.16 | Monitoring activities | SIEM/SOC monitoring | Implemented | SOC operating procedure | RISK-001, RISK-003 |
| 8.17 | Clock synchronization | Ensures reliable log correlation | Implemented | NTP standard across infrastructure | — |
| 8.18 | Use of privileged utility programs | Restricts powerful system tools | Implemented | PAM configuration; restricted utility access | — |
| 8.19 | Installation of software on operational systems | Prevents unauthorized/unvetted software | Implemented | Change Management Procedure; application allow-listing | — |
| 8.20 | Networks security | Perimeter and internal network protection | Partially Implemented | Payment/banking segments isolated; corporate VLAN segmentation open (RISK-013) | RISK-013 |
| 8.21 | Security of network services | Secure configuration of network services | Implemented | Network security standard | — |
| 8.22 | Segregation of networks | Isolates payment/banking systems from corporate | Partially Implemented | Core segments isolated; corporate VLAN segmentation open (RISK-013) | RISK-013 |
| 8.23 | Web filtering | Reduces malicious site/phishing exposure | Implemented | Secure web gateway | RISK-005 |
| 8.24 | Use of cryptography | Encryption in transit/at rest for financial data | Partially Implemented | KMS for new systems; legacy service rotation gap (RISK-014) | RISK-014 |
| 8.25 | Secure development life cycle | SDLC security gates | Implemented | Secure Development Policy | RISK-009 |
| 8.26 | Application security requirements | Security requirements defined pre-development | Implemented | Secure Development Policy §Requirements | — |
| 8.27 | Secure system architecture and engineering principles | Security-by-design for new systems | Implemented | Architecture Review Board process | — |
| 8.28 | Secure coding | Directly mitigates injection/logic flaws | Partially Implemented | Secure coding standard; admin module remediation open (RISK-001) | RISK-001, RISK-009, RISK-012 |
| 8.29 | Security testing in development and acceptance | SAST/DAST/pen testing | Partially Implemented | SAST in CI; SCA integration in progress (RISK-009) | RISK-009, RISK-012 |
| 8.30 | Outsourced development | Governs any third-party development work | Implemented | Supplier Relationships Policy §Outsourced Dev | — |
| 8.31 | Separation of development, test and production environments | Prevents test data/config leakage to prod | Implemented | Environment separation standard | — |
| 8.32 | Change management | CAB process for production changes | Partially Implemented | CAB for standard changes; emergency-change control open (RISK-015) | RISK-015 |
| 8.33 | Test information | Protects data used in test environments | Partially Implemented | Data masking standard applied inconsistently (linked to 8.11) | RISK-002 |
| 8.34 | Protection of information systems during audit testing | Prevents disruption from audit/pen-test activity | Implemented | Internal Audit Programme §Testing Safeguards | — |

## Approval

| Role | Name/Placeholder | Date |
|---|---|---|
| CISO (drafted) |  |  |
| CEO (approved) |  |  |

## Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | — | GRC Team | Initial control-by-control assessment |
| 1.0 | — | CISO | Approved by top management |
