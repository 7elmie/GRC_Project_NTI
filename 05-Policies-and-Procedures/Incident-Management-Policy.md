# Incident Management Policy

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-POL-004 |
| Annex A Controls | A.5.24, A.5.25, A.5.26, A.5.27, A.5.28, A.5.5, A.6.8 |
| Owner | CISO / SOC Manager |
| Status | Approved |
| Version | 1.0 |
| Classification | Internal |

## 1. Purpose

Defines how information security events and incidents are reported, triaged, responded to, and learned from, per A.5.24–5.28.

## 2. Definitions

- **Event**: an observed occurrence that may indicate a security weakness or incident (e.g., an alert).
- **Incident**: one or more events confirmed to compromise, or attempt to compromise, confidentiality, integrity, or availability.

## 3. §Reporting Channels (A.6.8)

- All personnel must report suspected events immediately via the SOC hotline, security@mfg (monitored 24/7), or the incident ticketing portal.
- No disciplinary action is taken against personnel who report in good faith, including reporting their own mistake (e.g., clicking a phishing link), to encourage prompt reporting.

## 4. §Triage (A.5.25)

- SOC performs initial triage within 15 minutes for automated alerts and immediately upon manual report.
- Severity is assigned (Critical/High/Medium/Low) based on scope, data sensitivity, and business impact, consistent with the Risk Assessment Methodology's impact criteria.

## 5. Response (A.5.26)

- Confirmed incidents are managed per documented Incident Response Playbooks (ransomware, data breach, DDoS, insider threat, third-party compromise).
- Critical/High incidents trigger activation of the Incident Response Team and, where applicable, the Business Continuity Plan.
- Regulatory/customer notification obligations are assessed jointly with Legal/Compliance and, where required, Contact with Authorities (A.5.5) is executed within applicable statutory timeframes.

## 6. §Evidence Handling (A.5.28)

- Evidence (logs, system images, artifacts) is collected and preserved with chain-of-custody documentation sufficient for potential legal or regulatory proceedings.
- Evidence collection follows forensic best practice to avoid contaminating or altering original data.

## 7. §Post-Incident Review (A.5.27)

- Every Critical/High incident undergoes a blameless post-incident review within 10 business days, producing: root cause, timeline, what worked/didn't, and corrective actions.
- Corrective actions are logged in the CAPA tracker (see `04-Internal-Audit-Execution`) and tracked to closure.
- Lessons learned feed back into the Risk Register and, where relevant, the Statement of Applicability.

## 8. Communication

An incident communication plan defines internal escalation (CISO, CEO, Legal, Comms) and, where applicable, external communication (customers, regulators, media) with a single designated spokesperson.

## 9. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.0 | — | CISO | Approved |
