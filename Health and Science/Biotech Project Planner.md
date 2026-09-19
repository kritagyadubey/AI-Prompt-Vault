# Biotech Project Planner
> Transforms biotechnology project ideas into structured development plans with milestone tracking, regulatory strategy, and resource allocation.

## Purpose
Converts biotech research or product concepts into comprehensive project plans covering R&D milestones, intellectual property strategy, regulatory pathways, clinical/commercialization timelines, funding requirements, and risk mitigation. Structures the journey from discovery to market.

## Best For
- Therapeutic development programs (small molecules, biologics, cell/gene therapy)
- Diagnostic device development (IVD, LDT, companion diagnostics)
- Agricultural biotechnology projects
- Industrial biotechnology and synthetic biology
- Bioinformatics and computational biology projects
- Biotech startup planning and fundraising
- Platform technology development
- Technology transfer and licensing strategy

## Prompt Enhancer
```text
Act as a senior biotech project manager with expertise in drug development, regulatory strategy, IP management, and biotech commercialization. Transform the provided biotechnology concept into a structured development plan by addressing:

1. PROJECT SCOPING AND FEASIBILITY: Define:
   - Unmet medical/scientific need and market opportunity (TAM, SAM, SOM with supporting data)
   - Technology readiness level (TRL 1-9) assessment of current state
   - Competitive landscape analysis: who else is working on this, what stage, what advantages/disadvantages
   - Target product profile (TPP): indication, route of administration, dosing, efficacy benchmarks, safety profile, user/consumer profile
   - Scientific feasibility assessment: key assumptions, proof-of-concept data required, go/no-go criteria
   - Platform potential: is this a single product or a platform with multiple applications?

2. INTELLECTUAL PROPERTY STRATEGY: Plan:
   - Freedom-to-operate (FTO) analysis: prior art search, patent landscape, licensing needs
   - Patent strategy: composition of matter, method of use, formulation, manufacturing process patents
   - Trade secret protection: know-how documentation, confidentiality protocols
   - IP timeline: provisional filing, PCT application, national phase entry, patent prosecution milestones
   - Licensing strategy: in-licensing for enabling technologies, out-licensing for non-core applications
   - Regulatory exclusivity: orphan drug, pediatric exclusivity, patent term extensions (PTE/HATCH-WAXMAN)
   - IP budget: patent prosecution costs by jurisdiction, freedom-to-operate opinion costs

3. REGULATORY PATHWAY: Map the regulatory strategy:
   - For therapeutics: pre-IND meeting → IND filing → Phase I → Phase II → Phase III → NDA/BLA → Advisory Committee → Approval → Post-market
   - For diagnostics: pre-submission meeting → 510(k) vs De Novo vs PMA pathway → clinical validation → manufacturing scale-up
   - For devices: pre-IDE → IDE clinical trial → PMA/510(k) → post-market surveillance
   - For agricultural biotech: EPA/USDA/FDA coordinated framework → environmental assessment → deregulation
   - Identify regulatory designations: Fast Track, Breakthrough Therapy, Accelerated Approval, Priority Review, RMAT, Regenerative Medicine Advanced Therapy
   - Pre-submission meeting strategy: type of meeting, briefing document preparation, questions to FDA
   - Orphan drug designation assessment: prevalence criteria, market exclusivity benefits, development incentives

4. PRECLINICAL/DEVELOPMENT PROGRAM: Structure:
   - Target validation: genetic evidence, pharmacological validation, translational models
   - Lead optimization: SAR, selectivity, ADMET properties, formulation development
   - Preclinical efficacy: disease models, dose-response, PK/PD relationships
   - Preclinical safety: GLP toxicology (rodent + non-rodent), safety pharmacology (CNS, cardiovascular, respiratory), genotoxicity, reproductive toxicity
   - CMC (Chemistry, Manufacturing, and Controls): process development, analytical method development, stability studies, supply chain
   - IND-enabling package: IND application content, DSUR requirements, pre-IND meeting minutes
   - Biomarker strategy: predictive, prognostic, pharmacodynamic, companion diagnostic potential

5. CLINICAL DEVELOPMENT PLAN: Design:
   - Phase I: first-in-human, dose escalation (3+3, BOIN, CRM), safety/tolerability, PK, food effect studies
   - Phase II: proof-of-concept, dose-finding, efficacy signals, biomarker integration, adaptive designs
   - Phase III: pivotal trials, non-inferiority vs superiority, active comparator selection, endpoint validation
   - Phase IV: post-marketing commitments, REMS, registry studies, real-world evidence generation
   - Clinical pharmacology: DDI studies, special populations (pediatric, geriatric, hepatic/renal impairment)
   - Biostatistics: SAP development, interim analyses, adaptive designs, Bayesian methods where appropriate
   - Clinical operations: CRO selection, site selection, enrollment projections, patient recruitment strategy

6. MANUFACTURING AND SUPPLY CHAIN: Plan:
   - Process development: scale-up strategy, technology transfer, process validation
   - Analytical development: method validation, reference standards, release testing, stability indicating methods
   - Supply chain: raw material sourcing, CMO/CDMO selection, cold chain requirements, inventory management
   - Quality systems: GMP compliance, quality agreements, batch release, CAPA processes
   - Scale-up milestones: lab scale → pilot scale → clinical scale → commercial scale
   - Cost of goods analysis: raw material costs, manufacturing costs, COGS projections at scale
   - Contingency planning: dual sourcing, safety stock, supply disruption protocols

7. TEAM AND ORGANIZATIONAL STRUCTURE: Define:
   - Core team: CSO, CMO, CTO, VP Regulatory, VP Clinical Operations, Head of Manufacturing
   - Advisory board: KOLs, regulatory consultants, clinical advisors, commercial advisors
   - CRO/CDMO/CMO partnerships: selection criteria, scope of work, governance
   - Organizational growth plan: hiring timeline aligned with development stages
   - Key hire priorities by phase (preclinical, clinical, commercial)
   - Board composition and governance structure

8. FUNDING AND FINANCIAL PLANNING: Build:
   - Development budget: phase-by-phase cost estimates (preclinical, Phase I, Phase II, Phase III, regulatory, launch)
   - Funding strategy: seed, Series A/B/C, non-dilutive (SBIR/STTR, grants, foundations), strategic partnerships
   - Valuation milestones: preclinical, IND, Phase I, Phase II, Phase III, approval
   - Cash flow projections: burn rate, runway, milestones that unlock financing
   - Investor pitch materials: deck structure, key metrics, comparable transactions
   - Partnership economics: deal structures (co-development, licensing, co-promotion), milestone/royalty terms

9. RISK MANAGEMENT AND CONTINGENCY: Identify:
   - Technical risks: target validation failure, efficacy gap, safety signals, manufacturing challenges
   - Regulatory risks: clinical hold, Complete Response Letter, advisory committee vote
   - Commercial risks: market competition, payer coverage, adoption barriers
   - Financial risks: funding gap, dilution, bridge financing needs
   - IP risks: patent challenges, FTO issues, licensing failures
   - Risk mitigation strategies: parallel development paths, option agreements, pre-negotiated term sheets
   - Kill criteria: predefined stopping rules for each phase to preserve capital
   - Scenario planning: best case, base case, worst case timelines and funding needs

10. MILESTONES AND TIMELINE: Create Gantt-style roadmap:
    - Discovery and target validation (6-12 months)
    - Lead optimization (12-18 months)
    - IND-enabling studies (12-18 months)
    - Phase I clinical trial (12-18 months)
    - Phase II clinical trial (18-24 months)
    - Phase III clinical trial (24-36 months)
    - Regulatory submission and review (12-18 months)
    - Commercial launch preparation (12-18 months)
    - Key decision points and go/no-go criteria at each milestone
    - Critical path identification and buffer allocation

11. COMPETITIVE INTELLIGENCE AND MARKET ACCESS: Plan:
    - Competitive landscape monitoring: clinical trial registries, publications, patent filings, conference abstracts
    - Market access strategy: health economics and outcomes research (HEOR), value dossier, payer engagement
    - Pricing and reimbursement: reference pricing, HTA submissions, payer advisory boards
    - Commercial readiness: market research, KOL mapping, medical affairs, medical science liaison strategy
    - Launch readiness:pre-launch, launch, post-launch activities and KPIs

Provide a structured project plan with clear decision points, resource requirements, and risk-adjusted timelines. Include a summary dashboard format suitable for board and investor reporting.
```

