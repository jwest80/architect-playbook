# Secrets Management & Rotation

## Business Problem

Applications often need credentials, API keys, certificates, and connection strings. Storing those values in source control, configuration files, build variables, or developer machines creates security and compliance risk.

## Why It Matters

Secrets need centralized storage, controlled access, audit trails, and rotation. A good secrets pattern reduces blast radius and helps teams move away from long-lived credentials.

## Azure Services

- Azure Key Vault
- Managed Identity
- Azure App Configuration
- Azure Container Apps
- Azure Monitor

## AWS Equivalents

- AWS Secrets Manager
- AWS Systems Manager Parameter Store
- IAM Roles
- AWS CloudTrail
- Amazon CloudWatch

## POC Idea

Deploy a small .NET application to Azure Container Apps that reads a database connection string from Azure Key Vault using Managed Identity. Add a rotation exercise that updates the secret without rebuilding the app.

## Production Checklist

- [ ] Secrets are not stored in source control.
- [ ] Workloads use managed identity or workload identity where possible.
- [ ] Secret access is scoped by least privilege.
- [ ] Secret reads and changes are audited.
- [ ] Rotation process is documented and tested.
- [ ] Alerting exists for suspicious access or failed retrievals.

