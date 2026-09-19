# Clinical Research Designer
> Enhances prompts for rigorous clinical study design, protocol development, and regulatory-compliant research methodologies.

## Purpose
Transforms vague clinical research ideas into structured, IRB-ready protocols with proper statistical power, inclusion/exclusion criteria, and regulatory alignment. Converts general health questions into systematic, evidence-based clinical investigation frameworks.

## Best For
- Clinical trial protocol development
- Study design methodology selection
- Sample size and power calculations
- Endpoint and outcome measure definition
- IRB/Ethics committee submission preparation
- Observational study design (cohort, case-control, cross-sectional)

## Prompt Enhancer
```text
Act as a senior clinical research methodologist with expertise in study design, biostatistics, and regulatory compliance (ICH-GCP, FDA IND/IDE requirements). Transform the following clinical research concept into a structured study protocol outline by addressing:

1. STUDY OBJECTIVES: Define primary and secondary endpoints using the PICO(S) framework (Population, Intervention, Comparison, Outcome, Study design). Specify measurable, time-bound endpoints with operational definitions.

2. STUDY DESIGN: Recommend the most appropriate design (RCT, crossover, parallel-group, factorial, adaptive, observational) and justify the choice against alternatives. Specify blinding strategy (open-label, single-blind, double-blind) with rationale.

3. POPULATION: Define inclusion and exclusion criteria that balance generalizability with internal validity. Specify target population, accessible population, and sample. Address recruitment strategy and anticipated enrollment challenges.

4. SAMPLE SIZE: Calculate required sample size using appropriate power analysis (specify alpha, power, expected effect size, attrition rate). Reference relevant prior studies for effect size estimation. State assumptions explicitly.

5. INTERVENTION/EXPOSURE: Describe the intervention or exposure protocol with sufficient detail for replication. Include dosing, timing, delivery method, and standardization procedures. Define co-interventions and prohibited concomitant medications.

6. COMPARATOR: Specify control conditions (placebo, active comparator, standard of care, no treatment). Justify the choice and address masking/concealment.

7. OUTCOMES MEASUREMENT: Define each endpoint with measurement instrument, timing of assessment, response options, and validated scoring systems where applicable. Specify biological sample collection protocols if relevant.

8. STATISTICAL ANALYSIS PLAN: Outline primary analysis methods, handling of missing data (multiple imputation, sensitivity analyses), subgroup analyses, interim analyses, and stopping rules. Specify software and version.

9. SAFETY MONITORING: Describe adverse event classification (CTCAE grading), monitoring frequency, Data Safety Monitoring Board (DSMB) composition and charter, stopping boundaries, and communication plan.

10. ETHICAL CONSIDERATIONS: Address informed consent process, risk-benefit assessment, vulnerable populations, data privacy (HIPAA/GDPR), compensation, and post-trial access.

11. TIMELINE: Create a realistic project timeline with milestones (IRB submission, first patient in, database lock, primary analysis, manuscript submission).

12. REGULATORY PATHWAY: Identify applicable regulatory requirements, registration requirements (ClinicalTrials.gov, WHO ICTRP), and reporting standards (CONSORT, STROBE, PRISMA as appropriate).

Support all recommendations with citations to current guidelines, Cochrane methodology standards, or relevant regulatory documents. Flag areas where institutional or local factors may require protocol modifications.
```

## Example
### Original Prompt
```text
I want to study whether meditation helps people with anxiety. Design a study for this.
```

