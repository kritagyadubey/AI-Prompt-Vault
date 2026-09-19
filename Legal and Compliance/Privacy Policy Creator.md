# Privacy Policy Creator
> Transforms data collection practices into comprehensive, jurisdiction-aware privacy policies with consent mechanisms and user rights disclosures.

## Purpose
This enhancer converts casual privacy policy requests into detailed, multi-jurisdiction privacy policy drafting instructions that cover all required disclosures under GDPR, CCPA, PIPEDA, and other privacy regulations. It forces identification of data processing activities, legal bases, user rights, and enforcement mechanisms that create legally compliant, user-transparent privacy documentation.

## Best For
- SaaS companies and app developers creating privacy policies
- E-commerce sites processing customer data
- Any business collecting personal information from users
- Multi-jurisdiction businesses needing layered privacy disclosures
- Organizations updating existing policies for new regulations

## Prompt Enhancer
```text
I need you to act as a privacy policy architect. Transform the following data collection and processing description into a detailed, structured privacy policy drafting instruction. DO NOT draft the policy yourself — instead, produce a comprehensive prompt that instructs an AI to draft a jurisdiction-compliant privacy policy.

For the given data practices, your enhanced prompt MUST include ALL of the following elements:

1. IDENTITY AND CONTACT INFORMATION:
   - Full legal name of data controller (or processor)
   - Registered address and contact details
   - DPO contact information (if appointed)
   - Supervisory authority contact (for GDPR Art. 13/14)
   - Effective date and version number
   - Last updated timestamp mechanism

2. DATA CATEGORIES AND COLLECTION SOURCES:
   - Personal data types collected (identity, contact, financial, behavioral)
   - Special category data (health, biometric, political, religious) if applicable
   - Sources of collection (direct, third-party, publicly available)
   - Automated collection technologies (cookies, analytics, tracking pixels)
   - Data collected from minors and age verification mechanisms
   - Whether data is mandatory vs. optional for service provision

3. PURPOSES AND LEGAL BASES FOR PROCESSING:
   - Map each data category to a specific processing purpose
   - Assign legal basis per processing activity (consent, contract, legitimate interest, legal obligation, vital interests, public task)
   - For legitimate interest processing, document the balancing test
   - Specify purposes with sufficient granularity (avoid vague language)
   - Identify secondary purposes and compatible use limitations

4. CONSENT MECHANISMS (where applicable):
   - Granular consent options (not bundled/fake consent)
   - Consent collection method (opt-in, not pre-ticked)
   - Consent withdrawal mechanisms (as easy as giving consent)
   - Consent records and audit trail requirements
   - Re-consent triggers and timelines
   - Parental consent for children's data (COPPA compliance)

5. DATA SHARING AND THIRD PARTIES:
   - Categories of recipients (service providers, partners, affiliates)
   - Specific third-party processors with processing purposes
   - Data sharing for legal compliance vs. commercial purposes
   - Joint controller arrangements (if applicable)
   - Third-country transfers and safeguard mechanisms (SCCs, BCRs, adequacy)
   - Sub-processor management and notification obligations

6. DATA RETENTION AND MINIMIZATION:
   - Retention periods per data category and purpose
   - Criteria for determining retention periods
   - Anonymization/pseudonymization procedures post-retention
   - Deletion/disposal methods and verification
   - Archiving exceptions for legal obligations
   - Automated deletion triggers

7. USER RIGHTS AND EXERCISE MECHANISMS:
   - Right of access (Art. 15 GDPR / CCPA Right to Know)
   - Right to rectification (Art. 16 GDPR)
   - Right to erasure/"right to be forgotten" (Art. 17 GDPR / CCPA Delete)
   - Right to restrict processing (Art. 18 GDPR)
   - Right to data portability (Art. 20 GDPR)
   - Right to object (Art. 21 GDPR / CCPA Opt-Out)
   - Right not to be subject to automated decision-making (Art. 22 GDPR)
   - CCPA-specific rights (opt-out of sale/sharing, non-discrimination)
   - Response timelines (30 days GDPR, 45 days CCPA)
   - Identity verification procedures for rights requests
   - Appeal mechanisms for denied requests

8. INTERNATIONAL DATA TRANSFERS:
   - Identification of all transfer mechanisms
   - adequacy decisions relied upon
   - Standard Contractual Clauses (SCCs) implementation details
   - Transfer Impact Assessment (TIA) results
   - Supplementary measures implemented
   - Data localization requirements (if applicable)

9. SECURITY MEASURES:
   - Technical measures (encryption, access controls, pseudonymization)
   - Organizational measures (training, policies, incident response)
   - Certification mechanisms and codes of conduct
   - Regular testing and evaluation procedures
   - Breach notification obligations and procedures

10. COOKIES AND TRACKING TECHNOLOGIES:
    - Cookie categories (strictly necessary, performance, functional, targeting)
    - Cookie purposes and duration per cookie
    - Consent management platform (CMP) integration
    - Do Not Track (DNT) and Global Privacy Control (GPC) signals
    - Third-party analytics and advertising tracking
    - Browser opt-out mechanisms

11. CHILDREN'S PRIVACY:
    - Age verification mechanisms
    - Parental consent requirements (COPPA: under 13; GDPR: varies by member state)
    - Data collected from children and processing limitations
    - Parental access and deletion rights

12. POLICY CHANGES AND NOTIFICATION:
    - Material change notification mechanisms
    - Consent requirements for material changes
    - Version history and changelog maintenance
    - Archive of previous versions

INSTRUCTIONS FOR THE AI:
- Use plain, clear language (avoid legalese where possible)
- Include layered notices (short-form + detailed policy)
- Add a "Data Processing Summary" table for quick reference
- Flag jurisdiction-specific requirements with [JURISDICTION NOTE]
- Include sample consent language where appropriate
- Reference specific regulatory articles for each disclosure
- Add a "USER RIGHTS QUICK REFERENCE" section
- Include contact information template with placeholder fields

DISCLAIMER: This is a policy drafting instruction, not legal advice. Privacy policies must be reviewed by qualified legal counsel in all applicable jurisdictions before publication. Privacy law is complex and varies significantly by jurisdiction.
```

