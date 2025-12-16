# idp-platform-config

This repository contains the **platform-level GitOps configuration** for an
**Internal Developer Platform (IDP)** built using **Argo CD** and **Kubernetes**.

It is the **source of truth** for:
- Argo CD applications
- Platform services (ingress, monitoring, logging)
- Environment configuration (dev, staging, prod)
- GitOps policies and boundaries

## 🚀 Platform Vision

> What if developers never had to ask DevOps again?

This repository enables:
- Self-service deployments via Git
- Automated synchronization using Argo CD
- Clear separation between platform and application ownership

## 🧱 What Lives Here

- Argo CD bootstrap and configuration
- Argo CD Applications pointing to service repos
- Shared Kubernetes platform components
- Environment-specific overlays

## 🔁 GitOps Flow

1. Changes are committed to this repository
2. Argo CD detects the change
3. Kubernetes state is automatically reconciled
4. Drift is detected and self-healed

## 🔐 Ownership

- **Platform Team** owns this repo
- Developers do **not** deploy directly to clusters
- Access is controlled via Argo CD AppProjects and RBAC
