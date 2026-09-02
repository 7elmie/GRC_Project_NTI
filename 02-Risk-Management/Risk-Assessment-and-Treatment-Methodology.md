# Risk Assessment and Risk Treatment Methodology

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-PRO-001 |
| ISO 27001:2022 Clause | 6.1.2, 6.1.3 |
| Owner | CISO |
| Status | Approved |
| Version | 1.0 |
| Classification | Internal |

## 1. Purpose

Defines a consistent, repeatable, and comparable method for identifying, analyzing, and evaluating information security risks, and for selecting risk treatment options, per Clause 6.1.2 and 6.1.3.

## 2. Risk Assessment Approach

FFG uses an **asset-based, threat/vulnerability risk assessment** methodology, performed:

- Annually as a full ISMS-wide assessment
- On significant change (new system, major architecture change, new regulation, post-incident)
- As part of new supplier onboarding (scoped to the supplier relationship) and new project initiation

### 2.1 Risk Identification

For each in-scope asset (from the Asset Inventory), the risk owner identifies:

1. **Threats** — sources of potential harm (e.g., external attacker, malicious insider, system failure, natural disaster, third-party compromise)
2. **Vulnerabilities** — weaknesses that a threat could exploit (e.g., unpatched software, weak access control, lack of redundancy, untrained staff)
3. **Existing controls** — controls already in place that reduce likelihood or impact

### 2.2 Risk Analysis — Likelihood

| Level | Rating | Description |
|---|---|---|
| 1 | Rare | Unlikely to occur (< once per 5 years); no known precedent |
| 2 | Unlikely | Could occur (once per 1–5 years); isolated precedent in industry |
| 3 | Possible | Might occur (annually); some precedent at FFG or peers |
| 4 | Likely | Expected to occur (multiple times/year); regular precedent |
| 5 | Almost Certain | Expected to occur frequently; ongoing exposure with no mitigating control |

### 2.3 Risk Analysis — Impact

Impact is assessed across Confidentiality, Integrity, and Availability; the **highest** applicable impact rating is used.

| Level | Rating | Financial | Regulatory/Legal | Reputational | Operational |
|---|---|---|---|---|---|
| 1 | Negligible | < $10K | No reporting obligation | No external visibility | < 1 hr disruption |
| 2 | Minor | $10K–$100K | Internal reporting only | Limited internal awareness | < 4 hr disruption |
| 3 | Moderate | $100K–$1M | Regulator notification required | Local media / customer complaints | < 24 hr disruption |
| 4 | Major | $1M–$10M | Regulatory fine/investigation | National media coverage | Multi-day disruption |
| 5 | Severe | > $10M | License/charter at risk | Sustained reputational damage, customer attrition | Extended outage, safety impact |

### 2.4 Risk Score and Heat Map

**Risk Score = Likelihood × Impact** (range 1–25)

| Score | Rating | Response Requirement |
|---|---|---|
| 1–4 | Low | Accept; monitor at next review cycle |
| 5–9 | Medium | Treat within 12 months; monitor quarterly |
| 10–15 | High | Treat within 90 days; monitor monthly; report to Steering Committee |
| 16–25 | Critical | Treat within 30 days; immediate escalation to CISO and top management |

## 3. Risk Evaluation and Acceptance Criteria

- Risks scoring **Low** may be accepted by the risk/asset owner.
- Risks scoring **Medium** require CISO acceptance if not treated.
- Risks scoring **High or Critical** require **top management (CEO)** acceptance if not fully mitigated, documented with justification in the Risk Register.
- Risk acceptance is time-bound (maximum 12 months) and must be re-reviewed at expiry.

## 4. Risk Treatment Options (Clause 6.1.3)

| Option | Description | Example |
|---|---|---|
| **Modify (Mitigate)** | Apply control(s) to reduce likelihood and/or impact | Implement MFA, patch management |
| **Retain (Accept)** | Formally accept the risk within tolerance, with sign-off | Accept residual risk of a low-impact legacy tool being decommissioned in 6 months |
| **Avoid** | Discontinue the activity/asset causing the risk | Decommission an unsupported system rather than patch indefinitely |
| **Share (Transfer)** | Transfer risk via insurance, contract, or outsourcing | Cyber insurance, contractual indemnification with a cloud provider |

## 5. Selecting Controls

Where "Modify" is selected, controls are selected primarily from **ISO/IEC 27001:2022 Annex A**, cross-checked to ensure no necessary control has been omitted (Clause 6.1.3 c), and documented in the Statement of Applicability with justification (Clause 6.1.3 d).

## 6. Roles

| Activity | Responsible |
|---|---|
| Facilitate risk assessment | CISO / GRC team |
| Identify risks for their asset/process | Asset/Process Owner |
| Approve risk treatment plan | CISO |
| Accept High/Critical residual risk | CEO / Top Management |
| Maintain Risk Register | GRC team |

## 7. Comparability and Consistency

This methodology, once approved, is applied consistently across all assessments so that results are comparable across cycles and across business units — enabling trend analysis at Management Review.

## 8. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | — | ISMS Team | Initial draft |
| 1.0 | — | CISO | Approved |
