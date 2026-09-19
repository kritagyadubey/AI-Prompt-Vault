# Data Pipeline Designer
> Transforms vague data movement requests into comprehensive pipeline architecture specifications with schema definitions, orchestration logic, and failure handling.

## Purpose
Convert casual requests like "move data from A to B" into detailed pipeline blueprints that cover source ingestion, transformation logic, schema evolution, backfill strategies, monitoring, and operational runbooks—ensuring no edge case is missed before implementation begins.

## Best For
- Designing batch or streaming data pipelines
- Planning ETL/ELT workflows across heterogeneous systems
- Documenting data flow architecture for stakeholder review
- Creating pipeline specifications for engineering teams

## Prompt Enhancer
```text
You are a senior data architect tasked with designing a production-grade data pipeline. Transform the following casual request into a comprehensive pipeline architecture specification.

INPUT REQUEST:
{user_request}

OUTPUT A COMPLETE PIPELINE SPEC INCLUDING:

1. EXECUTIVE SUMMARY
   - Business objective this pipeline serves
   - Data domain and criticality level (Tier 1/2/3)
   - Expected data volume and velocity
   - SLA requirements (freshness, completeness, latency)

2. SOURCE SYSTEM ANALYSIS
   - Source system type (RDBMS, API, file, event stream, SaaS)
   - Connection method and authentication pattern
   - Source schema with data types and constraints
   - Change data capture (CDC) strategy if applicable
   - Source reliability assessment and expected downtime windows
   - Rate limits, quotas, or throttling considerations

3. DESTINATION SYSTEM DESIGN
   - Target system (data warehouse, data lake, lakehouse, operational store)
   - Target schema with partitioning and clustering strategy
   - Slowly changing dimension (SCD) approach (Type 1/2/3)
   - Indexing and materialized view considerations
   - Data retention and archival policy

4. TRANSFORMATION LOGIC
   - Raw → Bronze → Silver → Gold layer transformations (if lakehouse)
   - Column-level transformations with explicit formulas
   - Data type casting and normalization rules
   - Deduplication strategy (exact vs. approximate, window size)
   - Null handling and default value policies
   - Business rule validations and data contracts

5. SCHEMA MANAGEMENT
   - Schema registry strategy
   - Schema evolution handling (additive, breaking, backward-compatible)
   - Column addition/removal/rename procedures
   - Data type change migration path

6. ORCHESTRATION DESIGN
   - Scheduling pattern (cron, event-driven, SLA-based)
   - Dependency graph with task-level DAG
   - Idempotency guarantees per task
   - Backfill and replay strategy
   - Concurrent execution limits and resource contention

7. ERROR HANDLING AND RECOVERY
   - Retry policy per task (exponential backoff, max retries)
   - Dead letter queue design
   - Partial failure handling
   - Data quality gate checkpoints
   - Rollback and recovery procedures
   - Alerting thresholds and escalation paths

8. MONITORING AND OBSERVABILITY
   - Key metrics (row counts, latency, freshness, error rate)
   - Data freshness SLA monitoring
   - Volume anomaly detection thresholds
   - Log aggregation strategy
   - Dashboard and alerting configuration

9. SECURITY AND COMPLIANCE
   - Data classification (PII, PHI, financial, public)
   - Encryption at rest and in transit
   - Access control and least-privilege principles
   - Audit logging requirements
   - Data masking or tokenization rules
   - GDPR/CCPA right-to-deletion handling

10. COST ESTIMATION
    - Compute resources required per stage
    - Storage costs (raw + transformed)
    - Network transfer costs
    - Third-party connector costs
    - Total estimated monthly cost

11. OPERATIONAL RUNBOOK
    - Common failure scenarios and resolution steps
    - Manual intervention procedures
    - Emergency kill-switch procedures
    - Capacity planning triggers
    - Decommissioning checklist

Format the output as a structured technical specification document with clear section headers, tables where appropriate, and code blocks for any SQL, Python, or configuration snippets.
```

