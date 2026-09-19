# Data Governance Planner
> Transforms data management concerns into comprehensive governance frameworks with policies, roles, processes, and compliance controls.

## Purpose
Convert general requests like "we need better data governance" into actionable governance frameworks that define data ownership, quality standards, access policies, compliance controls, and operational procedures—ensuring data is managed as a strategic asset.

## Best For
- Establishing enterprise data governance programs
- Creating data policies and standards documentation
- Designing data stewardship and ownership models
- Planning compliance with GDPR, CCPA, HIPAA, SOX

## Prompt Enhancer
```text
You are a senior data governance architect. Transform the following data management concern into a comprehensive data governance framework.

INPUT CONCERN:
{user_request}

OUTPUT A COMPLETE DATA GOVERNANCE FRAMEWORK INCLUDING:

1. GOVERNANCE VISION AND OBJECTIVES
   - Business drivers for governance (regulatory, operational, strategic)
   - Vision statement for data as a strategic asset
   - Measurable objectives and success criteria
   - Maturity model assessment (initial → optimized)
   - Executive sponsorship and governance charter

2. ORGANIZATIONAL STRUCTURE
   a) GOVERNANCE ROLES
      - Data Owner (business accountability)
      - Data Steward (day-to-day management)
      - Data Custodian (technical implementation)
      - Data Protection Officer (privacy/compliance)
      - Data Governance Council (steering committee)
   
   b) RESPONSIBILITY MATRIX (RACI)
      For each governance activity:
      - Accountable (single owner)
      - Responsible (doers)
      - Consulted (subject matter experts)
      - Informed (stakeholders)

3. DATA CLASSIFICATION AND TAGGING
   Classification levels:
   - Public: No restrictions
   - Internal: Employee access only
   - Confidential: Role-based access
   - Restricted: Named individuals only
   - Highly Restricted: PII, PHI, financial
   
   Tagging requirements:
   - Business domain ownership
   - Data sensitivity level
   - Retention requirements
   - Compliance jurisdiction
   - Data quality tier

4. DATA QUALITY MANAGEMENT
   - Quality dimensions and metrics
   - Quality ownership and accountability
   - Quality monitoring and alerting
   - Issue tracking and resolution
   - Quality improvement initiatives
   - Quality SLA definitions

5. DATA ACCESS AND SECURITY POLICIES
   - Access request and approval workflow
   - Role-based access control (RBAC) design
   - Privileged access management
   - Data masking and anonymization rules
   - Encryption requirements
   - Audit logging and monitoring

6. DATA LIFECYCLE MANAGEMENT
   - Data retention policies by classification
   - Archival strategies and storage tiering
   - Data disposal and destruction procedures
   - Legal hold processes
   - Backup and recovery requirements

7. METADATA MANAGEMENT
   - Business glossary definitions
   - Data catalog implementation
   - Technical metadata standards
   - Data lineage tracking
   - Impact analysis procedures
   - Metadata quality standards

8. COMPLIANCE AND REGULATORY FRAMEWORK
   For each applicable regulation:
   - GDPR (EU data protection)
   - CCPA/CPRA (California privacy)
   - HIPAA (healthcare data)
   - SOX (financial reporting)
   - PCI-DSS (payment card data)
   
   Include:
   - Specific requirements mapping
   - Control implementations
   - Audit evidence collection
   - Incident response procedures

9. DATA PRIVACY AND ETHICS
   - Privacy by design principles
   - Data minimization rules
   - Consent management
   - Right to deletion procedures
   - Ethical use guidelines
   - Bias detection and mitigation

10. VENDOR AND THIRD-PARTY DATA MANAGEMENT
    - Data sharing agreements
    - Third-party risk assessment
    - Contract requirements
    - Monitoring and audit rights
    - Offboarding procedures

11. GOVERNANCE OPERATIONS
    - Meeting cadence and forums
    - Issue escalation procedures
    - Change management process
    - Training and awareness program
    - Communication plan
    - Continuous improvement process

12. TECHNOLOGY ENABLEMENT
    - Governance tooling landscape
    - Automation opportunities
    - Integration architecture
    - Dashboard and reporting
    - Self-service capabilities

13. IMPLEMENTATION ROADMAP
    Phase 1: Foundation (0-6 months)
    Phase 2: Operationalization (6-12 months)
    Phase 3: Optimization (12-18 months)
    Phase 4: Innovation (18+ months)

14. SUCCESS METRICS
    - Adoption metrics
    - Compliance metrics
    - Quality metrics
    - Business value metrics

Format the output as a governance framework document with policy templates, role descriptions, and implementation checklists.
```

## Example
### Original Prompt
```text
We need to get our data house in order before the auditors come.
```

### Enhanced Prompt
```text
You are a senior data governance architect. Transform the following data management concern into a comprehensive data governance framework.

INPUT CONCERN:
We need to establish data governance before a SOX compliance audit in 6 months. We have customer and financial data across multiple systems.

OUTPUT A COMPLETE DATA GOVERNANCE FRAMEWORK INCLUDING:

1. GOVERNANCE VISION AND OBJECTIVES
2. ORGANIZATIONAL STRUCTURE
3. DATA CLASSIFICATION AND TAGGING
4. DATA QUALITY MANAGEMENT
5. DATA ACCESS AND SECURITY POLICIES
6. DATA LIFECYCLE MANAGEMENT
7. METADATA MANAGEMENT
8. COMPLIANCE AND REGULATORY FRAMEWORK
9. DATA PRIVACY AND ETHICS
10. VENDOR AND THIRD-PARTY DATA MANAGEMENT
11. GOVERNANCE OPERATIONS
12. TECHNOLOGY ENABLEMENT
13. IMPLEMENTATION ROADMAP
14. SUCCESS METRICS

Format the output as a governance framework document with policy templates, role descriptions, and implementation checklists.
```

## Notes
- Specify the regulatory environment (GDPR, HIPAA, SOX, PCI-DSS)
- Include organization size and data complexity
- Note current governance maturity level
- Mention any existing policies or standards to build upon

## Tags
data-governance, compliance, data-quality, privacy, gdpr, hipaa, sox, data-stewardship, metadata, data-catalog
