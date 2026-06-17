# GitHub Actions + Azure CI/CD

## Business Problem

Manual build and deployment steps are slow, inconsistent, and difficult to audit. Teams need an automated pipeline that validates, packages, and deploys applications safely.

## Why It Matters

CI/CD creates repeatability and traceability. It also provides a natural place for tests, security checks, infrastructure validation, approvals, and environment promotion.

## Azure Services

- GitHub Actions
- Azure Container Registry
- Azure Container Apps
- Azure Key Vault
- Azure Resource Manager
- Federated credentials with workload identity

## AWS Equivalents

- GitHub Actions
- Amazon ECR
- Amazon ECS Fargate
- AWS Secrets Manager
- AWS CloudFormation or CDK
- OpenID Connect to IAM Role

## POC Idea

Create a GitHub Actions workflow that builds a .NET API, runs tests, builds a container image, pushes it to Azure Container Registry, and deploys to Azure Container Apps using OpenID Connect instead of stored Azure credentials.

## Production Checklist

- [ ] Pipeline uses environment-specific approvals where needed.
- [ ] Cloud authentication uses federated identity.
- [ ] Build and deployment permissions are separated.
- [ ] Tests run before deployment.
- [ ] Deployment logs are retained.
- [ ] Secrets are not exposed in workflow output.

