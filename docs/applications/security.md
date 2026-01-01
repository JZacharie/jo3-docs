# Security & Infrastructure

Core security and identity management services.

## HashiCorp Vault
- **URL**: `vault.p.zacharie.org`
- **Description**: Secrets management, encryption as a service, and identity management.
- **Role**: Stores all sensitive credentials (database passwords, API keys) which are synced to Kubernetes Secrets via External Secrets Operator.

## Keycloak
- **URL**: `keycloak.p.zacharie.org`
- **Description**: Identity and Access Management (IAM).
- **Role**: Provides Single Sign-On (SSO) via OIDC for applications like Outline, Grafana, and potentially others.

## Trivy Operator
- **Description**: Continuous security scanning for Kubernetes. Scans container images for vulnerabilities and checks configuration issues.
