# Risk Assessment
> Transforms business uncertainty into structured risk registers with probability-impact analysis and actionable mitigation strategies.

## Purpose
This enhancer takes a business initiative, project, or strategic decision and transforms it into a comprehensive risk assessment. It systematically identifies, analyzes, evaluates, and prioritizes risks across multiple dimensions (strategic, operational, financial, compliance, reputational), then designs mitigation and contingency strategies. It moves beyond generic risk lists to produce an actionable risk management framework.

## Best For
- Project managers conducting pre-launch risk assessments
- Executives evaluating strategic decisions with significant downside
- Startups assessing risks before major investments or pivots
- Operations teams evaluating supply chain, vendor, or process risks
- Compliance teams assessing regulatory and legal exposure
- Any leader who needs to understand what could go wrong and how to prepare

## Prompt Enhancer
```text
Act as a risk management specialist with experience across strategic, operational, financial, and compliance risk domains. Use web search to research industry-specific risks, recent risk events in the user's sector, regulatory changes, and risk management best practices. Transform the business initiative or decision into a comprehensive risk assessment with actionable mitigation strategies.

Work through these sections systematically:

1. RISK CONTEXT AND SCOPE
   - What is the initiative, project, or decision being assessed?
   - Strategic objectives at stake: what success looks like and what failure costs
   - Risk appetite: how much risk is acceptable? Conservative, moderate, or aggressive?
   - Time horizon: short-term (0-6 months), medium-term (6-18 months), or long-term (18+ months)?
   - Assumptions that, if wrong, would fundamentally change the risk profile

2. RISK IDENTIFICATION
   Systematically identify risks across these categories:
   - STRATEGIC RISKS: market shifts, competitive moves, customer behavior changes, technology disruption, business model viability
   - OPERATIONAL RISKS: process failures, technology outages, supply chain disruptions, talent gaps, quality issues
   - FINANCIAL RISKS: cash flow, currency, interest rates, credit, funding availability, cost overruns
   - COMPLIANCE AND LEGAL RISKS: regulatory changes, litigation, contract disputes, data privacy, intellectual property
   - REPUTATIONAL RISKS: brand damage, customer trust, media exposure, social media, ethical concerns
   - EXTERNAL RISKS: economic conditions, geopolitical events, natural disasters, pandemics, industry disruptions
   
   For each risk, provide: risk description, risk owner, category, and potential triggers.

3. RISK ANALYSIS
   For each identified risk, assess:
   - Probability: likelihood of occurrence (1-5 scale: 1=rare, 5=almost certain)
   - Impact: severity if it occurs (1-5 scale: 1=negligible, 5=catastrophic)
   - Velocity: how quickly would the impact be felt? (immediate, days, weeks, months)
   - Detectability: how early can it be detected? (early warning, during, after)
   - Interconnectedness: does this risk trigger or amplify other risks?
   - Time sensitivity: is there a window after which the risk becomes irrelevant or escalates?
   
   Calculate risk score: Probability × Impact = Risk Score (1-25 scale)

4. RISK PRIORITIZATION
   - Risk heat map: categorize all risks into Critical (score 15-25), High (10-14), Medium (5-9), Low (1-4)
   - Critical risks: top 5 risks requiring immediate executive attention
   - Emerging risks: risks with low current probability but high potential impact that could escalate
   - Compound risks: scenarios where multiple risks materialize simultaneously
   - Risk interdependencies: how risks relate to and amplify each other

5. MITIGATION STRATEGIES
   For each Critical and High risk, design a specific mitigation plan:
   - AVOID: eliminate the risk by changing plans (what would you need to change?)
   - MITIGATE: reduce probability or impact (specific actions, resources, timeline)
   - TRANSFER: shift risk to a third party (insurance, outsourcing, contracts, hedging)
   - ACCEPT: acknowledge and prepare contingency (only for low-impact risks after mitigation attempts)
   
   For each mitigation, specify: action steps, responsible owner, required resources, timeline, success criteria, and cost of mitigation vs. cost of risk.

6. CONTINGENCY PLANS
   For the top 5 Critical risks, develop detailed contingency plans:
   - Trigger criteria: what specific conditions activate the contingency?
   - Response actions: step-by-step what happens when the risk materializes
   - Communication plan: who needs to know, when, through what channel
   - Resource requirements: what needs to be pre-positioned or quickly available
   - Recovery timeline: estimated time to return to normal operations
   - Lessons learned integration: how to update the risk assessment after an event

7. MONITORING AND EARLY WARNING SYSTEM
   - Key risk indicators (KRIs) for each Critical and High risk
   - Monitoring frequency: daily, weekly, monthly, quarterly by risk type
   - Data sources: what information feeds the monitoring?
   - Escalation thresholds: when does a KRI trigger action?
   - Risk dashboard design: what should leadership see?
   - Review cadence: when to formally reassess the risk register

8. RISK GOVERNANCE
   - Risk owner assignments for each Critical and High risk
   - Risk committee or review board composition and meeting cadence
   - Decision rights: who can accept, mitigate, or escalate each risk?
   - Reporting structure: how risks are communicated to leadership and board
   - Risk culture: how to embed risk awareness in daily operations
   - Documentation requirements: what records to maintain for audit and learning

9. SCENARIO ANALYSIS
   For the 3 most impactful risks, model specific scenarios:
   - Best case: risk is avoided or mitigated successfully
   - Base case: risk materializes at expected probability and impact
   - Worst case: risk materializes with compounded impacts
   - Black swan: extreme but possible scenario
   - For each scenario: financial impact, timeline impact, reputational impact, and response strategy

Present the output as a structured risk assessment report with a clear executive summary, risk register table, heat map visualization description, and prioritized action plan. Include a risk assessment template that can be updated as conditions change.
```

## Example
### Original Prompt
```text
Assess the risks of launching our new e-commerce platform next quarter.
```

### Enhanced Prompt
```text
Act as a risk management specialist. Use web search to research e-commerce launch risks, common platform migration failures, payment processing risks, cybersecurity threats to e-commerce, regulatory requirements (PCI-DSS, GDPR, CCPA), and recent e-commerce outage or breach case studies. Assess the risks of launching a new e-commerce platform next quarter.

1. RISK CONTEXT AND SCOPE
   - What is being launched: platform type, features, expected traffic, transaction volume
   - Business impact of a successful launch vs. a failed launch
   - Risk appetite: is this a mission-critical launch with zero tolerance for downtime, or a phased rollout with acceptable learning?

[Continue through all 9 sections with e-commerce-specific risks including payment processing, inventory management, security, performance, SEO migration, customer data, and regulatory compliance.]
```

## Notes
- Web search helps identify industry-specific risks and recent risk events that might not be in training data
- The enhancer prevents the common mistake of listing risks without actionable mitigation
- Risk assessment should be iterative — update as conditions change and new information emerges
- Compound risk scenarios (multiple risks materializing simultaneously) are often more damaging than individual risks
- The cost of mitigation should always be weighed against the expected cost of the risk

## Tags
#risk-assessment #risk-management #business-risk #mitigation #contingency #compliance #strategic-risk #governance #scenario-planning
