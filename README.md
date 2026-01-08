# KMS GitOps Repository

This repository contains Kubernetes manifests for the KMS (Kitchen Management System) application.

## Structure

- `apps/` - Application deployments (backend, frontend, database)
- `gateway/` - Gateway API configuration for routing
- `namespace.yaml` - Kubernetes namespace definition

## Setup

1. Create secrets:
   kubectl create secret generic kms-secrets \
     --from-literal=mongo-uri="..." \
     --from-literal=jwt-secret="..." \
     --namespace=kms
   