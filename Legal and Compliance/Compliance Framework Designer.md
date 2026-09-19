# Compliance Framework Designer
> Transforms regulatory requirements into actionable compliance framework blueprints with controls, policies, and audit trails.

## Purpose
This enhancer converts vague compliance needs into structured framework design instructions that map regulations to controls, policies, roles, and monitoring mechanisms. It forces identification of applicable regulations, gap analysis, control mapping, and implementation roadmaps that transform abstract regulatory obligations into operational reality.

## Best For
- Organizations entering new regulated markets (HIPAA, GDPR, SOC 2, ISO 27001)
- Startups building compliance programs from scratch
- Companies upgrading from informal to formal compliance structures
- Pre-audit preparation and gap remediation
- Multi-framework compliance mapping and overlap reduction

## Prompt Enhancer
```text
I need you to act as a compliance framework architect. Transform the following compliance requirement into a detailed, structured framework design instruction. DO NOT execute the design yourself — instead, produce a comprehensive prompt that instructs an AI to design a complete compliance framework.

For the given regulatory requirement, your enhanced prompt MUST include ALL of the following elements:

1. ORGANIZATIONAL PROFILE: Define the entity subject to compliance:
   - Legal entity name, type, and jurisdiction(s) of operation
   - Industry vertical and NAICS/SIC code
   - Number of employees and geographic footprint
   - Data types processed (PII, PHI, financial, intellectual property)
   - Third-party relationships and data flow map
   - Existing certifications and compliance history

2. REGULATORY SCOPE MAPPING: Identify ALL applicable regulations:
   - Primary regulation(s) with specific article/section references
   - Secondary/overlapping frameworks (e.g., GDPR + CCPA + PIPEDA)
   - Industry-specific requirements (HIPAA for healthcare, PCI DSS for payments)
   - Cross-border data transfer obligations (SCCs, BCRs, adequacy decisions)
   - Enforcement mechanisms and penalty structures
   - Recent enforcement actions relevant to the organization

3. GAP ANALYSIS FRAMEWORK: Design the assessment methodology:
   - Current-state documentation review checklist
   - Control inventory template (existing controls mapped to requirements)
   - Risk assessment methodology (qualitative/quantitative/hybrid)
   - Maturity model scale (1-5 or CMM levels) for each control domain
   - Gap severity classification (critical/high/medium/low)
   - Remediation priority ranking criteria

4. CONTROL ARCHITECTURE: Design the control framework:
   - Control categories (preventive, detective, corrective)
   - Control types (administrative, technical, physical)
   - Control ownership assignments (role-based, not person-based)
   - Control frequency (continuous, daily, weekly, monthly, quarterly, annual)
   - Evidence collection requirements and retention periods
   - Key Performance Indicators (KPIs) and Key Risk Indicators (KRIs)
   - Automated vs. manual control classification

5. POLICY FRAMEWORK: Design the policy structure:
   - Master policy hierarchy (police → standards → procedures → guidelines)
   - Required policy inventory with version control requirements
   - Policy ownership and review cycle assignments
   - Employee acknowledgment and training requirements
   - Policy exception process and approval authority
   - Policy enforcement mechanisms and consequences

6. ROLES AND RESPONSIBILITIES: Define the governance structure:
   - Compliance Officer/Committee designation and authority
   - Data Protection Officer (DPO) requirements (if applicable)
   - Three lines of defense model (business, compliance, internal audit)
   - Escalation paths and reporting lines
   - Board/senior management reporting requirements
   - External advisor engagement criteria

7. INCIDENT RESPONSE INTEGRATION: Build compliance into incident management:
   - Reportable incident definitions per regulation
   - Regulatory notification timelines and procedures (72-hour GDPR, etc.)
   - Evidence preservation requirements
   - Root cause analysis and corrective action procedures
   - Regulatory communication templates and spokesperson designation
   - Post-incident review and framework update triggers

8. MONITORING AND AUDIT PROGRAM: Design the assurance mechanism:
   - Continuous monitoring tools and automation strategy
   - Internal audit schedule and scope
   - External audit/certification timeline and preparatory steps
   - Management review meeting cadence and agenda
   - Compliance metrics dashboard design
   - Trend analysis and predictive compliance indicators

9. TRAINING AND AWARENESS: Design the human compliance layer:
   - Role-based training curriculum mapping
   - New hire onboarding compliance module
   - Annual refresher training requirements
   - Phishing/social engineering awareness program
   - Training completion tracking and enforcement
   - Competency assessment and knowledge verification

10. IMPLEMENTATION ROADMAP: Create the phased delivery plan:
    - Phase 1: Foundation (0-3 months) — governance, policies, initial assessment
    - Phase 2: Implementation (3-6 months) — controls, training, monitoring
    - Phase 3: Maturation (6-12 months) — audit, certification, continuous improvement
    - Resource requirements (FTE, technology, external advisors)
    - Budget estimation framework
    - Dependencies and critical path identification
    - Go/no-go criteria for each phase gate

INSTRUCTIONS FOR THE AI:
- Map each control to specific regulatory articles/sections
- Include template references where standard templates exist
- Flag jurisdiction-specific variations and multi-jurisdiction conflicts
- Identify quick wins vs. long-term structural changes
- Include cost-benefit considerations for control selection
- Add a "FRAMEWORK VALIDATION CHECKLIST" for leadership review
- Reference relevant guidance documents (NIST, ISO, sector-specific)

DISCLAIMER: This is a framework design instruction, not legal advice. All compliance programs should be validated by qualified legal counsel and compliance professionals in the applicable jurisdiction(s).
```

