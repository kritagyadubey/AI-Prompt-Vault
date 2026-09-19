# Public Health Researcher
> Transforms public health queries into systematic, population-level research frameworks with epidemiological rigor and health equity considerations.

## Purpose
Converts general public health questions into structured research analyses incorporating epidemiological methods, biostatistics, health surveillance data, social determinants of health, and policy evaluation frameworks. Ensures population-level thinking with disaggregated data analysis.

## Best For
- Epidemiological study design and analysis
- Disease surveillance and outbreak investigation
- Health disparities and equity assessments
- Program evaluation and cost-effectiveness analysis
- Systematic reviews and meta-analyses of public health interventions
- Policy impact assessment
- Community health needs assessments
- Health behavior and social determinants research

## Prompt Enhancer
```text
Act as a senior epidemiologist and public health researcher with expertise in study design, biostatistics, health equity frameworks, and program evaluation. Transform the provided public health query into a structured research framework by addressing:

1. EPIDEMIOLOGICAL FRAMING: Define the health problem using epidemiological metrics:
   - Incidence (cumulative and person-time), prevalence (point and period), mortality rates (crude, age-adjusted, cause-specific)
   - Morbidity measures: risk ratios, odds ratios, attributable risk, population attributable risk percent
   - Screening test characteristics: sensitivity, specificity, PPV, NPV, AUC-ROC
   - Natural history of disease: latency period, incubation period, chronicity, staging
   - Communicable disease specifics: R₀, secondary attack rate, herd immunity threshold, serial interval
   - Apply the epidemiologic triad (agent-host-environment) or web of causation as appropriate

2. POPULATION AND DISAGGREGATION: Specify:
   - Target population and denominator data sources (census, vital statistics, administrative data)
   - Required stratification: age, sex, race/ethnicity, socioeconomic status, geography, disability status
   - Health equity lens: identify which populations bear disproportionate burden and why
   - Social determinants of health (SDOH) framework: economic stability, education access, healthcare access, neighborhood/built environment, social/community context
   - Data sovereignty considerations for Indigenous and minoritized populations

3. DATA SOURCES AND SURVEILLANCE: Identify appropriate data sources:
   - National surveys: NHANES, BRFSS, MEPS, YRBSS, NSDUH, HOS
   - Disease registries: cancer (SEER, NCDB), birth defects, trauma, HIV
   - Administrative data: Medicaid/Medicare claims, hospital discharge (HCUP/NIS), ED visits
   - Vital statistics: death certificates (NVSS), birth certificates, fetal death records
   - Surveillance systems: FoodNet, NNDSS, BioSense, syndromic surveillance
   - Global data: WHO GHO, IHME GBD, DHS, MICS
   - Real-time data: wastewater surveillance, wastewater epidemiology, digital surveillance
   - Address data quality: representativeness, response rates, misclassification bias, ecological fallacy

4. STUDY DESIGN SELECTION: Recommend and justify the most appropriate design:
   - Descriptive: cross-sectional, ecological, case series, case reports
   - Analytical: cohort (prospective/retrospective), case-control, matched designs
   - Experimental: cluster RCT, stepped-wedge, community intervention trials
   - Quasi-experimental: interrupted time series, difference-in-differences, regression discontinuity, synthetic control
   - Surveillance: sentinel surveillance, syndromic surveillance, active vs passive
   - Mixed methods: convergent, explanatory sequential, community-based participatory research (CBPR)
   Justify design choice against alternatives considering feasibility, ethics, bias, and confounding.

5. MEASURES AND ANALYTICS: Specify:
   - Primary and secondary outcome measures with operational definitions
   - Confounding control: directed acyclic graphs (DAGs), stratification, multivariable regression, propensity scores, instrumental variables
   - Effect modification assessment and reporting
   - Spatial analysis methods if geographic variation is relevant (GIS, spatial autocorrelation, Getis-Ord Gi*)
   - Time-series analysis for trend data (joinpoint regression, Poisson regression, ARIMA)
   - Missing data handling: multiple imputation, inverse probability weighting, sensitivity analyses
   - Software requirements: SAS, R, Stata, Python with specific packages

6. HEALTH EQUITY ANALYSIS: Integrate equity throughout:
   - Apply PROGRESS-Plus framework (Place of residence, Race/ethnicity, Occupation, Gender/sex, Religion, Education, Socioeconomic status, Social capital + age, disability)
   - Measure disparities: absolute (rate difference), relative (rate ratio), index of disparity, concentration index
   - Assess structural determinants: policy context, historical context, institutional practices
   - Community engagement: CBPR principles, community advisory boards, participatory data analysis
   - Intersectionality: how multiple identities compound health risks
   - Translation: disaggregated results, community-facing summaries, policy briefs

7. POLICY AND PROGRAM EVALUATION: If applicable, apply:
   - Logic models (inputs → activities → outputs → outcomes → impact)
   - RE-AIM framework (Reach, Effectiveness, Adoption, Implementation, Maintenance)
   - Cost-effectiveness analysis: ICER, budget impact, societal perspective
   - Implementation science: RE-AIM, CFIR, constructs of implementation
   - Policy analysis frameworks: CDC Policy Process (Problem structuring, stakeholder analysis, options analysis, decisionmaking, implementation, evaluation)
   - Natural experiments and quasi-experimental evaluation designs

8. QUALITY AND BIAS ASSESSMENT: Systematically evaluate:
   - Risk of bias tools: ROBINS-I (non-randomized), Cochrane RoB 2 (randomized), QUADAS-2 (diagnostic), Newcastle-Ottawa Scale (observational)
   - GRADE evidence quality assessment (high/moderate/low/very low)
   - Threats to validity: selection bias, information bias, confounding, reverse causation, Healthy worker effect, Berkson's bias, surveillance bias
   - Sensitivity analyses to test robustness of findings
   - E-value for unmeasured confounding assessment

9. REPORTING AND DISSEMINATION: Structure output per:
   - STROBE (observational), CONSORT (RCT), PRISMA (systematic review), RECORD (administrative data), CHEERS (economic evaluation), TRIPOD (prediction models)
   - Plain-language summaries for community stakeholders
   - Policy brief format for decision-makers
   - Data visualization: epidemiological curves, forest plots, population pyramids, choropleth maps, dose-response curves
   - Press releases and media talking points for public communication

10. ETHICAL AND EQUITY CONSIDERATIONS: Address:
    - IRB requirements and waiver criteria for public health surveillance
    - Data privacy: HIPAA, FERPA, 42 CFR Part 2 (substance use), certificate of confidentiality
    - Dual-use research of concern (DURC) for pathogen research
    - Community benefit agreements and data sharing protocols
    - Stigmatization risk in population-level reporting
    - Historically unethical research practices and community trust-building

Flag areas where local data, community input, or specialist expertise is essential. Provide a quality checklist and dissemination plan tailored to the intended audience.
```

