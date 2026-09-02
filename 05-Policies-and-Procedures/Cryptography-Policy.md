# Cryptography Policy

| Field | Value |
|---|---|
| Document ID | FFG-ISMS-POL-009 |
| Annex A Controls | A.8.24 |
| Owner | Security Engineering Lead / CISO |
| Status | Approved |
| Version | 1.0 |
| Classification | Internal |

## 1. Purpose

Defines requirements for the use of cryptography to protect Confidential and Restricted information, addressing RISK-014 (legacy key rotation gap).

## 2. Approved Algorithms and Minimum Standards

| Use Case | Minimum Standard |
|---|---|
| Data at rest (databases, storage) | AES-256 |
| Data in transit | TLS 1.2 minimum, TLS 1.3 preferred |
| Password storage | Salted hash using a modern KDF (e.g., bcrypt/Argon2), never reversible encryption |
| Digital signatures | RSA-2048+ or ECDSA P-256+ |

Deprecated/weak algorithms (e.g., MD5, SHA-1 for integrity, RC4, SSL/early TLS) are prohibited on all in-scope systems.

## 3. Key Management

- Cryptographic keys are managed via a centralized Key Management Service (KMS) wherever technically feasible; keys are never hardcoded in source code or configuration files in plaintext.
- **Key rotation**: keys are rotated at least annually, or immediately upon suspected compromise. Legacy systems not yet migrated to centralized KMS are tracked with an explicit remediation deadline (see RISK-014, Risk Treatment Plan).
- Key access is restricted to authorized systems/personnel and independently logged.
- Key backup and recovery procedures ensure availability without weakening confidentiality (e.g., split-knowledge/dual-control for master keys where applicable).

## 4. Certificate Management

- TLS certificates are tracked in an inventory with automated expiry alerting; certificate renewal is automated where possible.
- Only certificates from trusted, approved Certificate Authorities are used for production systems.

## 5. Cryptography in Application Design

Encryption requirements are defined at the design phase per the Secure Development Policy §Requirements, particularly for any component handling Restricted data (PAN, authentication credentials, PII).

## 6. Legal and Export Considerations

Use of cryptography complies with applicable local/international regulations regarding export controls and lawful access, coordinated with Legal/Compliance.

## 7. Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.0 | — | Security Engineering Lead | Approved |
