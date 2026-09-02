# Information Security Objectives

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-DOC-003 |
| ISO 27001:2022 Clause | 6.2 |
| Owner | CISO |
| Status | Approved |
| Version | 1.0 |
| Classification | Internal |

## 1. Purpose

Establishes measurable information security objectives, consistent with the Information Security Policy, and the plans to achieve them, per Clause 6.2.

## 2. Objectives

| ID | Objective | Metric / Target | Owner | Resources | Deadline | Method of Evaluation |
|---|---|---|---|---|---|---|
| OBJ-01 | Reduce mean time to detect (MTTD) security incidents | MTTD ≤ 4 hours for High/Critical severity | SOC Manager | SIEM tuning, additional detection rules, analyst training | Q4 (current cycle) | Monthly SOC metrics review |
| OBJ-02 | Reduce mean time to remediate (MTTR) critical vulnerabilities | 100% of Critical CVSS ≥9.0 vulnerabilities on internet-facing assets patched within 7 days | Head of IT Ops | Patch management tooling, change window agreement | Ongoing, reviewed quarterly | Monthly vulnerability management report |
| OBJ-03 | Increase security awareness | ≥95% completion of annual security awareness training; phishing simulation click rate ≤5% | HR / Security Awareness Lead | LMS platform, phishing simulation tool | Annual cycle | Training completion reports, quarterly phishing campaign results |
| OBJ-04 | Maintain access control hygiene | 100% of user access reviews (UAR) completed each quarter with no overdue items >30 days | IAM Lead | Access review tooling, manager engagement | Quarterly | Quarterly UAR completion report |
| OBJ-05 | Improve third-party risk visibility | 100% of critical/high-risk suppliers assessed annually against the Supplier Security Questionnaire | Vendor Risk Manager | Vendor risk register, questionnaire tooling | Annual | Annual supplier risk assessment log |
| OBJ-06 | Sustain ISMS audit performance | Zero repeat major nonconformities across consecutive internal/external audit cycles | CISO | Internal audit programme, CAPA tracking | Each audit cycle | Internal audit reports, CAPA closure log |
| OBJ-07 | Improve incident response readiness | ≥2 tabletop exercises / DR-BCP tests per year, with findings closed within 60 days | BCP/DR Lead | Exercise scenarios, cross-functional participation | Semi-annual | Exercise after-action reports |

## 3. Monitoring and Communication

- Objective status is reviewed at each quarterly ISMS steering committee meeting and formally reported at the annual Management Review (see `Management-Review-Procedure-and-Minutes-Template.md`).
- Objectives are communicated to relevant personnel via the ISMS intranet page and team-level cascades.
- Objectives are updated when: the risk landscape changes materially, an audit finding requires a new objective, or an existing objective is achieved and superseded.

## 4. Alignment to Risk Treatment

Each objective above traces to one or more risks in the Risk Register (`02-Risk-Management/Risk-Register.md`) and/or controls in the Statement of Applicability (`03-SoA-and-AnnexA`). This traceability is maintained in the Risk Register's "Related Objective" column.

## 5. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | — | ISMS Team | Initial draft |
| 1.0 | — | CISO | Approved |
