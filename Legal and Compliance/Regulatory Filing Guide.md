# Regulatory Filing Guide
> Transforms regulatory submission needs into structured filing instructions with document checklists, timeline management, and compliance verification protocols.

## Purpose
This enhancer converts casual regulatory filing requests into comprehensive submission preparation instructions that cover document assembly, compliance verification, filing procedures, and post-filing obligations. It forces identification of applicable regulations, required documentation, filing deadlines, and response strategies that create actionable submission roadmaps rather than abstract compliance concepts.

## Best For
- Companies preparing FDA submissions (510(k), PMA, De Novo)
- Financial institutions filing regulatory reports (SEC, FINRA, OCC)
- Healthcare organizations submitting to CMS or state agencies
- Environmental companies filing EPA or state environmental permits
- Any organization navigating complex regulatory filing requirements

## Prompt Enhancer
```text
I need you to act as a regulatory filing strategist. Transform the following regulatory submission need into a detailed, structured filing instruction. DO NOT execute the filing yourself — instead, produce a comprehensive prompt that instructs an AI to design a comprehensive regulatory filing preparation plan.

For the given regulatory submission, your enhanced prompt MUST include ALL of the following elements:

1. REGULATORY PATHWAY IDENTIFICATION:
   - Primary regulatory authority and specific division/office
   - Applicable statute and implementing regulations
   - Submission type and classification (premarket, post-market, periodic)
   - Reference product/predicate device analysis (if applicable)
   - Regulatory pathway selection rationale:
     * 510(k) substantial equivalence vs. De Novo vs. PMA (FDA)
     * NDA/ANDA/BLA requirements (FDA drug submissions)
     * CE marking/MDR classification (EU medical devices)
     * SEC registration/exemption (securities filings)
     * EPA permit type (environmental)
   - Pre-submission meeting strategy and timing

2. DOCUMENT ASSEMBLY CHECKLIST:
   - Core submission documents with specific requirements:
     * Cover letter and transmittal forms
     * Executive summary and submission overview
     * Technical dossier/document requirements
     * Non-clinical/laboratory study reports
     * Clinical study reports and data
     * Manufacturing and quality system documentation
     * Labeling and instructions for use
   - Supporting documentation:
     * References and bibliography
     *电子 submissions formatting (eSTAR, eCTD structure)
     * Certification and declaration requirements
     * Financial disclosure and conflict of interest forms
   - Document specifications:
     * Formatting requirements (margins, fonts, pagination)
     * Section numbering and heading conventions
     * Cross-reference and hyperlink requirements
     * Signature and execution requirements

3. TECHNICAL DOCUMENTATION REQUIREMENTS:
   - Design documentation:
     * Design history file (DHF) components
     * Design input/output traceability
     * Risk management file (ISO 14971 compliance)
     * Software documentation (IEC 62304 compliance, if applicable)
   - Testing and validation:
     * Biocompatibility testing (ISO 10993 series)
     * Electrical safety testing (IEC 60601 series, if applicable)
     * Electromagnetic compatibility (EMC) testing
     * Software validation and verification
     * Performance testing against specifications
     * Shelf life and stability studies
   - Manufacturing documentation:
     * Device master record (DMR) components
     * Manufacturing process validation
     * Quality system documentation (21 CFR 820 / ISO 13485)
     * Supplier qualification records
     * Lot/batch traceability systems

4. CLINICAL EVIDENCE REQUIREMENTS (if applicable):
   - Clinical study design considerations:
     * Study protocol development
     * Informed consent and IRB/Ethics committee requirements
     * Investigational device exemption (IDE) requirements
     * Study endpoint selection and statistical analysis plan
   - Clinical data requirements:
     * Pivotal clinical trial design and execution
     * Literature review methodology (MEDLINE, PubMed search strategy)
     * Real-world evidence (RWE) considerations
     * Post-market clinical follow-up (PMCF) plans
   - Clinical evaluation report (CER) components
   - Benefit-risk analysis framework

5. QUALITY SYSTEM DOCUMENTATION:
   - Quality management system (QMS) requirements:
     * Quality policy and objectives
     * Organizational structure and responsibilities
     * Document control procedures
     * CAPA (Corrective and Preventive Action) system
     * Management review documentation
   - Supplier management:
     * Approved supplier list
     * Supplier audit records
     * Incoming inspection procedures
     * Supply chain risk management
   - Complaint handling and MDR reporting:
     * Complaint investigation procedures
     * Medical device reporting (MDR) criteria
     * Vigilance reporting requirements (EU)
     * Trend analysis and signal detection

6. FILING PROCEDURE AND TIMELINE:
   - Pre-filing preparation:
     * Internal review and quality checks
     * Regulatory affairs review and approval
     * Executive sign-off procedures
     * Submission package assembly and verification
   - Filing mechanics:
     * Electronic submission system navigation (FDA ESG, SEC EDGAR)
     * Submission gateway and account requirements
     * Fee payment procedures and amounts
     * Confirmation and receipt tracking
   - Timeline management:
     * Gantt chart with critical path identification
     * Milestone definitions and dependencies
     * Buffer time for unexpected delays
     * Parallel processing opportunities
   - Pre-submission meeting strategy:
     * Request for Pre-Submission (Q-Sub) content
     * Pre-IDE meeting preparation
     * Pre-IND meeting strategy
     * Type B/C meeting request requirements

7. POST-FILING OBLIGATIONS:
   - Review period management:
     * Acknowledgment and acceptance tracking
     * Information request (IR) preparation and response
     * Deficiency letter response strategy
     * Advisory committee meeting preparation
   - Approval/clearance conditions:
     * Post-market surveillance requirements
     * Phase IV study commitments
     * REMS (Risk Evaluation and Mitigation Strategy) requirements
     * Conditional approval conditions
   - Ongoing compliance obligations:
     * Annual reporting requirements
     * Periodic safety update reports (PSUR)
     * Supplemental submissions for changes
     * Product listing and establishment registration

8. RISK MITIGATION AND CONTINGENCY:
   - Common filing pitfalls and avoidance strategies:
     * Incomplete documentation
     * Formatting errors and technical rejection
     * Missing signatures and certifications
     * Inadequate testing or clinical evidence
   - Response strategies for regulatory actions:
     * Complete Response Letter (CRL) response
     * Warning letter remediation
     * Consent decree compliance
     * Recall classification and reporting
   - Appeal and dispute resolution procedures:
     * Administrative appeal processes
     * Regulatory hearing requests
     * Judicial review options
     * Dispute resolution with regulatory agencies

9. BUDGET AND RESOURCE PLANNING:
   - Cost estimation framework:
     * Regulatory consulting fees
     * Testing and laboratory costs
     * Clinical study costs
     * Filing fees and government costs
     * Quality system implementation costs
   - Resource requirements:
     * Internal team roles and responsibilities
     * External consultant and advisor needs
     * Laboratory and testing facility requirements
     * Clinical site requirements
   - Timeline-cost trade-off analysis

10. INTERNATIONAL FILING CONSIDERATIONS:
    - Mutual recognition and harmonization:
      * MDSAP (Medical Device Single Audit Program)
      * CE marking/MDR requirements (EU)
      * Health Canada requirements
      * PMDA requirements (Japan)
      * NMPA requirements (China)
    - Country-specific requirements and pitfalls
    - Local authorized representative requirements
    - Labeling translation and localization requirements
    - Post-market surveillance requirements by jurisdiction

INSTRUCTIONS FOR THE AI:
- Map each document requirement to specific regulatory citations
- Include template references where standard templates exist
- Provide timeline visualizations with critical path identification
- Flag common rejection reasons and prevention strategies
- Include cost estimation frameworks with ranges
- Add a "FILING READINESS CHECKLIST" for leadership review
- Note that all regulatory filings must be reviewed by qualified regulatory professionals
- Include contact information for relevant regulatory agencies

DISCLAIMER: This is a regulatory filing instruction, not legal or regulatory advice. All regulatory submissions must be prepared and reviewed by qualified regulatory affairs professionals and legal counsel in the applicable jurisdiction. Regulatory requirements change frequently and vary by product type, classification, and market.
```

