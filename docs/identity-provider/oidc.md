# OIDC Federation

## Overview

OpenID Connect (OIDC) provides modern authentication services for enterprise applications.

OIDC is the primary authentication protocol for modern web applications within the platform.

---

## Architecture

```text
User
      ↓
Application
      ↓
Identity Provider
      ↓
Directory Services

Authentication
      ↓

OIDC Token
      ↓

Application Access
```

---

## Planned Integrations

### Grafana

Target:

Directory Services
↓
Identity Provider
↓
OIDC
↓
Grafana

Status:

Next Implementation

---

### Future Applications

- ArgoCD
- Additional Platform Services

---

## Validation Requirements

- Authentication Success
- Token Issuance
- User Claims
- Session Creation
- Logout Validation
