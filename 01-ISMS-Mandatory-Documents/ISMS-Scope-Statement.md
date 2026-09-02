# ISMS Scope Statement

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-DOC-001 |
| ISO 27001:2022 Clause | 4.3 |
| Owner | Chief Information Security Officer (CISO) |
| Status | Approved |
| Version | 1.0 |
| Classification | Internal |
| Review Cycle | Annual, or on significant change |

## 1. Purpose

This document defines the boundaries and applicability of the Information Security Management System (ISMS) of Meridian Financial Group (FFG), in accordance with ISO/IEC 27001:2022 Clause 4.3, taking into account the external and internal issues referred to in Clause 4.1 and the requirements of interested parties referred to in Clause 4.2.

## 2. Scope Statement

The ISMS covers the design, development, delivery, and support of FFG's digital banking and payment processing services, including:

- **Core Banking Platform** — account management, transaction processing, and ledger systems (production and DR environments)
- **Payment Gateway** — card and account-to-account payment processing, including PCI-DSS-relevant components
- **Corporate IT Infrastructure** — internal networks, identity and access management, endpoint fleet, and corporate email/collaboration systems
- **Cloud Environments** — production and staging workloads hosted in the organization's public cloud provider(s), and associated cloud identity, networking, and storage services
- **Supporting Business Functions** — Software Engineering, IT Operations, Information Security, Risk & Compliance, Customer Support (to the extent they access in-scope systems or data), and Human Resources (to the extent of personnel security controls)

### 2.1 Locations In Scope

- FFG Head Office (primary data processing and corporate functions)
- Primary Data Center (core banking and payment production systems)
- Disaster Recovery (DR) site
- Cloud regions used for production and DR cloud workloads

### 2.2 Explicitly Excluded from Scope

- Marketing website and public-facing informational content hosted outside the corporate network, which does not process customer authentication credentials, account data, or payment data
- Physical branch locations that do not host in-scope IT systems (branches interacting with in-scope systems via the corporate network remain in scope for access and physical entry controls at the branch perimeter only)
- Third-party SaaS tools used solely for non-customer-data business functions (e.g., internal HR payroll processing) are excluded from the ISMS scope but are subject to the Supplier Relationships process under Annex A.5.19–5.23

> **Audit note:** Any exclusion must be justified and must not affect FFG's ability to provide information security that meets requirements determined by risk assessment and applicable legal, regulatory, or contractual obligations (Clause 4.3, final paragraph). Exclusions above are justified on the basis that excluded assets do not store, process, or transmit customer authentication data, account data, cardholder data, or other information assets identified in the Risk Register.

## 3. Interfaces and Dependencies

Where in-scope systems interface with out-of-scope environments (e.g., third-party payment processors, correspondent banks, cloud provider shared-responsibility boundary), the interface itself — and the controls governing data crossing that interface — is in scope, even though the counterparty system is not.

## 4. Basis for Scope Determination

This scope was determined with reference to:

1. **Clause 4.1** — External and internal issues (see Context of the Organization Register, `05-Policies-and-Procedures`)
2. **Clause 4.2** — Requirements of interested parties (regulators, customers, card networks, shareholders, employees)
3. **Interfaces and dependencies** between FFG and services performed by other organizations (outsourced infrastructure hosting, cloud provider)

## 5. Approval

| Role | Name/Placeholder | Date |
|---|---|---|
| CISO | [Insert Name] | [Insert Date] |
| CEO / Top Management | [Insert Name] | [Insert Date] |

## 6. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 0.1 | — | ISMS Team | Initial draft |
| 1.0 | — | CISO | Approved by top management |