### Enhanced Prompt
```text
Act as a senior clinical research methodologist with expertise in study design, biostatistics, and regulatory compliance (ICH-GCP, FDA IND/IDE requirements). Transform the following clinical research concept into a structured study protocol outline by addressing:

1. STUDY OBJECTIVES: Define primary and secondary endpoints using the PICO(S) framework. The concept is investigating mindfulness-based stress reduction (MBSR) for generalized anxiety disorder (GAD). Primary endpoint could be change in GAD-7 score at 8 weeks. Secondary endpoints: HAM-A response rates, remission rates, quality of life (SF-36), sleep quality (PSQI), and cortisol levels. Specify time-bound endpoints with operational definitions.

2. STUDY DESIGN: Recommend the most appropriate design and justify against alternatives. Consider: parallel-group RCT (MBSR vs. waitlist control vs. active comparator such as psychoeducation), with 1:1:1 randomization. Address whether an adaptive design might be efficient. Specify double-blind is not feasible for behavioral interventions but outline assessor blinding strategy.

3. POPULATION: Adults aged 18-65 with DSM-5 diagnosed GAD (GAD-7 score ≥10). Inclusion: stable medication regimen ≥4 weeks or medication-free; willing to attend 8 weekly sessions. Exclusion: active suicidal ideation, psychosis, substance use disorder, concurrent psychotherapy, meditation experience >6 months. Address recruitment through outpatient psychiatry clinics and community advertising.

4. SAMPLE SIZE: Using a medium effect size (Cohen's d = 0.5) based on meta-analyses (Hofmann et al., 2010), alpha = 0.05 (two-sided), power = 0.90, and 20% attrition, calculate required enrollment. Reference specific prior studies for effect size justification.

5. INTERVENTION: Standardized 8-week MBSR protocol (Kabat-Zinn format) with weekly 2-hour group sessions plus one full-day retreat. Home practice: 45 minutes/day, 6 days/week. Therapist qualifications: certified MBSR instructor with ≥3 years experience. Treatment fidelity: session audio recording, fidelity checklist adherence ≥80%.

6. COMPARATOR: Active comparator arm: 8-week psychoeducation program matched for time, therapist contact, and group format. Waitlist control: offered MBSR after study completion. Define standardization procedures for both.

7. OUTCOMES MEASUREMENT: Primary: GAD-7 administered at baseline, weeks 4, 8, 12, and 24 (follow-up). Secondary: HAM-A (clinician-rated) at baseline, week 8, week 24; cortisol sampling (awakening response) at baseline and week 8; SF-36 and PSQI at baseline and week 8. Specify biological sample collection (saliva) protocols with collection time windows.

8. STATISTICAL ANALYSIS PLAN: Mixed-effects model for repeated measures (MMRM) for primary endpoint. Intent-to-treat population. Handle missing data via multiple imputation with sensitivity analyses (complete case, last observation carried forward). Pre-specified subgroup analyses by baseline severity, medication status, and prior meditation experience. No interim analyses planned for this sample size.

9. SAFETY MONITORING: Adverse event monitoring at each session and follow-up. DSMB oversight not required for this minimal-risk study per IRB guidance, but safety review at 50% enrollment. Suicidality screening (C-SSRS) at each visit. Stopping rule: if ≥30% of MBSR participants report clinically significant worsening.

10. ETHICAL CONSIDERATIONS: Written informed consent. HIPAA-compliant data storage. No deception. Participants with clinically significant worsening referred to treatment. IRB approval from [institution]. Registration on ClinicalTrials.gov prior to enrollment.

11. TIMELINE: Month 1-2: Protocol finalization and IRB submission. Month 3: IRB approval and registration. Month 4-5: Recruitment and screening. Month 6-9: Intervention delivery (rolling enrollment). Month 10: 8-week follow-up. Month 15: 24-week follow-up. Month 16-18: Analysis and manuscript.

12. REGULATORY: No IND required (behavioral intervention). ClinicalTrials.gov registration required prior to first participant enrollment. CONSORT reporting standards. ICH-GCP compliance for data integrity.

Support all recommendations with citations to current guidelines, Cochrane methodology standards, or relevant regulatory documents. Flag areas where institutional or local factors may require protocol modifications.
```

## Notes
- Always verify sample size calculations with a biostatistician before finalizing protocols
- Adjust regulatory pathway based on whether intervention is drug, device, biologic, or behavioral
- Consider CONSORT 2010 extension for non-pharmacologic treatments for behavioral interventions
- Protocol should be reviewed by a methodologist not involved in the study design
- Factor in local IRB requirements which may exceed federal minimums
- For multi-site studies, consider a Data Coordinating Center (DCC) structure

## Tags
clinical-research, study-design, protocol-development, RCT, biostatistics, IRB, regulatory, GCP, PICO, sample-size, CONSORT, clinical-trials
