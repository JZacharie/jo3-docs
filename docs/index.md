# GitOps - Cluster Jo3

Welcome to the documentation for the **Jo3** Kubernetes cluster. This repository serves as the source of truth for the GitOps-based deployment strategy managed by **ArgoCD**.

## 📌 Objective

To implement a complete GitOps strategy for the **Jo3** cluster, centralizing all definitions of applications, resources, and Kubernetes infrastructure in a versioned, reliable, and traceable repository.

## 🚀 Stack

- **ArgoCD** – GitOps deployment tool
- **Kustomize** – Kubernetes configuration management
- **Helm** – Application templates
- **Kubernetes** – Target cluster (Jo3)
- **Git** – Source of truth (private repository)
- **ArgoCD App of Apps** – Model for deployment hierarchization

## 🔁 GitOps Flow

1. **Commit**: You push a commit to this repository.
2. **Detect**: ArgoCD automatically detects changes.
3. **Sync**: The **Jo3** cluster applies updates with full traceability.

## 🔐 Security

This repository is **private**. Secrets are externalized via:
- **External Secrets** (synced from Vault)
- **Sealed Secrets**
- **HashiCorp Vault** for secure storage.

## 👤 Maintainer
Maintained by **Joseph ZACHARIE**.
Contact: `joseph@zacharie.org`