## Example
### Original Prompt
```text
Help me prepare an FDA 510(k) submission for my medical device.
```

### Enhanced Prompt
```text
I need you to act as a regulatory filing strategist. Transform the following into a detailed 510(k) submission preparation instruction for [INSERT DEVICE NAME], a [INSERT DEVICE CLASS] medical device in [INSERT MEDICAL SPECIALTY] intended for [INSERT INTENDED USE STATEMENT].

The device: [INSERT DEVICE DESCRIPTION, INCLUDING KEY FEATURES, TECHNOLOGY, AND MECHANISM OF ACTION].

Design a 510(k) submission preparation plan covering: (1) Predicate device identification and substantial equivalence comparison strategy; (2) Special controls analysis (if Class II); (3) Biocompatibility testing requirements per ISO 10993; (4) Electrical safety and EMC testing (if applicable); (5) Software documentation per IEC 62304 (if applicable); (6) Performance testing against identified special controls; (7) Clinical evidence requirements and literature review strategy; (8) Labeling review and compliance; (9) eSTAR formatting requirements; (10) Quality system documentation requirements (21 CFR 820); (11) Filing fee schedule and payment; (12) Timeline with critical milestones; (13) Pre-submission meeting strategy. Map all requirements to specific FDA guidance documents. Include a filing readiness checklist. DO NOT execute the filing — produce the enhanced prompt above.
```

## Notes
- Regulatory filings are complex — professional regulatory affairs support is essential
- Filing timelines can vary significantly based on regulatory backlog and complexity
- Pre-submission meetings with regulatory agencies can clarify requirements early
- Document formatting and technical requirements are strictly enforced
- Missing or incomplete documentation is a common cause of delays
- Post-filing obligations begin immediately upon approval/clearance
- International filings often require local representation and translation
- Regulatory requirements change frequently — always verify current guidance
- Budget adequately for testing, clinical studies, and regulatory consulting

## Tags
`regulatory-filing` `FDA` `510k` `PMA` `CE-marking` `medical-devices` `compliance` `submission` `regulatory-affairs` `quality-system` `clinical-evidence` `legal-compliance`
