# Monitoring and Observability Prompt Enhancer
> Transforms basic monitoring requests into comprehensive observability architectures with metrics, logs, traces, alerting, and incident response integration.

## Purpose
To convert general monitoring and observability prompts into structured observability specifications that explicitly address telemetry collection, storage, visualization, alerting, incident response, and cost optimization before any monitoring tools are deployed.

## Best For
- Application performance monitoring (APM) design
- Infrastructure monitoring and health dashboards
- Distributed tracing implementation
- Log aggregation and analysis architecture
- Alerting strategy and escalation design
- SLI/SLO/SLA definition and monitoring
- Incident response and runbook automation
- Cost optimization for observability data

## Prompt Enhancer
```text
You are a senior SRE and observability architect specializing in monitoring strategy, distributed tracing, and incident response automation. Transform the following request into a structured observability architecture specification. Follow these steps precisely:

1. OBSERVABILITY PILLARS: Design the three pillars:
   - Metrics collection strategy (infrastructure, application, business)
   - Log aggregation architecture (structured logging, levels, retention)
   - Distributed tracing implementation (context propagation, sampling)
   - Correlation strategy across metrics, logs, and traces
   - OpenTelemetry adoption and instrumentation approach
   - Vendor selection or self-hosted observability stack
   - Data retention and archival policies per pillar

2. METRICS ARCHITECTURE: Design the metrics system:
   - Metric types and naming conventions (counters, gauges, histograms)
   - RED metrics (Rate, Errors, Duration) per service
   - USE metrics (Utilization, Saturation, Errors) per resource
   - Business metrics and KPI tracking
   - Metric cardinality management and cost control
   - Metric resolution and scrape intervals
   - Metric storage and retention strategy
   - Metric aggregation and downsampling rules

3. LOGGING ARCHITECTURE: Design the logging system:
   - Structured logging format (JSON, logfmt)
   - Log level taxonomy and usage guidelines
   - Log enrichment and context propagation
   - Log routing (hot, warm, cold storage tiers)
   - Log retention policies by sensitivity and compliance
   - Log-based metrics and alerting
   - Log sampling strategy for high-volume services
   - Log query optimization and index strategy

4. DISTRIBUTED TRACING: Design the tracing system:
   - Trace context propagation standards (W3C TraceContext, B3)
   - Sampling strategy (head-based, tail-based, adaptive)
   - Instrumentation approach (auto, manual, library)
   - Span naming conventions and attribute standards
   - Trace storage and retention strategy
   - Trace-based service dependency mapping
   - Latency analysis and bottleneck identification
   - Trace sampling cost optimization

5. ALERTING STRATEGY: Design the alerting system:
   - Alert severity taxonomy (P1-P4, critical/warning/info)
   - Alert routing and escalation policies
   - Alert fatigue mitigation strategies
   - Multi-window, multi-burn-rate alerting (for SLOs)
   - Composite alerting for complex failure modes
   - Alert correlation and grouping
   - Runbook automation and remediation
   - Alert suppression and maintenance windows

6. SLI/SLO/SLA DEFINITION: Design reliability targets:
   - SLI (Service Level Indicator) definition per service
   - SLO (Service Level Objective) target selection
   - Error budget calculation and consumption tracking
   - SLA (Service Level Agreement) contractual alignment
   - SLO reporting and stakeholder communication
   - Error budget policy enforcement
   - SLO rollup and aggregation strategy
   - Multi-service SLO composition

7. DASHBOARDS AND VISUALIZATION: Design the observability UI:
   - Dashboard hierarchy (executive, operational, troubleshooting)
   - Service health overview dashboards
   - Infrastructure health dashboards
   - Application performance dashboards
   - Business metrics dashboards
   - On-call dashboards for incident response
   - Dashboard templating and reuse
   - Dashboard access control and sharing

8. INCIDENT RESPONSE INTEGRATION: Design observability for incidents:
   - Alert to incident workflow integration
   - Incident detection and declaration automation
   - Incident context enrichment from observability data
   - War room and collaboration tool integration
   - Post-incident analysis data collection
   - Incident metrics (MTTD, MTTR, MTTA)
   - Status page integration and updates
   - Customer communication automation

9. COST OPTIMIZATION: Design for observability economics:
   - Data volume analysis and reduction strategies
   - Sampling and filtering for cost control
   - Storage tiering (hot, warm, cold, archive)
   - Retention policy optimization
   - Metric and log cardinality management
   - Observability cost allocation per team/service
   - Open source vs vendor cost comparison
   - Cost anomaly detection for observability spend

10. OPERATIONAL MATURITY: Design for operational excellence:
    - Observability onboarding for new services
    - Instrumentation standards and code review requirements
    - Observability testing and validation
    - Disaster recovery for observability stack
    - Observability team structure and responsibilities
    - Training and skill development program
    - Observability maturity assessment and roadmap
    - Continuous improvement and feedback loops

Present the output as a structured observability architecture document with instrumentation examples, dashboard mockups (described textually), alert rule definitions, and operational runbook outlines for each major component.
```

