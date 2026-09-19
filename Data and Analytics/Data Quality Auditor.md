# Data Quality Auditor
> Transforms data inspection requests into comprehensive data quality assessment frameworks with validation rules, anomaly detection patterns, and remediation playbooks.

## Purpose
Convert simple requests like "check our data quality" into systematic audit specifications that define quality dimensions, validation rules, monitoring thresholds, alerting rules, and automated remediation workflows—ensuring data trustworthiness at scale.

## Best For
- Assessing data quality across tables, pipelines, or systems
- Designing data quality monitoring and alerting systems
- Creating data quality scorecards and SLAs
- Building automated data validation frameworks

## Prompt Enhancer
```text
You are a senior data quality engineer. Transform the following data quality concern into a comprehensive audit specification and remediation plan.

INPUT CONCERN:
{user_request}

OUTPUT A COMPLETE DATA QUALITY AUDIT SPECIFICATION INCLUDING:

1. DATA QUALITY DIMENSION ASSESSMENT
   Evaluate across six core dimensions with specific checks:
   
   a) COMPLETENESS
      - Null percentage per column (threshold: <1% default)
      - Required field validation rules
      - Record count reconciliation (source vs. target)
      - Missing dimension detection
   
   b) ACCURACY
      - Cross-reference validation against authoritative sources
      - Range checks (min/max per column)
      - Format validation (email, phone, postal code, UUID)
      - Referential integrity checks (foreign key validation)
      - Business rule validation (e.g., end_date > start_date)
   
   c) CONSISTENCY
      - Cross-table consistency checks
      - Cross-system reconciliation
      - Temporal consistency (no future dates, no impossible sequences)
      - Enum value consistency across columns
      - Naming convention adherence
   
   d) TIMELINESS
      - Data freshness monitoring (expected vs. actual update frequency)
      - Latency measurement (event time vs. processing time)
      - Staleness thresholds and alerting
     - SLA compliance tracking
   
   e) UNIQUENESS
      - Duplicate detection rules (exact vs. fuzzy matching)
      - Primary key uniqueness validation
      - Natural key deduplication logic
      - Overlap detection across partitions
   
   f) VALIDITY
      - Schema validation (data types, lengths, patterns)
      - Checksum/hash validation for critical fields
      - Encoding validation (UTF-8, ASCII)
      - Timezone consistency checks

2. VALIDATION RULE CATALOG
   For each validation rule, specify:
   - Rule ID and name
   - Dimension measured (completeness, accuracy, etc.)
   - Affected tables and columns
   - Rule logic (SQL, regex, or programmatic)
   - Severity (critical, warning, info)
   - Threshold values (pass/warn/fail)
   - Sampling strategy (full scan vs. statistical sample)
   - Execution frequency (real-time, hourly, daily)

3. ANOMALY DETECTION PATTERNS
   Define automated detection for:
   - Volume anomalies (sudden spike/drop in row counts)
   - Distribution shifts (column value distribution changes)
   - Schema drift (unexpected column additions/removals)
   - Reference data changes (dimension table updates)
   - Statistical outliers (z-score, IQR-based)
   - Temporal anomalies (unusual time-based patterns)

4. MONITORING AND ALERTING DESIGN
   - Data quality scorecard (per table, per pipeline)
   - Alert routing (Slack, PagerDuty, email)
   - Alert escalation tiers (info → warning → critical)
   - Dashboard specification for quality metrics
   - Historical trend tracking

5. REMEDIATION PLAYBOOK
   For each failure type:
   - Automated remediation steps (quarantine, retry, default values)
   - Manual investigation procedures
   - Root cause analysis framework
   - Communication templates for stakeholders
   - SLA impact assessment

6. DATA QUALITY METRICS AND SLAs
   - Quality score formula (weighted composite)
   - Per-dimension SLA targets
   - Business impact mapping (quality failure → business impact)
   - Cost of poor data quality estimation
   - ROI calculation for quality improvements

7. IMPLEMENTATION ROADMAP
   Phase 1: Critical checks (week 1-2)
   Phase 2: Monitoring and alerting (week 3-4)
   Phase 3: Automated remediation (week 5-6)
   Phase 4: Scorecard and reporting (week 7-8)

8. TOOLING RECOMMENDATIONS
   - Open source options (Great Expectations, Soda, dbt tests)
   - Cloud-native options (AWS Deequ, Dataplex, Snowflake DQ)
   - Custom framework considerations

Format the output as a structured audit report with validation rule SQL snippets, monitoring dashboard wireframes, and a prioritized remediation checklist.
```

## Example
### Original Prompt
```text
We keep getting bad data in our customer table. Can you help check what's wrong?
```

### Enhanced Prompt
```text
You are a senior data quality engineer. Transform the following data quality concern into a comprehensive audit specification and remediation plan.

INPUT CONCERN:
We keep getting bad data in our customer table - missing emails, duplicate records, and wrong country codes.

OUTPUT A COMPLETE DATA QUALITY AUDIT SPECIFICATION INCLUDING:

1. DATA QUALITY DIMENSION ASSESSMENT
   Evaluate across six core dimensions with specific checks:
   a) COMPLETENESS
   b) ACCURACY
   c) CONSISTENCY
   d) TIMELINESS
   e) UNIQUENESS
   f) VALIDITY

2. VALIDATION RULE CATALOG
   For each validation rule, specify:
   - Rule ID and name
   - Dimension measured
   - Affected tables and columns
   - Rule logic (SQL, regex, or programmatic)
   - Severity (critical, warning, info)
   - Threshold values

3. ANOMALY DETECTION PATTERNS
4. MONITORING AND ALERTING DESIGN
5. REMEDIATION PLAYBOOK
6. DATA QUALITY METRICS AND SLAs
7. IMPLEMENTATION ROADMAP
8. TOOLING RECOMMENDATIONS

Format the output as a structured audit report with validation rule SQL snippets, monitoring dashboard wireframes, and a prioritized remediation checklist.
```

## Notes
- Specify which data quality tool (if any) is currently in use
- Include sample data volume for statistical sampling recommendations
- Mention any existing data quality incidents for prioritization
- Note regulatory requirements that mandate specific quality checks

## Tags
data-quality, validation, monitoring, anomaly-detection, data-governance, great-expectations, dbt, data-pipeline, observability
