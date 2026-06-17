# AWS Reference

Use this page to collect AWS notes, commands, naming conventions, service limits, and implementation links.

## Common Services

| Concept | AWS Service | Notes |
| --- | --- | --- |
| Secret storage | AWS Secrets Manager | Store and rotate secrets. |
| Workload identity | IAM Role | Assign permissions to services and workloads. |
| Container hosting | ECS Fargate | Run containers without managing servers. |
| Monitoring | CloudWatch | Logs, metrics, alarms, and dashboards. |

## Useful Commands

```powershell
aws sts get-caller-identity
aws configure list
```