## Example
### Original Prompt
```text
We need to move customer data from our PostgreSQL database into Snowflake every night so the analytics team can build reports.
```

### Enhanced Prompt
```text
You are a senior data architect tasked with designing a production-grade data pipeline. Transform the following casual request into a comprehensive pipeline architecture specification.

INPUT REQUEST:
Move customer data from PostgreSQL to Snowflake nightly for analytics reporting.

OUTPUT A COMPLETE PIPELINE SPEC INCLUDING:

1. EXECUTIVE SUMMARY
   - Business objective this pipeline serves
   - Data domain and criticality level (Tier 1/2/3)
   - Expected data volume and velocity
   - SLA requirements (freshness, completeness, latency)

2. SOURCE SYSTEM ANALYSIS
   - Source system type (RDBMS, API, file, event stream, SaaS)
   - Connection method and authentication pattern
   - Source schema with data types and constraints
   - Change data capture (CDC) strategy if applicable
   - Source reliability assessment and expected downtime windows
   - Rate limits, quotas, or throttling considerations

3. DESTINATION SYSTEM DESIGN
   - Target system (data warehouse, data lake, lakehouse, operational store)
   - Target schema with partitioning and clustering strategy
   - Slowly changing dimension (SCD) approach (Type 1/2/3)
   - Indexing and materialized view considerations
   - Data retention and archival policy

4. TRANSFORMATION LOGIC
   - Raw → Bronze → Silver → Gold layer transformations (if lakehouse)
   - Column-level transformations with explicit formulas
   - Data type casting and normalization rules
   - Deduplication strategy (exact vs. approximate, window size)
   - Null handling and default value policies
   - Business rule validations and data contracts

5. SCHEMA MANAGEMENT
   - Schema registry strategy
   - Schema evolution handling (additive, breaking, backward-compatible)
   - Column addition/removal/rename procedures
   - Data type change migration path

6. ORCHESTRATION DESIGN
   - Scheduling pattern (cron, event-driven, SLA-based)
   - Dependency graph with task-level DAG
   - Idempotency guarantees per task
   - Backfill and replay strategy
   - Concurrent execution limits and resource contention

7. ERROR HANDLING AND RECOVERY
   - Retry policy per task (exponential backoff, max retries)
   - Dead letter queue design
   - Partial failure handling
   - Data quality gate checkpoints
   - Rollback and recovery procedures
   - Alerting thresholds and escalation paths

8. MONITORING AND OBSERVABILITY
   - Key metrics (row counts, latency, freshness, error rate)
   - Data freshness SLA monitoring
   - Volume anomaly detection thresholds
   - Log aggregation strategy
   - Dashboard and alerting configuration

9. SECURITY AND COMPLIANCE
   - Data classification (PII, PHI, financial, public)
   - Encryption at rest and in transit
   - Access control and least-privilege principles
   - Audit logging requirements
   - Data masking or tokenization rules
   - GDPR/CCPA right-to-deletion handling

10. COST ESTIMATION
    - Compute resources required per stage
    - Storage costs (raw + transformed)
    - Network transfer costs
    - Third-party connector costs
    - Total estimated monthly cost

11. OPERATIONAL RUNBOOK
    - Common failure scenarios and resolution steps
    - Manual intervention procedures
    - Emergency kill-switch procedures
    - Capacity planning triggers
    - Decommissioning checklist

Format the output as a structured technical specification document with clear section headers, tables where appropriate, and code blocks for any SQL, Python, or configuration snippets.
```

## Notes
- Always specify whether the pipeline is batch or streaming in the original request
- Include data volume estimates for accurate resource planning
- Consider mentioning compliance requirements (GDPR, HIPAA, PCI-DSS) upfront
- The more source/destination details provided, the more actionable the output

## Tags
data-pipeline, etl, elt, data-architecture, orchestration, data-engineering, snowflake, postgresql, streaming, batch-processing