## Example
### Original Prompt
```text
Research childhood obesity trends in the US.
```

### Enhanced Prompt
```text
Act as a senior epidemiologist and public health researcher with expertise in study design, biostatistics, health equity frameworks, and program evaluation. Transform the provided public health query into a structured research framework by addressing childhood obesity trends in the United States:

1. EPIDEMIOLOGICAL FRAMING: Define the problem:
   - Prevalence: 19.7% of US children/adolescents aged 2-19 (NHANES 2017-2020), approximately 14.7 million affected
   - Trends: Increased from 13.9% (1999-2000) to 19.7% (2017-2020), accelerating during COVID-19 pandemic
   - Severity stratification: obesity (BMI ≥95th percentile) vs severe obesity (BMI ≥120% of 95th percentile, ~6.1%)
   - Comorbidities: type 2 diabetes, NAFLD, asthma, sleep apnea, depression, orthopedic complications
   - Economic burden: $14.1B in attributable healthcare costs annually (FAIR Health)
   - Life expectancy impact: estimated 2-5 years reduction in life expectancy for severely obese adolescents
   - Metrics: BMI-for-age z-scores, percentiles, change in z-score, incidence of obesity onset

2. POPULATION AND DISAGGREGATION: Stratify by:
   - Age: preschool (2-5), school-age (6-11), adolescents (12-19)
   - Race/ethnicity: Non-Hispanic Black (26.2%), Hispanic (24.8%), Non-Hispanic White (16.6%), Non-Hispanic Asian (9.0%)
   - Socioeconomic status: household income, parental education, food security status
   - Geography: regional variation (South highest), urban-rural, WIC participation areas
   - SDOH: food desert access, neighborhood walkability, park availability, school meal program participation
   - Intersectionality: race × sex × SES interactions, disability status

3. DATA SOURCES: Identify primary sources:
   - NHANES (national, measured heights/weights, biomarkers, dietary recall)
   - YRBSS (state/local, self-reported, school-based)
   - Early Childhood Longitudinal Study (ECLS-K:2011, birth cohort)
   - Pediatric Nutrition Surveillance System (PedNSS, WIC/School programs)
   - Electronic health records (EHR) from learning health systems
   - US Census and ACS for denominator and SDOH data
   - USDA Food Access Research Atlas for food environment
   - CDC growth charts and WHO growth standards for reference
   - Address: NHANES oversampling design, self-report bias, measurement standardization

4. STUDY DESIGN: Recommend mixed-methods approach:
   - Trend analysis: repeated cross-sectional (NHANES cycles 1999-2020), joinpoint regression to identify inflection points
   - Cohort analysis: ECLS-K longitudinal trajectories using growth mixture modeling
   - Ecological analysis: county-level obesity prevalence with spatial autocorrelation (Getis-Ord Gi*)
   - Quasi-experimental: evaluate policy impacts (SSB taxes, school nutrition standards) using difference-in-differences
   - Qualitative: community-based participatory research (CBPR) with affected families
   - Justification: Trend analysis captures population-level changes; cohort identifies risk/protective factors; ecological examines environmental determinants

5. MEASURES AND ANALYTICS: Specify:
   - Primary outcome: change in prevalence of obesity (BMI ≥95th percentile) over time
   - Secondary outcomes: severe obesity prevalence, incidence of comorbidities, healthcare utilization
   - Confounding control: DAGs for temporal trends, multilevel models (children nested in schools nested in counties)
   - Spatial analysis: SaTScan for cluster detection, spatial lag models
   - Time-series: joinpoint regression for trend segmentation, Poisson regression for incidence
   - Missing data: multiple imputation with chained equations, full information maximum likelihood
   - Software: R (survey, lme4, spdep, joinpoint), SAS (survey procedures), QGIS

6. HEALTH EQUITY ANALYSIS:
   - Disparities: absolute disparity (26.2% - 9.0% = 17.2 percentage points between highest and lowest racial groups)
   - Relative disparity: Non-Hispanic Black children 1.62x more likely to have obesity than Non-Hispanic White children
   - Structural determinants: food apartheid, residential segregation, marketing exposure (Black youth see 2x more food ads), built environment inequities
   - CBPR: partner with community organizations (churches, schools, community centers) for data collection and intervention design
   - Intersectionality: how race × SES × geography compound risk
   - Translation: community-facing infographic in multiple languages, school board presentations

7. POLICY EVALUATION: Apply RE-AIM and logic models to evaluate:
   - SSB taxes: Seattle, Philadelphia, Berkeley—what are measured impacts on purchasing and weight outcomes?
   - School nutrition standards: HHFKA 2012 impact on BMI trajectories
   - SNAP-Ed and WIC nutrition education programs
   - Built environment interventions: Complete Streets, park investments
   - Cost-effectiveness: ICER for policy interventions vs individual-level treatment
   - Implementation: CFIR assessment of adoption barriers in schools and communities

8. QUALITY AND BIAS: Address:
   - ROBINS-I for quasi-experimental evaluations
   - GRADE assessment for evidence certainty
   - Threats: measurement bias (self-report vs measured), Healthy migrant effect, selection bias in surveys, ecological fallacy
   - Sensitivity analyses: complete case, inverse probability weighting, alternative BMI definitions
   - E-value: assess potential for unmeasured confounding in observational analyses

9. REPORTING: Structure per:
   - STROBE for observational analyses, RECORD for administrative data
   - CHEERS for economic evaluations
   - Plain-language summary for parents and community members
   - Policy brief for state/local health departments
   - Data visualization: trend lines with 95% CIs, forest plots for subgroup analyses, choropleth maps, population pyramids

10. ETHICAL: Address:
    - Stigmatization risk in childhood obesity research: use person-first language ("children with obesity" not "obese children")
    - Data privacy for minors: assent/consent requirements, FERPA for school-based data
    - Community trust: historical exploitation, community benefit agreements
    - Dual-use: none anticipated, but acknowledge potential for misuse of data

Flag areas requiring local data, community input, or specialist expertise (pediatric endocrinology, nutrition science, urban planning).
```

## Notes
- Always contextualize findings within the Healthy People 2030 objectives for the relevant condition
- Consider seasonality, secular trends, and data collection artifacts when analyzing temporal data
- For global health comparisons, standardize metrics and account for data quality differences across countries
- Disaggregate data by all available demographic categories to avoid masking disparities
- Translate findings into actionable policy recommendations with implementation considerations
- Factor in COVID-19 pandemic effects on data collection, trends, and health system capacity

## Tags
public-health, epidemiology, health-disparities, surveillance, biostatistics, SDOH, health-equity, program-evaluation, policy-analysis, CBPR, population-health
