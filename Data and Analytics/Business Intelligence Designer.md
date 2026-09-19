# Business Intelligence Designer
> Transforms reporting needs into complete BI system architectures with data modeling, semantic layers, access patterns, and governance frameworks.

## Purpose
Convert basic reporting requests like "we need better insights" into comprehensive BI system designs that cover data modeling, semantic layer definitions, report hierarchies, access patterns, and self-service analytics frameworks.

## Best For
- Designing enterprise BI platforms
- Creating data models (star schema, snowflake, data vault)
- Planning self-service analytics capabilities
- Designing semantic layers and metric stores

## Prompt Enhancer
```text
You are a senior business intelligence architect. Transform the following reporting need into a comprehensive BI system design specification.

INPUT NEED:
{user_request}

OUTPUT A COMPLETE BI SYSTEM DESIGN INCLUDING:

1. BUSINESS CONTEXT AND OBJECTIVES
   - Business domains to serve (sales, marketing, finance, operations, HR)
   - Key business questions to answer
   - User personas and their analytics needs
   - Current pain points and gaps
   - Success metrics for the BI platform

2. DATA MODEL DESIGN
   For each business domain:
   
   a) CONCEPTUAL MODEL
      - Business entities and relationships
      - Grain definition (what each row represents)
      - Business keys and relationships
   
   b) LOGICAL MODEL (Star Schema)
      - Fact tables with measures and foreign keys
      - Dimension tables with attributes and hierarchies
      - Degenerate dimensions
      - Junk dimensions for flag attributes
      - Bridge tables for many-to-many relationships
   
   c) PHYSICAL MODEL
      - Table partitioning strategy
      - Indexing strategy (clustered, non-clustered, covering)
      - Materialized views and aggregation tables
      - Columnstore optimization for analytics
      - Storage optimization (compression, tiering)

3. SEMANTIC LAYER DESIGN
   - Business-friendly naming conventions
   - Metric definitions with formulas
   - Dimension hierarchies (time, geography, product, organization)
   - Derived metrics and calculated fields
   - Time intelligence (YTD, MTD, rolling averages, period-over-period)
   - Currency conversion and localization
   - Security predicates (row-level, column-level)

4. REPORT AND DASHBOARD HIERARCHY
   Tier 1: Executive Dashboards
   - Strategic KPIs and scorecards
   - Exception-based reporting
   - Trend analysis and forecasting
   
   Tier 2: Operational Dashboards
   - Real-time monitoring
   - Drill-down capabilities
   - Alerting and notifications
   
   Tier 3: Analytical Reports
   - Ad-hoc query support
   - Self-service exploration
   - Statistical analysis
   
   Tier 4: Detailed Reports
   - Transaction-level detail
   - Audit and compliance reports
   - Export and distribution

5. SELF-SERVICE ANALYTICS FRAMEWORK
   - Data catalog and discovery
   - Guided analytics templates
   - What-if analysis capabilities
   - Natural language query support
   - Data preparation tools for analysts
   - Governance guardrails

6. TECHNOLOGY STACK RECOMMENDATION
   - Data warehouse/lakehouse platform
   - ETL/ELT tools
   - BI and visualization tools
   - Semantic layer/metric store
   - Data catalog and governance tools
   - Infrastructure requirements

7. SECURITY AND ACCESS CONTROL
   - Authentication integration (SSO, MFA)
   - Authorization model (RBAC, ABAC)
   - Row-level security implementation
   - Column-level security for sensitive data
   - Data masking and anonymization
   - Audit logging and compliance

8. PERFORMANCE OPTIMIZATION
   - Query performance targets
   - Caching strategy
   - Pre-aggregation design
   - Concurrent user handling
   - Resource governance
   - Cost optimization

9. DATA GOVERNANCE INTEGRATION
   - Data quality monitoring
   - Data lineage tracking
   - Metadata management
   - Data stewardship workflows
   - Change management procedures

10. IMPLEMENTATION ROADMAP
    Phase 1: Foundation (Month 1-3)
    - Core data model
    - Essential reports
    - Basic security
    
    Phase 2: Enhancement (Month 4-6)
    - Self-service capabilities
    - Advanced analytics
    - Performance optimization
    
    Phase 3: Scale (Month 7-9)
    - Enterprise features
    - Governance framework
    - Advanced visualizations

11. SUCCESS METRICS AND KPIs
    - Platform adoption metrics
    - Query performance metrics
    - Data quality metrics
    - User satisfaction metrics
    - Business impact metrics

Format the output as a structured design document with data model diagrams, schema definitions, and configuration examples.
```

## Example
### Original Prompt
```text
We need better reporting across our sales and finance teams.
```

### Enhanced Prompt
```text
You are a senior business intelligence architect. Transform the following reporting need into a comprehensive BI system design specification.

INPUT NEED:
We need better reporting across our sales and finance teams. Sales needs pipeline visibility and finance needs revenue recognition and budget variance analysis.

OUTPUT A COMPLETE BI SYSTEM DESIGN INCLUDING:

1. BUSINESS CONTEXT AND OBJECTIVES
2. DATA MODEL DESIGN
   a) CONCEPTUAL MODEL
   b) LOGICAL MODEL (Star Schema)
   c) PHYSICAL MODEL
3. SEMANTIC LAYER DESIGN
4. REPORT AND DASHBOARD HIERARCHY
5. SELF-SERVICE ANALYTICS FRAMEWORK
6. TECHNOLOGY STACK RECOMMENDATION
7. SECURITY AND ACCESS CONTROL
8. PERFORMANCE OPTIMIZATION
9. DATA GOVERNANCE INTEGRATION
10. IMPLEMENTATION ROADMAP
11. SUCCESS METRICS AND KPIs

Format the output as a structured design document with data model diagrams, schema definitions, and configuration examples.
```

## Notes
- Specify the number of users and expected concurrent usage
- Include any existing BI tools being replaced or integrated
- Note data volume and growth rate for capacity planning
- Mention regulatory requirements (SOX, GDPR, HIPAA)

## Tags
business-intelligence, data-modeling, star-schema, semantic-layer, data-warehouse, tableau, power-bi, looker, analytics, reporting
