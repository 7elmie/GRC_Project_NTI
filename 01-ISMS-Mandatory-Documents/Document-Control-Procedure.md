# Document Control Procedure

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-DOC-005 |
| ISO 27001:2022 Clause | 7.5 (Documented Information) |
| Owner | CISO / ISMS Coordinator |
| Status | Approved |
| Version | 1.0 |
| Classification | Internal |

## 1. Purpose

Defines how ISMS documented information is created, updated, approved, distributed, protected, and controlled, per Clause 7.5.1–7.5.3.

## 2. Document Lifecycle

1. **Creation** — drafted by the document owner (role) using the standard template and naming convention.
2. **Review** — reviewed by the CISO or delegate for technical accuracy and consistency with related documents.
3. **Approval** — approved by the role designated in Section 4 below, recorded in the document's Revision History.
4. **Publication** — published to the controlled repository (this GitHub repository, `main` branch, protected).
5. **Periodic Review** — reviewed at the interval defined in the document header, or upon triggering event (Section 5).
6. **Retirement/Superseding** — superseded versions are retained per the Records Retention rules (Section 7), not deleted, and marked "Superseded."

## 3. Naming and Identification Convention

`FFG-ISMS-DOC-###` for ISMS mandatory documents, `FFG-ISMS-POL-###` for policies, `FFG-ISMS-PRO-###` for procedures, `FFG-ISMS-REC-###` for records/registers. Each document header must state: Document ID, Owner, Status, Version, Classification, and Review Cycle.

## 4. Approval Authority by Document Type

| Document Type | Reviewer | Approver |
|---|---|---|
| Top-level policy (e.g., Information Security Policy) | CISO | CEO / Top Management |
| Topic-specific policy | CISO | CISO |
| Procedure | Process Owner | CISO |
| Register/Record (e.g., Risk Register) | CISO | CISO |
| Audit report | Lead Auditor | Internal Audit Function Head |

## 5. Triggers for Off-Cycle Review

- Significant organizational or scope change
- Major security incident related to the document's subject matter
- New/changed legal, regulatory, or contractual requirement
- Internal or external audit finding requiring document update
- Introduction of new technology materially affecting the process described

## 6. Version Control

- Versions follow `MAJOR.MINOR` (e.g., 1.0, 1.1, 2.0). MINOR increments for clarifications/non-substantive edits; MAJOR increments for substantive scope or control changes requiring re-approval.
- All changes are tracked via Git commit history in this repository as the definitive audit trail, in addition to each document's Revision History table.
- The repository's `main` branch represents the current approved and effective set of documents; branches/PRs are used for drafts under review.

## 7. Protection, Distribution, and Retention

- **Protection**: Access to modify controlled documents is restricted to designated owners; the `main` branch is protected, requiring review/approval before merge.
- **Distribution**: Current versions are accessible to all relevant personnel via the internal ISMS documentation portal (mirrored from this repository) or, for public-classification documents, published externally.
- **External origin documents** (e.g., ISO standard text, regulator guidance, auditor certificates) are controlled by reference/link rather than reproduction, and are logged in the External Documents Register.
- **Retention**: Superseded controlled documents and audit records are retained for a minimum of **3 years** or per applicable regulatory retention requirements, whichever is longer, then securely disposed of per the Data Classification and Handling Policy.

## 8. Illegible/Obsolete Prevention

Superseded documents in the repository are moved to an `/archive` path and clearly marked "SUPERSEDED — see [current doc link]" in the document header to prevent unintended use.

## 9. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | — | ISMS Team | Initial draft |
| 1.0 | — | CISO | Approved |
