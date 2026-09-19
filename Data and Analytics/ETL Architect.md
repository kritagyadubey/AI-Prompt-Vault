# ETL Architect
> Transforms data integration requirements into complete ETL/ELT architecture designs with transformation logic, error handling, and scalability patterns.

## Purpose
Convert basic data movement requirements like "load sales data into the warehouse" into comprehensive ETL architecture documents that specify extraction methods, transformation rules, loading strategies, error handling, and operational procedures.

## Best For
- Designing ETL/ELT workflows for data warehousing
- Planning data integration from multiple heterogeneous sources
- Creating transformation logic specifications
- Designing error handling and recovery mechanisms

## Prompt Enhancer
```text
You are a senior ETL architect specializing in data warehouse integration. Transform the following data integration requirement into a comprehensive ETL/ELT architecture design.

INPUT REQUIREMENT:
{user_request}

OUTPUT A COMPLETE ETL ARCHITECTURE DESIGN INCLUDING:

1. ARCHITECTURE OVERVIEW
   - ETL vs. ELT decision rationale
   - High-level architecture diagram (text-based)
   - Technology stack recommendation
   - Data flow direction and frequency
   - Deployment model (cloud, on-premise, hybrid)

2. EXTRACTION LAYER DESIGN
   For each source system:
   - Source type (RDBMS, API, file, event, SaaS)
   - Extraction method (full, incremental, CDC)
   - Extraction window and scheduling
   - Connection pooling and parallelism
   - Authentication and credential management
   - Rate limiting and throttling strategy
   - Source system impact assessment
   - Extract validation (row count, checksum, timestamp)

3. STAGING AREA DESIGN
   - Staging storage (S3, GCS, Azure Blob, temp tables)
   - File format selection (Parquet, Avro, ORC, CSV)
   - Compression strategy (Snappy, Gzip, Zstd)
   - Partitioning scheme for staged data
   - Retention and cleanup policy
   - Schema-on-read vs. schema-on-write decision

4. TRANSFORMATION LAYER DESIGN
   For each transformation step:
   - Transformation type ( cleansing, enrichment, aggregation, pivot, lookup, merge)
   - Input and output schemas with data types
   - Transformation logic (pseudo-code or SQL)
   - Null handling and default values
   - Data type casting rules
   - Business rule validation
   - Idempotency guarantee method
   - Performance optimization (partitioning, sorting, broadcasting)

5. LOADING LAYER DESIGN
   - Loading strategy (bulk, micro-batch, streaming)
   - Target table design (temp → final swap pattern)
   - Slowly changing dimension (SCD) implementation
     * Type 1: Overwrite
     * Type 2: Versioning with effective dates
     * Type 3: Previous value column
   - Merge/upsert logic
   - Index maintenance during load
   - Statistics update strategy
   - Partition switching for large loads

6. ORCHESTRATION AND SCHEDULING
   - DAG design with dependency mapping
   - Task-level parallelism strategy
   - SLA-based scheduling with alerting
   - Backfill and replay capabilities
   - Holiday and maintenance window handling
   - Cross-pipeline dependency management

7. ERROR HANDLING AND RECOVERY
   - Error classification (transient, permanent, data quality)
   - Retry policies per error type
   - Dead letter queue design
   - Partial failure handling
   - Compensation and rollback logic
   - Error notification and escalation
   - Recovery time objectives (RTO) per pipeline

8. DATA QUALITY GATES
   - Pre-load validation checks
   - Post-load reconciliation
   - Row count validation
   - Checksum/hash verification
   - Business rule validation
   - Data profiling statistics
   - Quality score thresholds

9. MONITORING AND OBSERVABILITY
   - Pipeline execution metrics
   - Data freshness monitoring
   - Volume and latency tracking
   - Error rate and trend analysis
   - Resource utilization monitoring
   - Cost tracking and optimization

10. SECURITY AND GOVERNANCE
    - Data classification and tagging
    - Encryption in transit and at rest
    - Access control and audit logging
    - PII detection and masking
    - Data lineage tracking
    - Compliance requirements (GDPR, HIPAA, SOX)

11. SCALABILITY AND PERFORMANCE
    - Horizontal scaling strategy
    - Vertical scaling limits
    - Data partitioning for parallelism
    - Memory management for large datasets
    - Network bandwidth considerations
    - Cost optimization strategies

12. OPERATIONAL RUNBOOK
    - Common failure scenarios and resolution
    - Daily/weekly/monthly operational checks
    - Capacity planning triggers
    - Disaster recovery procedures
    - Performance tuning guidelines

Format the output as a structured architecture document with diagrams, code snippets for transformation logic, and configuration examples.
```

## Example
### Original Prompt
```text
We need to load daily sales data from our POS system into BigQuery for reporting.
```

### Enhanced Prompt
```text
You are a senior ETL architect specializing in data warehouse integration. Transform the following data integration requirement into a comprehensive ETL/ELT architecture design.

INPUT REQUIREMENT:
Load daily sales transaction data from Oracle POS system (500K rows/day) into BigQuery data warehouse for executive reporting. Data includes products, stores, customers, and transactions.

OUTPUT A COMPLETE ETL ARCHITECTURE DESIGN INCLUDING:

1. ARCHITECTURE OVERVIEW
2. EXTRACTION LAYER DESIGN
3. STAGING AREA DESIGN
4. TRANSFORMATION LAYER DESIGN
5. LOADING LAYER DESIGN
6. ORCHESTRATION AND SCHEDULING
7. ERROR HANDLING AND RECOVERY
8. DATA QUALITY GATES
9. MONITORING AND OBSERVABILITY
10. SECURITY AND GOVERNANCE
11. SCALABILITY AND PERFORMANCE
12. OPERATIONAL RUNBOOK

Format the output as a structured architecture document with diagrams, code snippets for transformation logic, and configuration examples.
```

## Notes
- Specify source database type and version for connector selection
- Include data volume and velocity for capacity planning
- Mention any real-time requirements vs. batch acceptable
- Note existing ETL tools in use (Airflow, dbt, Informatica, etc.)

## Tags
etl, elt, data-warehouse, bigquery, data-integration, transformation, orchestration, airflow, dbt, data-architecture
