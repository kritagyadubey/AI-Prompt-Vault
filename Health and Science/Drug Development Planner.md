# Drug Development Planner
> Transforms pharmaceutical development ideas into structured pipeline plans with preclinical-to-market timelines, regulatory strategy, and clinical trial design.

## Purpose
Converts drug development concepts into comprehensive program plans covering target identification through commercialization, including regulatory strategy (FDA, EMA, PMDA), clinical development pathway, CMC requirements, intellectual property protection, pharmacovigilance, and market access. Structures the full drug lifecycle.

## Best For
- Small molecule drug development programs
- Biologic and biosimilar development
- Cell and gene therapy programs
- Vaccine development and licensure
- Combination drug/device products
- Drug repurposing and indication expansion
- Generic drug and ANDA strategy
- Pharmaceutical pipeline management
- IND/CTA application preparation
- Post-market surveillance and pharmacovigilance planning

## Prompt Enhancer
```text
Act as a senior pharmaceutical development strategist with expertise in drug development from target discovery through commercialization, regulatory affairs (FDA, EMA, PMDA, NMPA), clinical pharmacology, CMC, and pharmacovigilance. Transform the provided drug development concept into a comprehensive development plan by addressing:

1. TARGET AND MOLECULE DEFINITION: Define:
   - Therapeutic area and indication: primary and potential expanded indications with epidemiology
   - Target identification and validation: genetic evidence (GWAS, Mendelian randomization), pharmacological validation, druggability assessment
   - Modality: small molecule (oral, injectable), biologic (monoclonal antibody, bispecific, ADC), RNA therapeutic (ASO, siRNA, mRNA), cell therapy (CAR-T, TCR-T), gene therapy (AAV, lentiviral), peptide, oligonucleotide
   - Mechanism of action: binding site, signaling pathway, downstream effects, selectivity requirements
   - Target product profile (TPP): indication, route, dosing, efficacy benchmarks, safety profile, user profile, differentiation from existing therapies
   - Competitive landscape: current standard of care, unmet need, competing molecules in development (by phase and modality)
   - Druggability assessment: structural biology, binding site accessibility, pharmacological tractability

2. INTELLECTUAL PROPERTY STRATEGY: Plan comprehensive protection:
   - Freedom-to-operate (FTO) analysis: patent landscape, prior art, licensing needs
   - Patent strategy: composition of matter, method of use, formulation, manufacturing process, combination patents, biomarker companion diagnostics
   - Filing timeline: provisional → PCT → national phase entry (jurisdiction selection based on market), patent prosecution milestones
   - Regulatory exclusivity: orphan drug (7 years US), pediatric exclusivity (6 months), patent term extension (PTE, max 5 years), new chemical entity (5 years), new clinical investigation (3 years for NCEs), biologics (12 years BLA exclusivity)
   - Trade secret strategy: manufacturing know-how, formulation details, process parameters
   - Licensing: in-licensing for enabling technologies, out-licensing for non-core indications/geographies
   - IP budget: patent prosecution by jurisdiction, FTO opinion costs, litigation reserves

3. REGULATORY PATHWAY MAPPING: Design multi-agency strategy:
   - FDA pathway: IND → Phase I → Phase II → Phase III → NDA/BLA → Advisory Committee → PDUFA date → approval → post-market
     - Special designations: Breakthrough Therapy, Fast Track, Accelerated Approval, Priority Review, Rare Pediatric Disease
     - IND requirements: CMC package, nonclinical data, clinical protocol, investigator brochure
     - NDA/BLA content: CTD format (Module 1-5), clinical efficacy and safety, CMC, nonclinical, clinical pharmacology
   - EMA pathway: Scientific Advice → CTAs (per country) → Phase I → Phase II → Phase III → MAA → CHMP opinion → EC decision
     - PRIME designation (Parallel Scientific Advice with HTA bodies)
     - Conditional MA, accelerated assessment, exceptional circumstances
   - PMDA pathway: pre-IND consultation → clinical trial notification → Phase I-III → NDA → standard/max 12-month review
     - SAKIGAKE designation, conditional/time-limited approval, regenerative medicine products
   - China NMPA: IND application → clinical trial → NDA → priority review, breakthrough therapy
   - ICH harmonization: CTD, E6(R2) GCP, E8(R1) clinical trial design, E9(R1) estimands, E19 safety databases
   - Orphan drug strategy: prevalence criteria, market exclusivity benefits, development incentives per region

4. PRECLINICAL DEVELOPMENT PROGRAM: Structure:
   - Target validation: genetic (CRISPR KO/KI, conditional models), pharmacological (tool compounds), clinical (biomarker data, patient samples)
   - Lead optimization: SAR, selectivity, ADMET properties (absorption, distribution, metabolism, excretion, toxicity), physicochemical properties
   - PK/PD modeling: exposure-response relationships, dose projection, human dose prediction (allometric scaling, PBPK)
   - Efficacy studies: disease-relevant animal models, dose-response, PK/PD, combination studies, biomarker characterization
   - Safety pharmacology: CNS (Irwin test, FOB), cardiovascular (hERG, telemetry), respiratory (plethysmography) per ICH S7A/S7B
   - GLP toxicology: 28-day and 90-day studies in 2 species (rodent + non-rodent), NOAEL determination, dose-limiting toxicity
   - Genotoxicity: Ames test, in vitro micronucleus, in vivo micronucleus (ICH S2(R1))
   - Reproductive toxicity: fertility and early embryonic development (ICH 4.1.1), embryo-fetal development (4.1.2), pre/postnatal development (4.1.3)
   - Carcinogenicity: 2-year bioassay (if indicated by chronic dosing, genotoxicity signals, or TPP)
   - CMC package: synthetic route, process development, analytical methods (HPLC, LC-MS, XRPD), formulation development, stability studies (ICH Q1A-Q1E)
   - IND enabling package: integrated summary of safety (ISS), integrated summary of efficacy (ISE), individual study reports, CMC documentation

5. CLINICAL DEVELOPMENT PLAN: Design:
   - Phase I: first-in-human (FIH), single ascending dose (SAD), multiple ascending dose (MAD), food effect, food effect, mass balance (radiolabeled), special populations (hepatic/renal impairment), DDI studies
   - Phase II: proof-of-concept (efficacy signal), dose-finding (exposure-response), biomarker integration, adaptive designs (Bayesian, seamless I/II or II/III)
   - Phase III: pivotal trials, superiority vs non-inferiority, active comparator selection, endpoint validation, subgroup analyses, special populations
   - Phase IV/post-marketing: REMS, registry studies, PASS, post-marketing commitments, real-world evidence
   - Clinical pharmacology: DDI studies (CYP inhibition/induction, transporter studies), QT/QTc study (ICH E14), exposure-response, special populations
   - Biostatistics: estimand framework (ICH E9(R1)), SAP development, interim analyses (alpha spending), adaptive designs, Bayesian methods
   - Clinical operations: CRO selection, site selection and activation, enrollment projections, patient recruitment, data management, EDC systems

6. MANUFACTURING AND SUPPLY CHAIN: Plan:
   - Process development: route scouting, route optimization, process development, process validation (PPQ)
   - Analytical development: method development, validation (ICH Q2), reference standards, release testing, stability indicating methods
   - Formulation development: pre-formulation, formulation screening, scale-up, clinical trial material (CTM), commercial formulation
   - Supply chain: raw material sourcing, CMO/CDMO selection, cold chain management, inventory management
   - Quality systems: GMP compliance (21 CFR 210/211, EU GMP Annex 1), quality agreements, batch release, CAPA processes
   - Scale-up: lab → pilot → clinical → commercial scale, tech transfer packages
   - Cost of goods: raw material costs, manufacturing costs, COGS projections at commercial scale
   - Contingency: dual sourcing, safety stock, supply disruption protocols, second source strategy
   - For biologics: cell line development, upstream (bioreactor), downstream (purification), fill-finish, comparability studies

7. PHARMACOVIGILANCE AND SAFETY MONITORING: Design:
   - Safety database: MedDRA coding, ICSR (individual case safety report) processing, signal detection
   - Risk management plan (RMP): safety specification, pharmacovigilance plan, risk minimization measures
   - REMS (Risk Evaluation and Mitigation Strategy): if required by FDA, elements to assure safe use (ETASU)
   - DSMB/DMC charter: composition, meeting schedule, stopping rules, unblinding procedures
   - Safety monitoring: SAE reporting timelines (7/15-day), SUSAR reporting, DSUR (Development Safety Update Report)
   - Signal management: periodic safety update reports, signal detection algorithms, benefit-risk assessment (PrOACT-URL framework)
   - Long-term follow-up: registries, post-marketing surveillance, REMS assessments
   - Safety pharmacology follow-up: cardiovascular safety (ICH E14/S7B Q&A), hepatotoxicity (DILI assessment)

8. COMMERCIALIZATION AND MARKET ACCESS: Plan:
   - Market research: epidemiology, treatment landscape, patient journey mapping, KOL insights
   - Pricing and reimbursement: value-based pricing, health technology assessment (HTA) submissions (NICE, G-BA, CADTH, PBAC, HAS), ICER review
   - Market access strategy: payer engagement, formulary positioning, outcomes-based contracts, patient assistance programs
   - Medical affairs: publication plan, medical education, medical science liaison (MSL) strategy, advisory boards
   - Commercial readiness: market research, KOL mapping, medical affairs, medical science liaison strategy
   - Launch preparation: pre-launch (2 years), launch, post-launch activities and KPIs
   - Global launch sequencing: US first (highest price), EU, Japan, RoW, emerging markets
   - Lifecycle management: line extensions, new indications, formulation improvements, combination products, pediatric development

9. TEAM AND ORGANIZATIONAL STRUCTURE: Define:
   - Core executive team: CSO, CMO, CTO (CMC), VP Regulatory Affairs, VP Clinical Operations, VP Commercial
   - KOL advisory board: therapeutic area experts, regulatory consultants, HTA experts, commercial advisors
   - CRO/CDMO/CMO partnerships: selection criteria, scope of work, governance structure
   - Organizational growth: hiring timeline aligned with development stages (preclinical → clinical → commercial)
   - Key hires by phase: preclinical (toxicologists, CMC), Phase I (clinical pharmacologists), Phase II (medical directors, biostatisticians), Phase III (regulatory, commercial), approval (medical affairs, pharmacovigilance)
   - Board composition and governance: independent directors, audit committee, compensation committee

10. FUNDING AND FINANCIAL PLANNING: Build:
    - Development budget: phase-by-phase cost estimates with confidence ranges
    - Funding strategy: seed → Series A → Series B → Series C → partnership/licensing → IPO → commercial
    - Non-dilutive funding: SBIR/STTR, NIH grants (NCI, NHLBI, NIAID), DOD, BARDA, CIRM, foundation grants
    - Valuation milestones: preclinical, IND, Phase I, Phase II, Phase III, NDA/BLA, approval
    - Cash flow projections: burn rate, runway, milestones that unlock financing
    - Partnership economics: deal structures (co-development, licensing, co-promotion), milestone payments, tiered royalties, equity stakes
    - IPO readiness: timeline, governance requirements, SOX compliance
    - Comparable transactions: recent deals in the therapeutic area, valuation benchmarks

11. RISK MANAGEMENT AND CONTINGENCY: Identify:
    - Technical: target validation failure, efficacy gap, safety signals, manufacturing challenges, formulation instability
    - Regulatory: clinical hold, Complete Response Letter, advisory committee negative vote, REMS requirements
    - Commercial: market competition, payer restrictions, pricing pressure, adoption barriers
    - Financial: funding gap, dilution, bridge financing, market downturn
    - IP: patent challenges (IPR/PGR), FTO issues, licensing failures, patent term limitations
    - Operational: CRO performance, site enrollment, data quality issues, supply chain disruption
    - Kill criteria: predefined stopping rules for each phase to preserve capital
    - Scenario planning: best case, base case, worst case timelines and funding needs
    - Hedge strategies: parallel development paths, option agreements, pre-negotiated term sheets

12. MILESTONES AND TIMELINE: Create development roadmap:
    - Target identification and validation (0-12 months)
    - Lead optimization and candidate selection (12-24 months)
    - IND-enabling studies and IND filing (24-36 months)
    - Phase I clinical trial (36-48 months)
    - Phase II clinical trial (48-66 months)
    - Phase III clinical trial (66-90 months)
    - NDA/BLA submission and review (90-102 months)
    - Commercial launch (102-108 months)
    - Total: approximately 9-11 years from concept to approval (accelerated pathways may shorten by 2-3 years)
    - Critical path identification and buffer allocation
    - Key decision points and go/no-go criteria at each milestone

13. GLOBAL REGULATORY HARMONIZATION: Address:
    - ICH guidelines: E6(R2) GCP, E8(R1) trial design, E9(R1) estimands, E14 QT study, M4 CTD
    - Regional variations: FDA vs EMA vs PMDA requirements, bridging studies, ethnic factors (ICH E5)
    - Multi-regional clinical trials (MRCTs): design, conduct, data sharing, regulatory submissions
    - Global clinical trial registry: ClinicalTrials.gov, EU Clinical Trials Register, WHO ICTRP
    - Data privacy: HIPAA (US), GDPR (EU), PIPA (Japan), PIPL (China), cross-border data transfer
    - Local regulatory requirements: language, labeling, packaging, distribution, import/export

14. REAL-WORLD EVIDENCE AND LIFECYCLE: Plan post-approval strategy:
    - Real-world evidence (RWE): claims data, EHR data, registries, patient-reported outcomes
    - Post-marketing commitments: PASS, PMC, registry studies
    - Label expansion: new indications, new populations, new formulations
    - Lifecycle management: line extensions, 505(b)(2) pathway, combination products
    - Competitive intelligence: pipeline monitoring, patent landscape, regulatory intelligence
    - Benefit-risk reassessment: periodic PSURs, advisory committees, labeling updates

Provide a structured development plan with clear decision points, resource requirements, risk-adjusted timelines, and a summary dashboard format suitable for board and investor reporting. Include go/no-go criteria at each major milestone.
```

