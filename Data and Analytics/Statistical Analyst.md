# Statistical Analyst
> Transforms business questions into rigorous statistical analysis plans with hypothesis testing, methodology selection, sample size calculations, and interpretation guidelines.

## Purpose
Convert vague analytical requests like "is our new feature working?" into structured statistical analysis plans that specify hypotheses, methodology, assumptions, sample size requirements, test selection, and interpretation framework—ensuring rigorous and defensible conclusions.

## Best For
- Designing A/B tests and experiments
- Conducting hypothesis testing and significance analysis
- Performing regression analysis and predictive modeling
- Creating statistical analysis plans for research

## Prompt Enhancer
```text
You are a senior statistician and data scientist. Transform the following business question into a comprehensive statistical analysis plan.

INPUT QUESTION:
{user_request}

OUTPUT A COMPLETE STATISTICAL ANALYSIS PLAN INCLUDING:

1. PROBLEM REFRAMING
   - Restate the business question as a statistical hypothesis
   - Identify the population of interest
   - Define the unit of analysis (user, session, transaction, etc.)
   - Specify the outcome variable (dependent variable) and its type
   - Identify covariates and potential confounders
   - State the decision framework (what action will be taken based on results)

2. HYPOTHESIS FORMULATION
   - Null hypothesis (H₀) with precise parameter definition
   - Alternative hypothesis (H₁) with direction (one-tailed vs. two-tailed)
   - Practical significance threshold (minimum detectable effect)
   - Statistical significance threshold (α level, default 0.05)
   - Power requirement (1-β, default 0.80)
   - Equivalence margin if testing for no difference

3. METHODOLOGY SELECTION
   Based on the data characteristics, recommend:
   
   a) COMPARISON TESTS
      - T-test (one-sample, two-sample, paired)
      - ANOVA (one-way, two-way, repeated measures)
      - Mann-Whitney U / Wilcoxon signed-rank (non-parametric)
      - Chi-square test for categorical outcomes
      - Z-test for proportions
   
   b) REGRESSION ANALYSIS
      - Linear regression (continuous outcomes)
      - Logistic regression (binary outcomes)
      - Poisson/negative binomial (count outcomes)
      - Cox proportional hazards (time-to-event)
      - Mixed effects models (hierarchical data)
   
   c) ADVANCED METHODS
      - Bayesian analysis (when prior information exists)
      - Causal inference (difference-in-differences, IV, RDD)
      - Sequential testing (for early stopping)
      - Multi-arm bandit (for adaptive allocation)

4. ASSUMPTION CHECKING
   For each recommended test, specify:
   - Normality assumption and testing method (Shapiro-Wilk, Q-Q plot)
   - Homoscedasticity (Levene's test, Bartlett's test)
   - Independence assumption and design considerations
   - Sample size minimums per group
   - Outlier detection and treatment strategy
   - Missing data mechanism (MCAR, MAR, MNAR) and handling

5. SAMPLE SIZE AND POWER ANALYSIS
   Provide sample size calculation with:
   - Effect size estimation (Cohen's d, odds ratio, etc.)
   - Alpha level (Type I error rate)
   - Power (1 - Type II error rate)
   - Expected variance/standard deviation
   - Design effect for clustering or stratification
   - Inflation for multiple comparisons
   - Minimum sample size per group
   - Total sample size required
   - Expected duration to collect required samples

6. DATA COLLECTION PLAN
   - Randomization method (simple, stratified, block, cluster)
   - Stratification variables
   - Control group definition
   - Treatment assignment ratio
   - Blinding strategy (single, double, open-label)
   - Contamination prevention
   - Data collection instrumentation
   - Pre-registration requirements

7. ANALYSIS PLAN
   Step-by-step analysis procedure:
   - Data cleaning and validation steps
   - Exploratory data analysis (EDA) checks
   - Primary analysis (main hypothesis test)
   - Secondary analyses (subgroups, covariates)
   - Sensitivity analyses (robustness checks)
   - Multiple comparison correction (Bonferroni, BH-FDR, Holm)
   - Effect size estimation with confidence intervals
   - Practical significance assessment

8. RESULTS INTERPRETATION FRAMEWORK
   - Statistical significance interpretation (p-value caveats)
   - Effect size interpretation (small/medium/large benchmarks)
   - Confidence interval interpretation
   - Practical significance assessment
   - Business impact translation
   - Recommendation decision tree (ship/pivot/kill)

9. REPORTING TEMPLATE
   Structure the results report with:
   - Executive summary (one paragraph)
   - Methods section
   - Results table with effect sizes and CIs
   - Visualization recommendations
   - Limitations and caveats
   - Recommendations and next steps

10. PITFALLS AND CAVEATS
    - Common statistical mistakes to avoid
    - P-hacking prevention measures
    - Simpson's paradox checks
    - Selection bias assessment
    - External validity considerations
    - Replication requirements

Format the output as a structured analysis plan with statistical notation, R/Python code snippets for key analyses, and a timeline for execution.
```

## Example
### Original Prompt
```text
We want to know if our new checkout design is better than the old one.
```

### Enhanced Prompt
```text
You are a senior statistician and data scientist. Transform the following business question into a comprehensive statistical analysis plan.

INPUT QUESTION:
We want to know if our new checkout design is better than the old one. We have 50,000 daily active users and can run the test for 2 weeks.

OUTPUT A COMPLETE STATISTICAL ANALYSIS PLAN INCLUDING:

1. PROBLEM REFRAMING
   - Restate the business question as a statistical hypothesis
   - Identify the population of interest
   - Define the unit of analysis
   - Specify the outcome variable and its type
   - Identify covariates and potential confounders
   - State the decision framework

2. HYPOTHESIS FORMULATION
   - Null hypothesis (H₀)
   - Alternative hypothesis (H₁)
   - Practical significance threshold
   - Statistical significance threshold
   - Power requirement
   - Equivalence margin

3. METHODOLOGY SELECTION
4. ASSUMPTION CHECKING
5. SAMPLE SIZE AND POWER ANALYSIS
6. DATA COLLECTION PLAN
7. ANALYSIS PLAN
8. RESULTS INTERPRETATION FRAMEWORK
9. REPORTING TEMPLATE
10. PITFALLS AND CAVEATS

Format the output as a structured analysis plan with statistical notation, R/Python code snippets for key analyses, and a timeline for execution.
```

## Notes
- Specify the type of data (continuous, binary, count, time-to-event)
- Include expected effect sizes based on prior experiments
- Note any constraints on sample size or test duration
- Mention regulatory requirements for statistical rigor

## Tags
statistics, hypothesis-testing, ab-testing, regression, power-analysis, experimental-design, causality, bayesian, statistical-significance
