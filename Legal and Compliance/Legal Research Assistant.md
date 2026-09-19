# Legal Research Assistant
> Transforms legal questions into structured research methodologies with source hierarchies, citation frameworks, and analytical frameworks.

## Purpose
This enhancer converts casual legal research requests into systematic, multi-source research instructions that follow proper legal research methodology. It forces identification of jurisdiction, applicable authority hierarchy, search strategy, and analytical framework, producing prompts that yield thorough, well-cited legal analysis rather than surface-level generalizations.

## Best For
- Attorneys conducting preliminary research on unfamiliar areas of law
- Law students researching case briefs and memoranda
- Business professionals understanding legal obligations
- Compliance officers researching regulatory requirements
- Anyone needing authoritative legal information (not legal advice)

## Prompt Enhancer
```text
I need you to act as a legal research methodologist. Transform the following legal research question into a detailed, structured research instruction. DO NOT conduct the research yourself — instead, produce a comprehensive prompt that instructs an AI to perform systematic legal research.

For the given legal question, your enhanced prompt MUST include ALL of the following elements:

1. RESEARCH SCOPING AND JURISDICTION:
   - Precise legal question framed as an issue (not a conclusion)
   - Jurisdiction(s) of interest (federal, state, international)
   - Temporal scope (current law, historical development, pending legislation)
   - Subject matter jurisdiction (civil, criminal, administrative, regulatory)
   - Conflicts of law considerations (choice of law, venue, preemption)

2. AUTHORITY HIERARCHY MAPPING:
   - Primary authorities to search:
     * Constitutional provisions (federal and state)
     * Statutes (codes, session laws, compiled laws)
     * Administrative regulations (CFR, state registers)
     * Case law (trial, appellate, supreme court)
     * Treaty/international law (if applicable)
   - Secondary authorities to consult:
     * Legal treatises and hornbooks
     * Law review articles and journals
     * Restatements of the Law
     * ABA publications and practice guides
     * Jurisprudence constant (civil law jurisdictions)
   - Persuasive vs. binding authority distinction by jurisdiction
   - unpublished opinion considerations and citation rules

3. SEARCH STRATEGY DESIGN:
   - Keyword search terms (Boolean operators, natural language)
   - Key statutory provisions and section numbers
   - Known leading cases and their citations
   - Shepard's/KeyCite treatment requirements (good law verification)
   - Secondary source starting points
   - Practice area-specific databases and resources
   - Legislative history sources (committee reports, floor debates)
   - Regulatory guidance (advisory opinions, FAQ documents, guidance letters)

4. ANALYTICAL FRAMEWORK:
   - Issue-spotting methodology (IRAC/CRAC/CREAC)
   - Rule synthesis approach (majority rule, minority rule, trend analysis)
   - Application methodology (fact-intensive analysis)
   - Policy considerations and legislative intent
   - Comparative law analysis (if multi-jurisdictional)
   - Historical development and evolution of the law
   - Scholarly criticism and academic debate

5. SOURCE EVALUATION CRITERIA:
   - Authority hierarchy (primary vs. secondary, mandatory vs. persuasive)
   - Precedential value (binding, persuasive, distinguished, overruled)
   - Publication status and official reporter citations
   - Shepardizing/KeyCiting requirements
   - Recency and continuing validity checks
   - Judicial treatment and subsequent history
   - Scholarly critique and academic consensus

6. CITATION AND DOCUMENTATION:
   - Bluebook/ALWD citation format requirements
   - Pinpoint citations to specific pages/paragraphs
   - Quotation vs. paraphrase guidelines (accuracy obligations)
   - Signal usage (see, cf., but see, contra, accord)
   - Parenthetical descriptions
   - Short form vs. full citation requirements
   - Electronic source citations (WLex, Westlaw, LexisNexis)

7. RESEARCH DELIVERABLES:
   - Issue presentation statement
   - Brief answer (conclusionary statement)
   - Heading structure for memorandum
   - Rule synthesis with supporting citations
   - Application section with factual analysis
   - Conclusion with confidence level assessment
   - Appendix of key statutes and cases

8. LIMITATIONS AND CAVEATS:
   - Identification of open questions requiring further research
   - Jurisdiction-specific variations requiring local counsel
   - Pending legislation or litigation that may change the law
   - Areas of uncertainty or conflicting authority
   - Recommendations for additional research steps
   - Disclaimers about the nature of AI-generated legal information

INSTRUCTIONS FOR THE AI:
- Frame the research as a series of searchable queries
- Include specific database search strings (Westlaw, LexisNexis syntax)
- Specify minimum number of sources per category
- Require verification of all citations for continuing validity
- Flag areas where professional legal judgment is essential
- Include a "RESEARCH ROADMAP" with prioritized search steps
- Add a "CONFIDENCE ASSESSMENT" framework for findings
- Note that AI-generated legal research must be verified by a licensed attorney

DISCLAIMER: This is a legal research instruction, not legal advice. AI-generated legal research must be verified against current, authoritative sources by a licensed attorney in the applicable jurisdiction. Laws change frequently, and AI may not reflect the most recent developments.
```

## Example
### Original Prompt
```text
Research whether my non-compete agreement is enforceable.
```

### Enhanced Prompt
```text
I need you to act as a legal research methodologist. Transform the following into a detailed legal research instruction for analyzing the enforceability of non-compete agreements in [INSERT STATE/JURISDICTION].

The research question is: "Under what conditions is a non-compete agreement enforceable in [INSERT STATE], and what are the current trends in judicial treatment of non-compete restrictions?"

Design a research framework covering: (1) Applicable state statute and common law standards; (2) Reasonableness analysis factors (duration, geographic scope, scope of restricted activity); (3) Legitimate business interest requirements (trade secrets, customer relationships, specialized training); (4) Consideration requirements (new employment vs. continued employment); (5) Recent legislative developments (state-specific bans or restrictions); (6) Judicial trends (narrow construction, blue-pencil doctrine, reformation); (7) Comparison with neighboring jurisdictions; (8) Practical enforceability considerations. Search Westlaw and LexisNexis using specific Boolean queries. Shepardize all cited cases. Include a research roadmap with prioritized search steps. DO NOT conduct the research — produce the enhanced prompt above.
```

## Notes
- Legal research is jurisdiction-specific — always verify the applicable jurisdiction
- AI-generated legal information may not reflect recent case law or statutory changes
- Always verify citations using Shepard's or KeyCite before relying on them
- Primary authority (statutes, cases) takes precedence over secondary sources
- Unpublished opinions may have limited precedential value
- Legislative history can clarify ambiguous statutory language
- Consider both majority and minority rules when analyzing unsettled areas
- Professional legal judgment is essential — AI provides information, not judgment

## Tags
`legal-research` `case-law` `statutes` `citation` `legal-analysis` `IRAC` `jurisdiction` `legal-compliance` `research-methodology` `authority-hierarchy` `legal-writing`
