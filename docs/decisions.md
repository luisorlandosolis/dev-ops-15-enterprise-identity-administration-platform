# Architecture Decisions

## ADR-001

### Title

Identity Services Separated From Storage Services

### Decision

Identity services and storage services will operate as separate platform components.

### Rationale

Directory services, authentication, DNS, certificate services, and policy management have different operational requirements than user data storage and file services.

### Benefits

- Reduced platform coupling
- Improved scalability
- Easier troubleshooting
- Clear service ownership

---

## ADR-002

### Title

Hybrid Identity Architecture

### Decision

The platform will integrate on-premises identity services with cloud identity services.

### Rationale

Modern identity platforms require synchronized identities across multiple authentication platforms.

### Benefits

- Unified identity lifecycle
- Consistent group management
- Future federation support
- Simplified administration

---

## ADR-003

### Title

Enterprise Identity Provider Platform

### Decision

A dedicated identity provider platform will provide federation, authentication, and single sign-on services.

### Rationale

Modern enterprise applications require standards-based authentication services including:

- LDAP Federation
- OIDC
- SAML

### Benefits

- Centralized authentication
- Application federation
- Single Sign-On
- Standards-based architecture

---

## ADR-004

### Title

Documentation Sanitization Standard

### Decision

Repository documentation will remain sanitized.

### Requirements

Do not document:

- Real IP addresses
- Real hostnames
- Real domain names
- Real usernames
- Real email addresses
- Internal URLs
- Tenant identifiers
- Client identifiers
- Passwords
- Secrets
- Certificates
- Environment-identifying information

### Benefits

- Security
- Public release readiness
- Consistent portfolio standards
- Easier publication

---

## ADR-005

### Title

PostgreSQL Required For Identity Persistence

### Decision

The identity provider platform will utilize PostgreSQL as the persistence layer.

### Rationale

The embedded application database does not provide the persistence requirements expected of enterprise identity services.

### Benefits

- Persistent realms
- Persistent users
- Persistent federation settings
- Backup capability
- Recovery capability
- Platform resiliency

---

## ADR-006

### Title

Persistent Storage Required For Identity Services

### Decision

Identity platform data will be stored on persistent storage rather than ephemeral container storage.

### Rationale

Realm configuration, federation settings, users, and authentication services are critical platform data and must survive container recreation.

### Benefits

- Data durability
- Platform stability
- Recovery capability
- Reduced operational risk

---

## ADR-007

### Title

Secure Directory Federation

### Decision

Directory federation will use LDAPS rather than unsecured LDAP.

### Rationale

Directory authentication requires encrypted communication and certificate validation.

### Benefits

- Secure credential transmission
- Encrypted directory communications
- Standards compliance
- Enterprise security alignment

---

## ADR-008

### Title

Custom Trust Infrastructure

### Decision

The identity provider platform will trust the internal certificate authority through an explicitly configured truststore.

### Rationale

Secure federation depends upon successful certificate chain validation.

### Benefits

- Trusted LDAPS communication
- Secure federation
- Certificate lifecycle support
- Internal PKI integration

---

## ADR-009

### Title

Dedicated Service Account For Federation

### Decision

Federation services will use a dedicated directory service account.

### Rationale

Service integrations should not rely on administrator accounts or user identities.

### Benefits

- Principle of least privilege
- Improved auditing
- Reduced operational risk
- Easier credential management

---

## ADR-010

### Title

Directory Services As Source Of Truth

### Decision

Directory services remain the authoritative identity source.

### Rationale

The identity provider platform consumes identities from directory services but does not replace directory services.

### Benefits

- Centralized identity management
- Consistent user lifecycle
- Consistent group lifecycle
- Simplified governance

---

## ADR-011

### Title

OIDC As Primary Application Federation Method

### Decision

OIDC will serve as the primary authentication protocol for modern applications.

### Rationale

OIDC is broadly supported across modern platforms and integrates well with web applications.

### Initial Targets

- Grafana
- ArgoCD
- Future platform services

### Benefits

- Modern authentication
- Token-based federation
- Simplified integration
- Standards compliance

---

## ADR-012

### Title

SAML Retained For Enterprise Compatibility

### Decision

SAML federation will be maintained for applications requiring enterprise federation support.

### Rationale

Many enterprise applications continue to rely on SAML authentication.

### Initial Target

- Jenkins

### Benefits

- Enterprise compatibility
- Federation flexibility
- Broader application support
