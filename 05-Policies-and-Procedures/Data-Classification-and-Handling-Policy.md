# Data Classification and Handling Policy

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-POL-003 |
| Annex A Controls | A.5.12, A.5.13, A.5.14, A.5.33, A.5.34, A.8.10, A.8.11, A.8.12 |
| Owner | CISO / Data Protection Officer |
| Status | Approved |
| Version | 1.0 |
| Classification | Internal |

## 1. Purpose

Establishes classification levels and corresponding handling requirements for FFG information, ensuring proportionate protection — critical for cardholder data and customer PII central to banking operations.

## 2. Classification Levels

| Level | Description | Examples |
|---|---|---|
| **Public** | Approved for public release | Marketing material, public website content |
| **Internal** | For FFG personnel; low sensitivity | Internal memos, non-sensitive process docs |
| **Confidential** | Sensitive business information | Risk register, audit reports, financial forecasts, source code |
| **Restricted** | Highest sensitivity — regulatory/contractual protection required | Customer PII, cardholder data (PAN), authentication credentials, cryptographic keys |

## 3. Labelling (A.5.13)

- Documents and systems handling Confidential/Restricted data must be labelled accordingly (header/footer for documents; tagging for structured data stores).
- Automated labelling for Restricted data is a planned enhancement (see SoA A.5.13 status).

## 4. §Transfer (A.5.14)

- Restricted data must be encrypted in transit (TLS 1.2+) and, where sent externally, only via approved secure channels (SFTP, encrypted email, or partner API with mutual TLS).
- Transfer of Restricted data to third parties requires a data processing agreement per the Supplier Relationships Policy.

## 5. §Media (A.7.10)

- Removable media use is restricted by default; exceptions require CISO approval and mandatory encryption.
- Restricted data must never be copied to unencrypted removable media or personal devices.

## 6. Masking and Leakage Prevention (A.8.11, A.8.12)

- Restricted data (e.g., PAN) must be masked or tokenized in non-production environments and in application logs — this policy is the basis for the FND-03 remediation (log redaction) and the RISK-002 treatment plan.
- DLP tooling monitors and blocks unauthorized transfer of Restricted data via email, web upload, and removable media on primary channels.

## 7. §Deletion (A.8.10)

- Data is retained only per the applicable retention schedule (see Protection of Records, A.5.33) and securely deleted (cryptographic erasure or certified destruction) once the retention period expires or a valid deletion request is received (e.g., under applicable privacy law).

## 8. Privacy and PII (A.5.34)

- Processing of customer PII follows data minimization, purpose limitation, and lawful basis principles.
- Data subject rights requests (access, correction, deletion) are routed to the Data Protection Officer / Compliance function.

## 9. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.0 | — | CISO | Approved |
