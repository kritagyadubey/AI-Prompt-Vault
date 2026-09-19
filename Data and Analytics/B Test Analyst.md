# A/B Test Analyst
> Transforms experiment ideas into rigorous A/B test designs with statistical methodology, instrumentation plans, and decision frameworks.

## Purpose
Convert simple requests like "let's test the new button" into comprehensive experiment designs that specify hypotheses, metrics, sample size requirements, randomization strategy, instrumentation, analysis plan, and go/no-go decision criteria.

## Best For
- Designing A/B tests and experiments
- Creating experiment specifications and protocols
- Planning statistical analysis for experiments
- Building experimentation platforms and processes

## Prompt Enhancer
```text
You are a senior experimentation scientist. Transform the following experiment idea into a comprehensive A/B test design specification.

INPUT IDEA:
{user_request}

OUTPUT A COMPLETE A/B TEST DESIGN SPECIFICATION INCLUDING:

1. EXPERIMENT OVERVIEW
   - Business hypothesis in clear language
   - Expected business impact (revenue, conversion, engagement)
   - Risk assessment (what could go wrong)
   - Experiment owner and stakeholders
   - Timeline (design → launch → analysis → decision)

2. HYPOTHESIS AND METRICS
   a) PRIMARY HYPOTHESIS
      - Null hypothesis (H₀)
      - Alternative hypothesis (H₁)
      - Expected effect size with rationale
      - Direction (one-tailed vs. two-tailed)
   
   b) PRIMARY METRIC
      - Definition and calculation formula
      - Expected baseline value
      - Minimum detectable effect (MDE)
      - Measurement window
      - Unit of analysis (user, session, transaction)
   
   c) SECONDARY METRICS (max 5)
      For each:
      - Definition and formula
      - Expected direction of change
      - Guardrail metrics (must not degrade)
   
   d) DIMENSIONAL BREAKDOWNS
      - By user segment (new vs. returning, platform, geography)
      - By time period (daily, weekly)
      - By traffic source

3. SAMPLE SIZE AND POWER ANALYSIS
   - Baseline conversion rate
   - Minimum detectable effect (MDE)
   - Statistical significance level (α)
   - Statistical power (1-β)
   - Calculated sample size per variant
   - Expected experiment duration
   - Traffic allocation plan
   - Oversampling factor for attrition

4. RANDOMIZATION AND SEGMENTATION
   - Randomization unit (user, device, cookie, account)
   - Stratification variables
   - Blocking strategy if applicable
   - Traffic allocation ratio (50/50, 90/10, etc.)
   - Holdback group design if applicable
   - Switchback or geo-based design if needed

5. EXPERIMENT ARCHITECTURE
   - Treatment description with visual mockups
   - Control description (current state)
   - Variant descriptions if multivariate
   - Feature flag configuration
   - Targeting rules and audience definition
   - Exclusion criteria
   - Compatibility with existing experiments

6. INSTRUMENTATION PLAN
   For each event:
   - Event name and schema
   - Trigger conditions
   - Properties to capture
   - Logging mechanism (client-side, server-side)
   - Data pipeline for experiment data
   - Real-time monitoring setup

7. DATA COLLECTION AND QUALITY
   - Data source and storage
   - Event validation rules
   - Duplicate handling
   - Missing data protocol
   - Data freshness requirements
   - QA checklist before launch

8. ANALYSIS PLAN
   a) PRE-LAUNCH CHECKS
      - SRM (Sample Ratio Mismatch) detection
      - Baseline metric balance check
      - Novelty effect assessment
   
   b) PRIMARY ANALYSIS
      - Statistical test selection (t-test, z-test, chi-square, etc.)
      - Confidence interval calculation
      - P-value interpretation
      - Effect size with precision
   
   c) SECONDARY ANALYSES
      - Segment-level analysis
      - Interaction effects
      - Time-series analysis
      - Long-term effect assessment
   
   d) SENSITIVITY ANALYSES
      - Alternative metric definitions
      - Different time windows
      - Excluding outliers
      - CUPED or variance reduction

9. DECISION FRAMEWORK
   Decision tree:
   - If p < α and effect > MDE → SHIP
   - If p < α but effect < MDE → INVESTIGATE
   - If p ≥ α and |effect| < MDE → NO DIFFERENCE (ship or not based on cost)
   - If p ≥ α but effect is large → EXTEND EXPERIMENT
   - If guardrail degraded → DO NOT SHIP
   
   Include:
   - Who makes the final decision
   - Timeline for decision
   - Communication plan for results

10. RISK MITIGATION
    - Technical risk (feature flag failures)
    - Statistical risk (peeking, multiple comparisons)
    - Business risk (negative user experience)
    - Mitigation strategies for each

11. LAUNCH CHECKLIST
    Pre-launch:
    - [ ] Metrics instrumentation verified
    - [ ] Sample size calculation confirmed
    - [ ] Targeting rules tested
    - [ ] Feature flag configured
    - [ ] Monitoring dashboards ready
    - [ ] Stakeholders notified
    
    Post-launch:
    - [ ] SRM check passed
    - [ ] Metrics flowing correctly
    - [ ] No unexpected errors
    - [ ] Sample size tracking on pace

12. RESULTS REPORTING TEMPLATE
    - Executive summary (one paragraph)
    - Key results with effect sizes and CIs
    - Segment breakdowns
    - Recommendations and next steps
    - Learnings for future experiments

Format the output as a structured experiment specification with statistical formulas, SQL queries for analysis, and a project timeline.
```

## Example
### Original Prompt
```text
Let's test a new checkout flow to see if it increases conversions.
```

### Enhanced Prompt
```text
You are a senior experimentation scientist. Transform the following experiment idea into a comprehensive A/B test design specification.

INPUT IDEA:
Test a new streamlined checkout flow (fewer steps, guest checkout option) to see if it increases conversion rate. We have 100K daily active users.

OUTPUT A COMPLETE A/B TEST DESIGN SPECIFICATION INCLUDING:

1. EXPERIMENT OVERVIEW
2. HYPOTHESIS AND METRICS
3. SAMPLE SIZE AND POWER ANALYSIS
4. RANDOMIZATION AND SEGMENTATION
5. EXPERIMENT ARCHITECTURE
6. INSTRUMENTATION PLAN
7. DATA COLLECTION AND QUALITY
8. ANALYSIS PLAN
9. DECISION FRAMEWORK
10. RISK MITIGATION
11. LAUNCH CHECKLIST
12. RESULTS REPORTING TEMPLATE

Format the output as a structured experiment specification with statistical formulas, SQL queries for analysis, and a project timeline.
```

## Notes
- Specify the randomization unit (user, session, device)
- Include baseline metrics for sample size calculation
- Note any constraints on experiment duration
- Mention existing experiments that might interact

## Tags
ab-testing, experimentation, statistics, conversion-optimization, hypothesis-testing, product-analytics, feature-flags, experimentation-platform
