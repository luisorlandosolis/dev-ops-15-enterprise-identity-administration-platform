# Dev-Ops-15 Enterprise Identity & Administration Platform

diagrams/dev-ops-15-high-level-architecture.png

## Overview

Dev-Ops-15 is an Enterprise Identity & Administration Platform designed to automate identity lifecycle management, directory services provisioning, organizational unit assignment, department group assignment, home folder provisioning, access control enforcement, hybrid identity synchronization, identity federation, and modern authentication services.

The platform evolved from a user provisioning script into a centralized identity platform providing automated onboarding, storage integration, hybrid identity synchronization, enterprise identity federation, persistence, certificate trust management, LDAP integration, OIDC, and SAML capabilities.

---

## Portfolio Relationship

Dev-Ops-15 serves as the Identity and Access Management (IAM) platform within the broader Platform Engineering portfolio.

The platform bridges traditional directory services and modern authentication technologies including:

- Microsoft Entra ID
- LDAP
- LDAPS
- OIDC
- SAML
- Keycloak

---

## Project Origin

The project began as a PowerShell-based user provisioning solution.

As additional requirements emerged, the platform expanded to provide:

- Automated onboarding
- Organizational Unit placement
- Department group assignment
- Home folder provisioning
- ACL management
- Hybrid identity integration
- Identity federation
- Single Sign-On services

---

## Objectives

### Completed Objectives

- Automate user creation
- Automate OU assignment
- Automate department group assignment
- Automate home folder creation
- Automate ACL assignment
- Implement operational logging
- Validate drive mappings
- Validate hybrid identity synchronization
- Deploy enterprise identity provider
- Implement LDAP federation
- Implement LDAPS authentication
- Implement user synchronization
- Implement persistent identity services

### Future Objectives

- Implement OIDC authentication for enterprise applications
- Implement SAML federation for enterprise applications
- Design authorization models
- Implement role mapping strategies
- Implement group-based authorization
- Expand enterprise application integrations
- Mature identity governance processes

---

## Environment

### Identity Services

- Active Directory
- Microsoft Entra ID
- Keycloak
- LDAP
- LDAPS

### Platform Services

- Kubernetes
- Ingress NGINX
- Kyverno

### Administration Services

- PowerShell
- WinForms

### Storage Services

- SMB
- NTFS Permissions
- Home Directory Services

### Data Services

- PostgreSQL
- Persistent Storage

---

## Technology Stack

### Identity

- Active Directory Domain Services
- Microsoft Entra ID
- Keycloak
- LDAP
- LDAPS

### Automation

- PowerShell
- Windows Forms

### Infrastructure

- Kubernetes
- Ingress NGINX
- PostgreSQL
- SMB CSI Storage
- Kyverno

### Authentication Protocols

- LDAP
- LDAPS
- OIDC
- SAML 2.0

---

## Architecture

### Enterprise Identity Platform

```text
Directory Services Platform
│
├─ DNS
├─ Certificate Services
├─ LDAPS
├─ Users
├─ Groups
│
▼

Enterprise Identity Platform
│
├─ Enterprise Realm
├─ LDAP Federation
├─ User Synchronization
├─ Trust Infrastructure
├─ PostgreSQL Persistence
│
▼

Federated Users

│

├─ OIDC Federation
└─ SAML Federation

        │
        ▼

Enterprise Applications
```

### Identity Flow

```text
User
      ↓
Enterprise Application
      ↓
Identity Provider
      ↓
Directory Services

Authentication
      ↓

OIDC Token
or
SAML Assertion

      ↓

Application Access
```

---

## Implementation

### Phase 1 - Identity Lifecycle Automation

✅ Complete

- WinForms GUI
- User Creation
- OU Assignment
- Group Assignment
- Logging
- Validation

### Phase 2 - Folder & Access Automation

✅ Complete

- Home Folder Creation
- File Server Integration
- ACL Automation
- Drive Validation
- Access Validation

### Phase 3 - Hybrid Identity

✅ Complete

- User Synchronization
- Group Synchronization
- Membership Synchronization
- Cloud Identity Integration

### Phase 4 - Identity Provider Foundation

✅ Complete

- Keycloak Deployment
- Enterprise Realm Configuration
- PostgreSQL Persistence
- Truststore Configuration
- LDAPS Authentication
- LDAP Federation
- User Synchronization
- Administrative Access
- Imported User Validation

### Phase 5 - Application SSO

🟨 In Progress

Current Focus:

- Grafana OIDC Integration

Completed:

- Application Routing
- Reverse Proxy Configuration
- Application Reachability Validation

Current Tasks:

- Create OIDC Client
- Configure OAuth Integration
- Validate Authentication
- Validate Claims
- Validate Logout
- Validate Dashboard Access

---

## Validation

### Identity Automation

- User Creation Validation
- OU Placement Validation
- Group Assignment Validation
- Logging Validation

### Access Validation

- Home Folder Provisioning Validation
- ACL Assignment Validation
- Drive Access Validation

### Hybrid Identity Validation

- User Synchronization Validation
- Group Synchronization Validation
- Membership Synchronization Validation

### Identity Provider Validation

- Keycloak Deployment
- PostgreSQL Persistence
- Persistent Storage
- Truststore Configuration
- LDAP Connectivity
- LDAPS Connectivity
- LDAP Authentication
- User Synchronization
- Imported User Validation
- Administrative Access

---

## Current Status

### Identity Foundation

✅ Operational

Validated:

- PostgreSQL Persistence
- Trust Infrastructure
- LDAPS
- LDAP Federation
- User Synchronization
- Administrative Access
- Imported Users

### Current Work

🟨 Grafana OIDC Integration

Next:

- Create OIDC Client
- Configure OAuth
- Validate Authentication
- Validate Claims
- Validate Logout
- Validate Dashboard Access

---

## Lessons Learned

- Authentication and authorization are separate functions.
- LDAP connectivity does not guarantee successful authentication.
- Hybrid identity validation requires user, group, and membership synchronization.
- Persistence must be validated rather than assumed.
- PKIX failures often indicate trust infrastructure issues.
- Trust validation and hostname validation are independent controls.
- Identity providers depend on multiple platform services operating correctly.
- Federation requires more than network connectivity.

---

## Key Outcomes

- Automated onboarding workflow implemented.
- Home folder provisioning automated.
- Access control assignment automated.
- Hybrid identity synchronization validated.
- Enterprise identity provider established.
- PostgreSQL-backed persistence implemented.
- LDAPS federation operational.
- User synchronization operational.
- Foundation established for enterprise SSO.

---

## Future Enhancements

1. Complete Grafana OIDC integration.
2. Validate OIDC claims and authentication flows.
3. Implement Jenkins SAML federation.
4. Design authorization strategy.
5. Implement role mapping.
6. Implement group mapping.
7. Expand OIDC integrations.
8. Expand SAML integrations.
9. Mature identity governance processes.

---

## Repository Structure

```text
docs/
diagrams/
kubernetes/
scripts/
screenshots/
examples/
```

---

## Screenshots

Screenshots will be added as implementation milestones are completed.

Planned screenshots:

- Identity Platform GUI
- User Provisioning Validation
- Home Folder Provisioning
- Hybrid Identity Validation
- Identity Provider Administration
- LDAP Federation
- User Synchronization
- Grafana OIDC Authentication
- SAML Federation Validation