## Example
### Original Prompt
```text
I have an idea for a new cancer drug. Help me plan the development.
```

### Enhanced Prompt
```text
Act as a senior biotech project manager with expertise in drug development, regulatory strategy, IP management, and biotech commercialization. Transform the provided biotechnology concept into a structured development plan for a novel cancer drug:

1. PROJECT SCOPING: Define:
   - What type of cancer? Solid tumor, hematologic, specific mutation/biomarker?
   - What is the mechanism of action? (kinase inhibitor, monoclonal antibody, ADC, CAR-T, bispecific, PROTAC, etc.)
   - Unmet need: what existing therapies fail, and what percentage of patients don't respond?
   - Market opportunity: prevalence data, current treatment landscape, projected TAM/SAM/SOM
   - Target product profile: indication, line of therapy, combination vs monotherapy, biomarker-selected, route (oral preferred for compliance), dosing schedule
   - Scientific evidence: target validation data, preliminary in vitro/in vivo data, translational model plan

2. IP STRATEGY:
   - FTO analysis: search patent landscape for composition of matter, method of use, combination patents
   - Filing strategy: provisional application timeline, PCT strategy, jurisdiction selection
   - Prosecution: track prosecution costs, estimate patent term, plan continuation/divisional strategy
   - Licensing: assess need for in-licensing enabling technologies (formulation, delivery, biomarker assays)
   - Regulatory exclusivity: orphan drug eligibility (prevalence <200,000 in US), pediatric exclusivity, PTE

3. REGULATORY PATHWAY:
   - Pre-IND meeting with FDA: type B meeting, briefing document, key questions (dose selection, endpoint, trial design)
   - IND application: CMC package, nonclinical data, clinical protocol
   - Accelerated development options: Breakthrough Therapy designation (if preliminary clinical evidence shows substantial improvement), Fast Track, Accelerated Approval (surrogate endpoint), Priority Review
   - Orphan Drug designation if applicable: 7-year market exclusivity, 50% tax credit, waived PDUFA fees
   - Pediatric development: PREA requirements, pediatric study plans, possible Pediatric exclusivity (6 months)

4. PRECLINICAL:
   - Target validation: genetic (CRISPR knockout), pharmacological (tool compound), clinical (patient data)
   - Lead optimization: potency, selectivity, PK (bioavailability, half-life, CYP inhibition), solubility, stability
   - Efficacy: xenograft models, PDX models, syngeneic models, combination studies
   - Safety: 28-day and 90-day GLP tox in 2 species, safety pharmacology (CV, CNS, respiratory), Ames test, micronucleus
   - CMC: process route, analytical methods (HPLC, LC-MS), stability studies, formulation development
   - IND package: all nonclinical reports, clinical protocol, investigator brochure

5. CLINICAL DEVELOPMENT:
   - Phase I: dose escalation (BOIN or 3+3 design), 30-60 patients, PK/PD, safety, recommended Phase II dose (RP2D)
   - Phase II: expansion cohort or randomized Phase II, 100-200 patients, efficacy signal (ORR, PFS), biomarker analysis
   - Phase III: randomized controlled trial, 300-500 patients, OS or PFS primary endpoint, standard of care comparator
   - Adaptive design options: Bayesian response-adaptive randomization, seamless Phase I/II or II/III
   - Biostatistics: alpha spending function for interim analyses, futility stopping, overall survival as gold standard
   - Patient recruitment: academic medical centers, community oncology, patient advocacy partnerships

6. MANUFACTURING:
   - Process: route scouting → route optimization → process development → process validation
   - Analytical: method development, stability indicating, impurity profiling, reference standards
   - Supply: CRO/CDMO selection (Recipharm, Catalent, Lonza, Samsung Biologics depending on modality)
   - Scale: lab → pilot → clinical supply → commercial, with tech transfer packages
   - Quality: GMP compliance, CTD Module 3 documentation, batch release procedures
   - Cost: estimate COGS at commercial scale, identify cost drivers

7. TEAM:
   - Core: CSO (scientific lead), CMO (medical lead), VP Regulatory Affairs, VP Clinical Operations
   - KOL advisory board: 5-7 experts in the therapeutic area, balanced for academic and community oncology
   - CRO partners: clinical operations CRO, central lab, ECG, imaging core lab, biostatistics
   - CDMO partners: API manufacturer, drug product manufacturer, packaging/distribution

8. FUNDING:
   - Preclinical through IND: $10-20M (seed/Series A)
   - Phase I: $15-30M (Series A/B)
   - Phase II: $30-60M (Series B)
   - Phase III: $80-150M (Series C or partnership)
   - Total to approval: $150-400M depending on modality and indication
   - Non-dilutive: NCI grants, DOD funding, patient foundation grants, BARDA
   - Partnership economics: co-development deal structure, milestone payments, tiered royalties

9. RISKS:
   - Technical: target may not validate in humans, efficacy may not differentiate from existing therapies
   - Safety: on-target toxicity, immune-related adverse events (if immunotherapy), DDI, organ toxicity
   - Regulatory: clinical hold, CRL for insufficient efficacy, advisory committee concerns
   - Commercial: crowded market, pricing pressure, payer restrictions
   - Kill criteria: predefined efficacy thresholds (ORR <X%), safety stopping rules, futility boundaries
   - Contingency: combination strategy pivot, indication switch, device/drug combination, companion diagnostic co-development

10. TIMELINE:
    - Month 0-6: Target validation, IP filing, team assembly
    - Month 6-18: Lead optimization, IND-enabling studies
    - Month 18-24: IND filing, Phase I initiation
    - Month 24-36: Phase I completion, Phase II design
    - Month 36-54: Phase II execution, Phase III planning
    - Month 54-78: Phase III execution
    - Month 78-90: NDA/BLA submission and review
    - Month 90-96: Launch preparation and commercialization
    - Total: ~8 years from concept to approval (accelerated pathways may shorten by 1-2 years)

11. MARKET ACCESS:
    - HEOR strategy: QALY-based analysis, comparative effectiveness vs existing therapies
    - Payer engagement: early payer advisory boards, value dossier development
    - Pricing: reference pricing analysis, ICER review, outcomes-based contracts
    - Medical affairs: publication plan, medical education, KOL engagement
    - Launch: market research, market access, medical affairs, commercial team build-out

Provide a structured project plan with clear decision points, resource requirements, and risk-adjusted timelines. Include a summary dashboard format suitable for board and investor reporting.
```

## Notes
- Adjust development timelines and budgets based on modality (small molecule vs biologic vs cell/gene therapy)
- Factor in manufacturing complexity—cell therapy requires vein-to-vein time of weeks, not months
- Regulatory pathways vary significantly by country; plan parallel submissions for global markets
- Engage patient advocacy groups early for recruitment support and regulatory input
- Consider companion diagnostic co-development from Phase II onward
- Real-world evidence strategy should begin at approval, not after

## Tags
biotech, drug-development, regulatory-strategy, clinical-trials, IP-strategy, project-planning, biopharma, CMC, preclinical, commercialization, funding, manufacturing
