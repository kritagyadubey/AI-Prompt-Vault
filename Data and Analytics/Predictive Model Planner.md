# Predictive Model Planner
> Transforms prediction requirements into comprehensive ML project plans with data requirements, feature engineering strategies, model selection frameworks, and deployment blueprints.

## Purpose
Convert requests like "predict customer churn" into complete ML project specifications that define the prediction problem precisely, specify data requirements, feature engineering approaches, model selection criteria, validation strategies, and deployment patterns.

## Best For
- Planning machine learning projects end-to-end
- Designing predictive analytics solutions
- Creating ML project proposals and charters
- Structuring data science workstreams

## Prompt Enhancer
```text
You are a senior data science project manager. Transform the following prediction requirement into a comprehensive ML project plan.

INPUT REQUIREMENT:
{user_request}

OUTPUT A COMPLETE ML PROJECT PLAN INCLUDING:

1. PROBLEM DEFINITION
   - Business problem statement
   - Prediction target variable (exact definition)
   - Prediction horizon (when to predict, how far ahead)
   - Prediction unit (user, account, transaction, item)
   - Business value quantification
   - Success criteria (technical and business)
   - Constraints (latency, interpretability, fairness)

2. DATA REQUIREMENTS
   a) REQUIRED DATA SOURCES
      For each source:
      - Table/entity name
      - Key fields needed
      - Time window requirements
      - Expected volume and freshness
      - Access method and permissions
   
   b) DATA SUFFICIENCY ASSESSMENT
      - Historical data availability (minimum 2-3 cycles)
      - Label availability and quality
      - Feature completeness assessment
      - Data gaps and mitigation strategies
   
   c) DATA COLLECTION PLAN
      - New data sources needed
      - Feature store requirements
      - Real-time vs. batch feature serving
      - Data enrichment opportunities

3. FEATURE ENGINEERING STRATEGY
   For each feature category:
   
   a) BEHAVIORAL FEATURES
      - Aggregation windows (7d, 30d, 90d, lifetime)
      - Trend features (slope, acceleration)
      - Recency features
      - Frequency features
      - Intensity features
   
   b) CONTEXTUAL FEATURES
      - Time-based features (day of week, hour, season)
      - Device/platform features
      - Geographic features
      - Session-level features
   
   c) RELATIONAL FEATURES
      - Social network features
      - Household/account features
      - Segment-level aggregations
   
   d) EXTERNAL FEATURES
      - Market data
      - Weather data
      - Economic indicators
      - Third-party enrichment
   
   Feature engineering pipeline:
   - Feature definitions and SQL/Python code
   - Feature validation and monitoring
   - Feature importance estimation
   - Feature selection methodology

4. MODEL SELECTION FRAMEWORK
   Evaluation criteria:
   - Predictive performance (AUC, RMSE, F1)
   - Interpretability requirements
   - Training time constraints
   - Inference latency requirements
   - Maintenance complexity
   
   Candidate models:
   a) BASELINE MODELS
      - Simple heuristics
      - Rule-based systems
      - Linear/logistic regression
   
   b) TREE-BASED MODELS
      - Random Forest
      - XGBoost/LightGBM/CatBoost
      - Decision tree interpretation
   
   c) NEURAL NETWORK MODELS
      - Feed-forward networks
      - Sequence models (if temporal)
      - Embedding approaches
   
   d) ENSEMBLE APPROACHES
      - Stacking
      - Blending
      - Model selection strategy

5. TRAINING AND VALIDATION STRATEGY
   a) DATA SPLITTING
      - Time-based splitting (train/validation/test by time)
      - User-level splitting (no data leakage)
      - Cross-validation strategy (temporal, spatial)
   
   b) LABEL DEFINITION
      - Label construction logic
      - Positive/negative class definition
      - Label window and observation window
      - Handling class imbalance (SMOTE, undersampling, class weights)
   
   c) EVALUATION METRICS
      - Primary metric (aligned with business objective)
      - Secondary metrics (for model selection)
      - Fairness metrics (equal opportunity, demographic parity)
      - Calibration metrics (reliability diagram)
   
   d) VALIDATION CHECKS
      - Overfitting detection
      - Temporal stability checks
      - Segment-level performance
      - A/B test validation plan

6. DEPLOYMENT ARCHITECTURE
   a) SERVING PATTERN
      - Real-time inference (API endpoint)
      - Batch scoring (scheduled pipeline)
      - Hybrid (near real-time with caching)
   
   b) INFRASTRUCTURE
      - Model serving framework (Seldon, BentoML, SageMaker)
      - Container strategy
      - Auto-scaling configuration
      - Latency requirements and SLAs
   
   c) FEATURE SERVING
      - Feature store integration
      - Real-time feature computation
      - Feature freshness requirements
      - Fallback for missing features

7. MONITORING AND MAINTENANCE
   a) MODEL MONITORING
      - Prediction distribution monitoring
      - Feature drift detection
      - Model performance decay detection
      - Data quality monitoring
   
   b) OPERATIONAL MONITORING
      - Latency monitoring
      - Throughput monitoring
      - Error rate monitoring
      - Cost monitoring
   
   c) RETRAINING TRIGGERS
      - Performance degradation thresholds
      - Data drift thresholds
      - Scheduled retraining cadence
      - A/B test for model updates

8. FAIRNESS AND ETHICS
   - Protected attributes identification
   - Fairness metrics and thresholds
   - Bias detection methodology
   - Mitigation strategies
   - Explainability requirements (SHAP, LIME)
   - Audit trail requirements

9. PROJECT TIMELINE
   Week 1-2: Problem framing and data audit
   Week 3-4: Data collection and feature engineering
   Week 5-6: Model development and iteration
   Week 7: Validation and testing
   Week 8: Deployment and monitoring setup
   Week 9-10: A/B test and iteration

10. RESOURCE REQUIREMENTS
    - Data science team composition
    - Compute requirements (training and inference)
    - Storage requirements
    - Tooling and infrastructure costs
    - Ongoing maintenance costs

11. RISK ASSESSMENT
    - Technical risks (data quality, model complexity)
    - Business risks (adoption, false positives)
    - Operational risks (latency, cost)
    - Mitigation strategies

12. SUCCESS METRICS
    - Model performance metrics
    - Business impact metrics
    - Operational metrics
    - Adoption metrics

Format the output as a structured project plan with technical specifications, code snippets for key components, and a Gantt-style timeline.
```