## Example
### Original Prompt
```text
Set up monitoring for our microservices.
```

### Enhanced Prompt
```text
You are a senior SRE and observability architect specializing in monitoring strategy, distributed tracing, and incident response automation. Transform the following request into a structured observability architecture specification. Follow these steps precisely:

1. OBSERVABILITY PILLARS: Design the three pillars:
   - Metrics collection strategy (infrastructure, application, business)
   - Log aggregation architecture (structured logging, levels, retention)
   - Distributed tracing implementation (context propagation, sampling)
   - Correlation strategy across metrics, logs, and traces
   - OpenTelemetry adoption and instrumentation approach
   - Vendor selection or self-hosted observability stack
   - Data retention and archival policies per pillar

2. METRICS ARCHITECTURE: Design the metrics system:
   - Metric types and naming conventions (counters, gauges, histograms)
   - RED metrics (Rate, Errors, Duration) per service
   - USE metrics (Utilization, Saturation, Errors) per resource
   - Business metrics and KPI tracking
   - Metric cardinality management and cost control
   - Metric resolution and scrape intervals
   - Metric storage and retention strategy
   - Metric aggregation and downsampling rules

3. LOGGING ARCHITECTURE: Design the logging system:
   - Structured logging format (JSON, logfmt)
   - Log level taxonomy and usage guidelines
   - Log enrichment and context propagation
   - Log routing (hot, warm, cold storage tiers)
   - Log retention policies by sensitivity and compliance
   - Log-based metrics and alerting
   - Log sampling strategy for high-volume services
   - Log query optimization and index strategy

4. DISTRIBUTED TRACING: Design the tracing system:
   - Trace context propagation standards (W3C TraceContext, B3)
   - Sampling strategy (head-based, tail-based, adaptive)
   - Instrumentation approach (auto, manual, library)
   - Span naming conventions and attribute standards
   - Trace storage and retention strategy
   - Trace-based service dependency mapping
   - Latency analysis and bottleneck identification
   - Trace sampling cost optimization

5. ALERTING STRATEGY: Design the alerting system:
   - Alert severity taxonomy (P1-P4, critical/warning/info)
   - Alert routing and escalation policies
   - Alert fatigue mitigation strategies
   - Multi-window, multi-burn-rate alerting (for SLOs)
   - Composite alerting for complex failure modes
   - Alert correlation and grouping
   - Runbook automation and remediation
   - Alert suppression and maintenance windows

6. SLI/SLO/SLA DEFINITION: Design reliability targets:
   - SLI (Service Level Indicator) definition per service
   - SLO (Service Level Objective) target selection
   - Error budget calculation and consumption tracking
   - SLA (Service Level Agreement) contractual alignment
   - SLO reporting and stakeholder communication
   - Error budget policy enforcement
   - SLO rollup and aggregation strategy
   - Multi-service SLO composition

7. DASHBOARDS AND VISUALIZATION: Design the observability UI:
   - Dashboard hierarchy (executive, operational, troubleshooting)
   - Service health overview dashboards
   - Infrastructure health dashboards
   - Application performance dashboards
   - Business metrics dashboards
   - On-call dashboards for incident response
   - Dashboard templating and reuse
   - Dashboard access control and sharing

8. INCIDENT RESPONSE INTEGRATION: Design observability for incidents:
   - Alert to incident workflow integration
   - Incident detection and declaration automation
   - Incident context enrichment from observability data
   - War room and collaboration tool integration
   - Post-incident analysis data collection
   - Incident metrics (MTTD, MTTR, MTTA)
   - Status page integration and updates
   - Customer communication automation

9. COST OPTIMIZATION: Design for observability economics:
   - Data volume analysis and reduction strategies
   - Sampling and filtering for cost control
   - Storage tiering (hot, warm, cold, archive)
   - Retention policy optimization
   - Metric and log cardinality management
   - Observability cost allocation per team/service
   - Open source vs vendor cost comparison
   - Cost anomaly detection for observability spend

10. OPERATIONAL MATURITY: Design for operational excellence:
    - Observability onboarding for new services
    - Instrumentation standards and code review requirements
    - Observability testing and validation
    - Disaster recovery for observability stack
    - Observability team structure and responsibilities
    - Training and skill development program
    - Observability maturity assessment and roadmap
    - Continuous improvement and feedback loops

Set up monitoring for our microservices.

Present the output as a structured observability architecture document with instrumentation examples, dashboard mockups (described textually), alert rule definitions, and operational runbook outlines for each major component.
```

## Notes
- The three pillars (metrics, logs, traces) should be correlated — force this design decision early
- Alert fatigue is a major operational risk — the enhancer includes strategies to mitigate it
- SLI/SLO-based alerting is more reliable than threshold-based alerting for microservices
- Cost optimization is critical for observability — data volumes can grow unbounded without controls
- OpenTelemetry is the emerging standard — consider it as the default instrumentation approach

## Tags
`observability` `monitoring` `APM` `distributed-tracing` `logging` `alerting` `SLO` `SLI` `SLA` `OpenTelemetry` `Prometheus` `Grafana` `incident-response` `SRE`
