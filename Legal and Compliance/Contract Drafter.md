# Contract Drafter
> Transforms vague contract requests into structured, clause-by-clause drafting instructions with risk flags and negotiation considerations.

## Purpose
This enhancer converts casual contract requests into professional, comprehensive drafting instructions that cover all essential contractual elements. It forces specificity on terms, obligations, remedies, and edge cases that non-lawyers often overlook, producing prompts that yield legally sound draft contracts ready for attorney review.

## Best For
- Freelancers drafting client agreements
- Startups creating vendor or employment contracts
- Anyone needing NDAs, MSAs, SOWs, or service agreements
- Contract negotiations requiring clause-level detail
- Converting handshake deals into formal written agreements

## Prompt Enhancer
```text
I need you to act as a legal drafting assistant. Transform the following contract request into a detailed, structured drafting instruction. DO NOT execute the drafting yourself — instead, produce a comprehensive prompt that instructs an AI to draft a professional contract.

For the given contract type, your enhanced prompt MUST include ALL of the following elements:

1. CONTRACT IDENTIFICATION: Specify full legal names, entity types, jurisdiction of incorporation, and principal addresses for all parties. Identify the contract type (bilateral/unilateral), effective date mechanics, and whether it is governed by UCC, common law, or a specific statutory regime.

2. RECITALS AND PURPOSE: Draft a "WHEREAS" section establishing the business context, the relationship between parties, and the commercial intent behind the agreement. This grounds the contract in real-world purpose.

3. DEFINITIONS: List every term that requires precise definition, including capitalized terms, technical jargon, deliverables, milestones, intellectual property, confidential information, and any domain-specific vocabulary. Specify that definitions must be internally consistent throughout the document.

4. SCOPE OF WORK / OBLIGATIONS: For each party, detail:
   - Specific deliverables with measurable acceptance criteria
   - Performance standards and service levels (SLAs)
   - Timeframes, deadlines, and milestone schedules
   - Dependencies and prerequisites between parties
   - Right to subcontract and conditions for delegation

5. CONSIDERATION AND PAYMENT: Specify:
   - Payment structure (fixed, milestone, hourly, usage-based)
   - Invoicing procedures and payment terms (Net 30/60/90)
   - Late payment penalties and interest calculations
   - Expense reimbursement policies
   - Currency and tax withholding obligations
   - Right to audit financial records

6. INTELLECTUAL PROPERTY: Define:
   - Ownership of pre-existing IP vs. newly created IP
   - Work-for-hire vs. license-back provisions
   - Background IP licensing scope and restrictions
   - Derivative works ownership and allocation
   - IP indemnification obligations

7. CONFIDENTIALITY: Include:
   - Definition of confidential information (broad vs. narrow)
   - Permitted disclosures and carve-outs
   - Duration of confidentiality obligations (survival period)
   - Return/destruction of materials upon termination
   - Remedies for breach (injunctive relief clause)

8. REPRESENTATIONS AND WARRANTIES: For each party, specify warranties regarding:
   - Authority and capacity to enter the agreement
   - No conflicts with existing obligations
   - Compliance with applicable laws
   - Accuracy of provided information
   - Quality and fitness for purpose of deliverables

9. INDEMNIFICATION: Detail:
   - Scope of indemnifiable losses (direct, indirect, consequential)
   - Third-party claim procedures
   - Defense and control of litigation
   - Caps on liability and exclusions
   - Insurance requirements and minimum coverage

10. TERM AND TERMINATION:
    - Initial term and renewal mechanics (auto-renew vs. opt-in)
    - Termination for convenience with notice period
    - Termination for cause and cure periods
    - Effects of termination on ongoing obligations
    - Surviving provisions list

11. DISPUTE RESOLUTION:
    - Negotiation/escalation ladder with timeframes
    - Mediation requirements before arbitration/litigation
    - Arbitration rules (AAA, JAMS, ICC) or court jurisdiction
    - Venue and governing law selection
    - Attorneys' fees and costs allocation

12. GENERAL PROVISIONS: Include standard boilerplate:
    - Entire agreement / integration clause
    - Amendment mechanics (written, signed)
    - Severability with reformation authority
    - Waiver (no oral waivers, no continuing waiver)
    - Assignment restrictions
    - Force majeure with enumerated events
    - Notices (method, addresses, deemed receipt)
    - Counterparts and electronic signatures

INSTRUCTIONS FOR THE AI:
- Flag any missing elements as "[INSERT REQUIRED]"
- Use square brackets for all variables requiring customization
- Include drafting notes in italics explaining rationale for key choices
- Note jurisdiction-specific variations where applicable
- Flag any clauses that may be unenforceable in certain jurisdictions
- Include a "DRAFTING CHECKLIST" at the end for attorney review

DISCLAIMER: This is a drafting instruction, not legal advice. All contracts should be reviewed by a licensed attorney in the applicable jurisdiction before execution.
```

## Example
### Original Prompt
```text
Help me write a contract for a web developer building my website.
```

### Enhanced Prompt
```text
I need you to act as a legal drafting assistant. Transform the following contract request into a detailed, structured drafting instruction for a WEB DEVELOPMENT SERVICES AGREEMENT between a Client [INSERT CLIENT LEGAL NAME, ENTITY TYPE, STATE OF INCORPORATION, PRINCIPAL ADDRESS] and a Developer [INSERT DEVELOPER LEGAL NAME/DBA, ENTITY TYPE, STATE OF INCORPORATION, PRINCIPAL ADDRESS].

The contract must cover: (1) Scope of work — specific website deliverables including design mockups, front-end development, back-end integration, CMS setup, responsive design, and launch; (2) IP ownership — Client owns all final deliverables as work-for-hire, Developer retains rights to pre-existing tools and frameworks; (3) Payment — milestone-based payments tied to deliverable approval, Net 15 terms, 1.5% monthly late fee; (4) Timeline — estimated completion within [X] weeks, with defined milestones; (5) Confidentiality — mutual NDA covering business plans, source code, and user data, surviving 2 years post-termination; (6) Warranties — Developer warrants work conforms to specifications and is free from material defects for 90 days post-launch; (7) Termination — Client may terminate for convenience with 14 days notice, paying for completed work; (8) Governing law — State of [INSERT STATE].

Include all standard boilerplate provisions. Flag any missing elements as [INSERT REQUIRED]. Use square brackets for all customization variables. Include drafting notes in italics. Add a DRAFTING CHECKLIST for attorney review. DO NOT execute the drafting — produce the enhanced prompt above.
```

## Notes
- Always recommend attorney review before execution
- Jurisdiction matters — enforceability varies by state/country
- Consider whether UCC Article 2 applies (goods vs. services)
- Insurance requirements often overlooked in service agreements
- IP ownership should be explicit — default "work for hire" rules vary
- Force majeure clauses gained importance post-pandemic

## Tags
`contracts` `legal-drafting` `agreements` `NDA` `MSA` `SOW` `business-law` `commercial-law` `legal-compliance` `risk-management`