## Example
### Original Prompt
```text
We want to predict which customers are going to churn so we can reach out to them.
```

### Enhanced Prompt
```text
You are a senior data science project manager. Transform the following prediction requirement into a comprehensive ML project plan.

INPUT REQUIREMENT:
Predict customer churn 30 days in advance so we can target retention campaigns. We have 500K active customers with 18 months of behavioral data.

OUTPUT A COMPLETE ML PROJECT PLAN INCLUDING:

1. PROBLEM DEFINITION
2. DATA REQUIREMENTS
3. FEATURE ENGINEERING STRATEGY
4. MODEL SELECTION FRAMEWORK
5. TRAINING AND VALIDATION STRATEGY
6. DEPLOYMENT ARCHITECTURE
7. MONITORING AND MAINTENANCE
8. FAIRNESS AND ETHICS
9. PROJECT TIMELINE
10. RESOURCE REQUIREMENTS
11. RISK ASSESSMENT
12. SUCCESS METRICS

Format the output as a structured project plan with technical specifications, code snippets for key components, and a Gantt-style timeline.
```

## Notes
- Specify the prediction horizon (how far ahead to predict)
- Include data volume and historical depth available
- Note any constraints on model interpretability
- Mention regulatory requirements for model explainability

## Tags
machine-learning, predictive-analytics, churn-prediction, feature-engineering, model-deployment, data-science, mlops, classification, regression
