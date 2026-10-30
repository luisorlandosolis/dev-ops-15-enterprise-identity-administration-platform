# Dev-Ops-15 Enterprise Identity & Administration Platform

diagrams/dev-ops-15-high-level-architecture.png

## Overview

Dev-Ops-15 is an Enterprise Identity & Administration Platform designed to automate identity lifecycle management, Active Directory provisioning, organizational unit assignment, department group assignment, home folder provisioning, access control enforcement, hybrid identity synchronization, and modern authentication services.

The platform evolved from a simple Active Directory user creation script into a centralized identity solution capable of automating employee onboarding, storage integration, authorization management, logging, and identity provider services.

---

## Portfolio Relationship

Dev-Ops-15 serves as the Identity and Access Management (IAM) platform within the broader Platform Engineering portfolio.

The platform integrates traditional Active Directory services with modern identity technologies including Microsoft Entra ID, OpenID Connect (OIDC), SAML, LDAP, LDAPS, and Keycloak.

---

## Project Origin

The project began as a PowerShell-based Active Directory user provisioning script.

As additional requirements emerged, the solution expanded into a platform that automates:

- User onboarding
- Organizational Unit placement
- Department group assignment
- Home folder creation
- ACL management
- Authentication integration
- Hybrid identity synchronization
- Identity provider services

---

## Objectives

### Completed Objectives

- Automate Active Directory user creation
- Automate OU assignment
- Automate department group assignment
- Automate home folder creation
- Automate NTFS permission assignment
- Automate operational logging
- Validate user authentication
- Validate drive mappings
- Validate hybrid identity synchronization
- Deploy Keycloak identity provider

### Future Objectives

- Complete LDAP federation
- Synchronize Active Directory users into Keycloak
- Synchronize Active Directory groups into Keycloak
- Implement OIDC authentication for applications
- Implement SAML federation
- Build enterprise authorization models
- Expand application integration

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
- WinForms GUI

### Storage Services

- SMB Shares
- NTFS ACLs
- Home Directory Services

---

## Technology Stack

### Identity

- Active Directory Domain Services (AD DS)
- Microsoft Entra ID
- Keycloak
- LDAP
- LDAPS

### Automation

- PowerShell
- Windows Forms (WinForms)

### Infrastructure

- Kubernetes
- Ingress NGINX
- Kyverno

### Storage

- SMB
- NTFS Permissions
- Home Directory Services

### Authentication Protocols

- OpenID Connect (OIDC)
- SAML 2.0
- LDAP
- LDAPS

---

## Architecture

### Enterprise Identity Architecture

```text
Administrator
      ↓
Dev-Ops-15 GUI
      ↓
Active Directory
      ↓
OU Assignment
      ↓
Group Assignment
      ↓
Home Folder Creation
      ↓
File Server
      ↓
User Login
      ↓
G: Drive / H: Drive

                ↓

Microsoft Entra ID
      ↓
User Synchronization
      ↓
Group Synchronization

                ↓

Keycloak
      ↓
LDAP / LDAPS
      ↓
OIDC / SAML
      ↓
Applications
```

### Identity Provider Architecture

```text
User
      ↓
Application
      ↓
Keycloak
      ↓
LDAP / LDAPS
      ↓
Active Directory
      ↓
Authentication
      ↓
OIDC Token / SAML Assertion
      ↓
Application
      ↓
RBAC Authorization
      ↓
Access Granted
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
- G: Drive Validation
- H: Drive Validation

### Phase 3 - Hybrid Identity

✅ Complete

- Entra Connect Validation
- User Synchronization
- Group Synchronization
- Group Membership Synchronization

### Phase 4 - Identity Provider Platform

🟨 In Progress

Completed:

- Keycloak Deployed
- SOLIS Realm Created
- Admin Account Created
- Bootstrap Password Replaced
- LDAP Provider Created
- LDAP Connectivity Validated
- LDAPS Connectivity Validated
- Root Cause Identified

---

## Validation

### Identity Automation

- User Creation Validated
- OU Placement Validated
- Group Assignment Validated
- Logging Validated

### Access Validation

- Home Folder Provisioning Validated
- ACL Assignment Validated
- G: Drive Validation
- H: Drive Validation

### Hybrid Identity Validation

- Entra User Synchronization
- Entra Group Synchronization
- Group Membership Synchronization

### Identity Provider Validation

- Keycloak Deployment
- Realm Administration
- LDAP Provider Connectivity
- LDAPS Connectivity

---

## Current Status

Current LDAP federation status:

✅ LDAP Provider Created

✅ LDAP Connectivity Successful

✅ LDAPS Connectivity Successful

❌ LDAP Authentication Failed

Root Cause Identified:

Active Directory requires secure LDAP authentication over LDAPS.

---

## Lessons Learned

- Authentication and authorization are separate functions.
- LDAP connectivity does not guarantee authentication success.
- Hybrid identity validation requires users, groups, and memberships to synchronize successfully.
- Identity services and storage services should remain architecturally separated.
- Stateful applications require persistent storage planning.

---

## Key Outcomes

- Enterprise onboarding workflow automated.
- Home folder provisioning fully automated.
- ACL assignment automated.
- Active Directory integrated with Microsoft Entra ID.
- Keycloak established as an enterprise identity provider.
- Foundation created for OIDC and SAML federation.

---

## Future Enhancements

1. Remove old bootstrap password from deployment.
2. Move credentials into Kubernetes Secret.
3. Configure LDAPS federation.
4. Validate Active Directory authentication.
5. Import Active Directory users.
6. Synchronize Active Directory groups.
7. Implement first OIDC application.
8. Implement first SAML application.
9. Add PostgreSQL backend and persistent storage.
10. Implement backup and recovery processes.

---

## Repository Structure

Repository documentation and implementation artifacts are organized into:

- docs/
- diagrams/
- kubernetes/
- scripts/
- screenshots/
- examples/

---

## Screenshots

Screenshots will be added as implementation milestones are completed.