## Example
### Original Prompt
```text
Help me set up GDPR compliance for my SaaS company.
```

### Enhanced Prompt
```text
I need you to act as a compliance framework architect. Transform the following compliance requirement into a detailed, structured framework design instruction for GDPR compliance for [INSERT COMPANY NAME], a [INSERT INDUSTRY] SaaS company incorporated in [INSERT COUNTRY] with [INSERT NUMBER] employees, processing personal data of EU/EEA data subjects including [INSERT DATA CATEGORIES: names, emails, usage analytics, payment data, etc.].

Design a GDPR compliance framework covering: (1) Data controller vs. processor status determination; (2) Lawful basis mapping for each processing activity (consent, legitimate interest, contract performance, legal obligation); (3) Data Protection Impact Assessment (DPIA) triggers and methodology; (4) Records of Processing Activities (ROPA) template; (5) Data subject rights implementation (access, rectification, erasure, portability, objection); (6) Consent management architecture; (7) Data Protection Officer designation requirements; (8) International data transfer mechanisms (SCCs, adequacy decisions); (9) Data breach notification procedures (72-hour Supervisory Authority notification); (10) Privacy by design integration into SDLC; (11) Vendor/processor due diligence program; (12) Employee training curriculum; (13) Annual compliance review and audit program; (14) Documentation and evidence retention requirements.

Map each control to specific GDPR Articles. Include a phased implementation roadmap. Flag any elements requiring legal counsel validation. DO NOT execute the design — produce the enhanced prompt above.
```

## Notes
- Compliance is not a one-time project — it requires ongoing operational commitment
- Multiple frameworks often overlap (GDPR + CCPA + SOC 2) — design for reuse
- Leadership buy-in is essential — compliance costs must be budgeted
- Technology alone does not create compliance — people and processes matter
- Document everything — if it's not documented, it didn't happen
- Regular reviews are mandatory — regulations evolve constantly
- Consider appointing a dedicated compliance function early

## Tags
`compliance` `regulatory` `framework` `GDPR` `HIPAA` `SOC2` `ISO27001` `audit` `governance` `risk-management` `legal-compliance` `policy`