## Example
### Original Prompt
```text
I want to develop a new drug for Alzheimer's disease. Plan the development program.
```

### Enhanced Prompt
```text
Act as a senior pharmaceutical development strategist with expertise in drug development from target discovery through commercialization, regulatory affairs (FDA, EMA, PMDA, NMPA), clinical pharmacology, CMC, and pharmacovigilance. Transform the provided drug development concept into a comprehensive development plan for a novel Alzheimer's disease therapy:

1. TARGET AND MOLECULE: Define:
   - Therapeutic area: Alzheimer's disease (AD), estimated 6.9 million Americans age 65+ living with AD (Alzheimer's Association 2025), projected to reach 13 million by 2050
   - Target: what mechanism? Anti-amyloid (lecanemab, donanemab precedent), anti-tau, neuroinflammation (microglial modulation), metabolic (GLP-1 RA), synaptic protection, combination
   - Unmet need: existing anti-amyloid antibodies (lecanemab, donanemab) show modest clinical benefit (CDR-SB 27-35% slowing); need for disease-modifying therapies addressing tau, neuroinflammation, and/or synapse loss
   - Competitive landscape: anti-amyloid (lecanemab, donanemab, aducanumab), anti-tau (semorinemab, zagotenemab), neuroinflammation (AL002, DSP-1181), metabolic (oral semaglutide in trial)
   - TPP: indication (early AD, MCI due to AD, mild-moderate AD), route (IV vs subcutaneous vs oral), dosing schedule, efficacy (CDR-SB, ADCS-ADL, amyloid PET reduction), safety profile

2. IP STRATEGY:
   - FTO analysis: patent landscape for mechanism, specific molecule, formulation, dosing regimen
   - Filing: composition of matter patent (provisional → PCT → national phase), method of use (AD indication), formulation patents, combination therapy patents
   - Orphan drug designation: AD prevalence >200,000 in US — does NOT qualify for orphan designation (requires <200,000); however, specific rare AD subtypes (familial AD, early-onset) may qualify
   - PTE: if applicable, extend patent term for regulatory delay
   - Licensing: in-license enabling technologies (brain delivery enhancement, biomarker assays)

3. REGULATORY PATHWAY:
   - FDA: pre-IND meeting (type B, focused on clinical trial design and endpoints), IND filing, Breakthrough Therapy designation consideration (if preliminary evidence shows substantial improvement over existing therapies)
   - Accelerated Approval: consider amyloid PET or CSF biomarker as surrogate endpoint for accelerated approval, with post-marketing confirmatory trial
   - Priority Review: 6-month review clock if targeting serious condition with unmet need
   - Real-World Evidence: FDA may accept RWE for label expansion (21st Century Cures Act)
   - EMA: PRIME designation, Scientific Advice, conditional MA if accelerated pathway
   - PMDA: SAKIGAKE designation for innovative therapies, conditional approval
   - Orphan Drug: assess familial AD or rare AD subtypes (prevalence <200,000 in US)

4. PRECLINICAL:
   - Target validation: genetic (APOE4, TREM2, PSEN1/2), pharmacological (tool compound in transgenic models), clinical (biomarker data from existing studies)
   - Animal models: 5xFAD, APP/PS1, Tau(P301S) transgenic mice, non-human primate models (for CNS penetration assessment)
   - Efficacy: cognitive testing (Morris water maze, Y-maze, novel object recognition), neuropathology (amyloid plaque load, tau tangles, synapse density, neuroinflammation)
   - Safety pharmacology: CNS (behavioral assessment), cardiovascular (hERG, telemetry), respiratory
   - GLP tox: 28-day and 90-day in 2 species, CNS safety margin, BBB penetration assessment
   - CMC: formulation for IV/SC delivery, stability, lyophilization if biologic, analytical methods
   - Biomarker strategy: amyloid PET, tau PET, CSF Aβ42/40 ratio, p-tau181/217, NfL, GFAP, neurofilament

5. CLINICAL DEVELOPMENT:
   - Phase I: SAD/MAD in healthy volunteers and mild AD patients, food effect, DDI (if CYP-metabolized), PET imaging sub-study to confirm target engagement
   - Phase II: proof-of-concept, 200-300 patients, dose-finding, biomarker enrichment (amyloid-positive by PET or CSF), adaptive design (Bayesian response-adaptive), primary endpoint CDR-SB or ADAS-Cog, secondary: ADCS-ADL, biomarkers (amyloid PET SUVr, tau PET, CSF markers)
   - Phase III: pivotal trials, 1000-2000 patients, randomized double-blind, active comparator (lecanemab or donepezil), primary endpoint CDR-SB, key secondary ADCS-ADL, amyloid PET as surrogate for accelerated approval, 18-month treatment duration, enrichment by amyloid positivity
   - Adaptive design: seamless Phase II/III, Bayesian response-adaptive randomization, biomarker-based enrichment, futility stopping rules
   - Special populations: APOE4 carriers vs non-carriers (stratification), age subgroups, comorbidities
   - Clinical pharmacology: BBB penetration assessment, PET PK studies, DDI with common AD medications (donepezil, memantine, rivastigmine), QT study (ICH E14)

6. MANUFACTURING:
   - If biologic: cell line development, upstream bioreactor (CHO cells), downstream purification (Protein A affinity), analytical characterization (SEC, cIEF, peptide mapping), fill-finish (lyophilization or liquid), comparability studies for process changes
   - If small molecule: synthetic route optimization, process development, API manufacturing, formulation (oral or IV), stability studies (ICH conditions), reference standards
   - Scale-up: lab → pilot → clinical supply → commercial, with tech transfer packages
   - Supply: CDMO selection (Lonza, Samsung Biologics for biologics; Catalent, Recipharm for small molecule)
   - Quality: GMP compliance, CTD Module 3 documentation, batch release procedures, stability program

7. PHARMACOVIGILANCE:
   - Safety database: MedDRA coding, ICSR processing (7/15-day SAE reporting, SUSARs)
   - ARIA monitoring: amyloid-related imaging abnormalities (ARIA-E, ARIA-H) — mandatory monitoring with MRI per FDA guidance
   - DSMB/DMC: composition (neurologist, biostatistician, patient representative), ARIA monitoring, stopping rules for safety signals
   - RMP: safety specification, pharmacovigilance plan, risk minimization (ARIA monitoring, REMS if required)
   - Long-term follow-up: registry studies, 10-year safety follow-up as per FDA expectation for disease-modifying AD therapies
   - Signal management: hepatotoxicity, immunogenicity (if biologic), infusion reactions, ARIA detection

8. MARKET ACCESS:
   - HTA: NICE (UK), G-BA (Germany), CADTH (Canada), PBAC (Australia), HAS (France) submissions
   - Value proposition: slowing cognitive decline, maintaining independence, reducing caregiver burden, societal cost savings
   - Pricing: reference pricing, ICER review, outcomes-based contracts, indication-based pricing
   - Payer engagement: early advisory boards, real-world evidence generation, patient registries
   - Patient assistance: copay programs, foundation support, hub services, specialty pharmacy distribution
   - Global launch: US first (highest price), EU, Japan, key emerging markets

9. TEAM:
   - Core: CSO (neuroscience), CMO (AD clinical expert), VP Regulatory (FDA/EMA experience), VP Clinical Operations (CNS trial expertise), VP Commercial (neurology launch experience)
   - Advisory board: 5-7 AD KOLs (academic neurologists, geriatric psychiatrists), regulatory consultants, HTA experts
   - CRO partners: IQVIA, Parexel, Covance for clinical operations; ERT, Bioclinica for imaging; Eurofins, Covance for central lab
   - CDMO: Lonza, Samsung Biologics (biologics), Catalent (small molecule/formulation)

10. FUNDING:
    - Preclinical through IND: $20-40M (Series A)
    - Phase I: $20-40M (Series A/B)
    - Phase II: $50-100M (Series B)
    - Phase III: $150-300M (Series C or partnership)
    - NDA/BLA and launch: $50-100M (Series D or partnership)
    - Total to approval: $300-600M (AD is one of the most expensive therapeutic areas)
    - Non-dilutive: NIH (NIA), BARDA, Alzheimer's Drug Discovery Foundation, Michael J. Fox Foundation (if Parkinson's overlap)
    - Partnership: pharma co-development, licensing deals (Pfizer, Roche, Biogen have AD track records)

11. RISKS:
    - Technical: mechanism may not translate from animal models to human AD, efficacy may be modest (15-30% CDR-SB slowing), ARIA safety concerns, brain delivery challenges
    - Regulatory: amyloid hypothesis still debated, surrogate endpoint acceptance uncertain, accelerated approval risk (may require confirmatory trial)
    - Commercial: existing anti-amyloid antibodies (lecanemab, donanemab) are first-movers, differentiation required, payer resistance to high prices, diagnostic burden (amyloid PET required)
    - Financial: AD trials are long (18+ months), large (1000+ patients), expensive, high failure rate
    - Kill criteria: Phase II futility (CDR-SB <10% slowing), safety signal (ARIA-E >30%), biomarker non-engagement

12. TIMELINE:
    - Month 0-12: target validation, lead optimization, IP filing
    - Month 12-24: candidate selection, IND-enabling studies
    - Month 24-30: IND filing, pre-IND meetings, Breakthrough Therapy designation application
    - Month 30-42: Phase I (SAD/MAD, food effect, PET imaging sub-study)
    - Month 42-60: Phase II (proof-of-concept, dose-finding, adaptive design)
    - Month 60-84: Phase III (pivotal trials, 1000+ patients, 18-month treatment)
    - Month 84-96: NDA/BLA submission and FDA review
    - Month 96-102: commercial launch preparation, market access, manufacturing scale-up
    - Total: ~8.5 years from concept to approval (accelerated pathways may shorten by 1-2 years)

Provide a structured development plan with clear decision points, resource requirements, risk-adjusted timelines, and a summary dashboard format suitable for board and investor reporting. Include go/no-go criteria at each major milestone.
```

## Notes
- AD drug development is one of the highest-risk therapeutic areas; ~99% failure rate in clinical trials
- Anti-amyloid hypothesis remains controversial; diversify pipeline if possible (tau, inflammation, metabolic)
- ARIA monitoring is mandatory for anti-amyloid therapies; requires MRI infrastructure and trained readers
- Patient recruitment for AD trials is challenging; plan 18-24 month enrollment window
- Partnering with academic medical centers and AD research centers is essential for enrollment
- Real-world evidence strategy should begin at approval, especially for label expansion
- Consider companion diagnostic co-development (amyloid PET, CSF biomarkers)

## Tags
drug-development, pharmaceutical, clinical-trials, regulatory-strategy, FDA, EMA, CMC, pharmacovigilance, Alzheimer, biologics, small-molecule, pipeline-management, market-access, HTA, REMS, GCP
