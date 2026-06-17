# Deploy .NET Apps to Cloud

## Business Problem

Teams need a repeatable way to deploy .NET applications to cloud infrastructure without relying on manual portal changes or machine-specific scripts.

## Why It Matters

Reliable deployments reduce downtime, configuration drift, and onboarding friction. A clear deployment pattern also makes cloud costs, scaling, security, and rollback behavior easier to reason about.

## Azure Services

- Azure Container Apps
- Azure Container Registry
- Azure Key Vault
- Managed Identity
- Azure Application Insights
- Azure Log Analytics

## AWS Equivalents

- Amazon ECS Fargate
- Amazon Elastic Container Registry
- AWS Secrets Manager
- IAM Roles
- Amazon CloudWatch
- AWS X-Ray

## POC Idea

Containerize a minimal .NET API, publish the image to Azure Container Registry, and deploy it to Azure Container Apps with environment variables and secrets provided through cloud-native configuration.

## Production Checklist

- [ ] Application is containerized with a minimal runtime image.
- [ ] Infrastructure is defined as code.
- [ ] Health checks are configured.
- [ ] Logs, metrics, and traces are available.
- [ ] Rollback strategy is documented.
- [ ] Runtime identity does not require stored cloud credentials.