## Example
### Original Prompt
```text
Write a privacy policy for my app that collects user data.
```

### Enhanced Prompt
```text
I need you to act as a privacy policy architect. Transform the following into a detailed privacy policy drafting instruction for [INSERT APP NAME], a [INSERT APP TYPE] mobile application available on iOS and Android, developed by [INSERT COMPANY NAME], incorporated in [INSERT COUNTRY].

The app collects the following data: (1) Account creation data: email, username, password (hashed), date of birth; (2) Profile data: display name, profile photo, bio; (3) Usage data: app interactions, session duration, feature usage, crash logs; (4) Device data: device model, OS version, IP address, device identifiers; (5) Location data: coarse location (city-level) with explicit consent; (6) Payment data: processed through [INSERT PAYMENT PROCESSOR] — we do not store card details; (7) Third-party data: [INSERT THIRD PARTIES e.g., Google Analytics, Firebase, Stripe].

Design a privacy policy covering GDPR (EU users), CCPA (California residents), and PIPEDA (Canadian users) simultaneously. Include layered notices, a Data Processing Summary table, granular consent mechanisms, cookie disclosure, user rights exercise procedures, international transfer mechanisms, children's privacy (COPPA), and a comprehensive user rights quick reference. Map each disclosure to specific regulatory articles. Flag jurisdiction-specific variations. DO NOT draft the policy — produce the enhanced prompt above.
```

## Notes
- Privacy policies are legally binding documents — accuracy is critical
- GDPR requires plain language — legalese may not be enforceable
- CCPA/CPRA requires specific opt-out mechanisms (Global Privacy Control)
- "Free" consent is required — bundled consent is not valid under GDPR
- Privacy policies must be easily accessible (not buried in footers)
- Regular updates are required as processing activities change
- Data Protection Impact Assessments may be required for high-risk processing
- Supervisory authorities actively enforce privacy compliance
- Consider privacy-by-design principles in all product development

## Tags
`privacy` `GDPR` `CCPA` `data-protection` `consent` `user-rights` `privacy-policy` `compliance` `data-governance` `legal-compliance` `cookies` `international-transfers`
