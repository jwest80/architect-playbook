# Enterprise Audit Ledger

## Business Problem

Enterprise systems need trustworthy records of important business and administrative actions. Standard application logs are often insufficient because they can be noisy, mutable, incomplete, or difficult to query for compliance.

## Why It Matters

An audit ledger supports compliance, incident response, customer support, fraud investigation, and accountability. It should answer who did what, when, from where, and why the system accepted it.

## Azure Services

- Azure SQL Database
- Azure Cosmos DB
- Azure Event Hubs
- Azure Service Bus
- Azure Storage immutable blob policies
- Azure Monitor

## AWS Equivalents

- Amazon Aurora or RDS
- Amazon DynamoDB
- Amazon Kinesis
- Amazon SQS
- S3 Object Lock
- Amazon CloudWatch

## POC Idea

Create a small API that records business actions to an append-only audit table and publishes audit events to a queue for downstream processing. Include correlation IDs, actor identity, source IP, action type, and before/after metadata where appropriate.

## Production Checklist

- [ ] Audit records are append-only.
- [ ] Actor, action, resource, timestamp, and correlation ID are captured.
- [ ] Sensitive fields are redacted or tokenized.
- [ ] Retention requirements are documented.
- [ ] Audit write failures have defined behavior.
- [ ] Access to audit data is restricted and logged.

