# Revenue Model Designer
> Transforms product concepts into detailed monetization architectures with pricing strategies, unit economics, and revenue optimization frameworks.

## Purpose
This enhancer takes a product or service concept and transforms it into a comprehensive revenue model with multiple monetization levers, pricing structures, unit economics, and optimization strategies. It forces founders to think through pricing psychology, value metrics, packaging, and the financial mechanics that determine whether a business can sustain itself and scale.

## Best For
- Founders determining how to monetize a new product or service
- Product managers optimizing pricing for existing offerings
- Teams evaluating pricing model changes or introductions of new tiers
- Business analysts building financial models requiring revenue assumptions
- Consultants advising clients on monetization strategy
- SaaS companies evaluating freemium, usage-based, or hybrid pricing

## Prompt Enhancer
```text
Act as a monetization strategist and pricing consultant with deep expertise in SaaS, marketplace, and subscription business models. Use web search to research current pricing benchmarks, industry standards, and examples of successful monetization in the user's specific market. Transform the product concept into a comprehensive revenue model with actionable pricing guidance.

Work through these sections systematically:

1. PRODUCT-MONETIZATION FIT ANALYSIS
   - What value does the product deliver? Quantify the value in terms the customer cares about (time saved, revenue generated, risk reduced, cost avoided)
   - Who pays? End user, buyer, IT department, procurement? Map the buying committee.
   - Willingness to pay assessment: what is the value ceiling and floor?
   - Comparable pricing in the market (web search for competitor pricing pages and pricing data)

2. REVENUE MODEL SELECTION
   - Evaluate and recommend from: subscription, usage-based, freemium, marketplace/commission, licensing, advertising, data monetization, services附加, hybrid
   - For each considered model, provide: pros, cons, fit with product type, expected revenue predictability, and customer acquisition implications
   - Primary model recommendation with rationale
   - Potential secondary revenue streams for diversification

3. PRICING ARCHITECTURE
   - Value metric: what unit best correlates with value delivered (seats, usage, transactions, revenue, storage, API calls)?
   - Tier structure: design 3-4 tiers (Good/Better/Best or custom) with specific features per tier
   - Price points for each tier with justification (cost-plus floor, value-based ceiling, competitive anchors)
   - Price anchoring strategy: which tier is the target, which serves as a decoy?
   - Free tier or trial design: what is free, what triggers upgrade, conversion rate benchmarks
   - Enterprise pricing: how to handle custom pricing, volume discounts, annual commitments

4. UNIT ECONOMICS FRAMEWORK
   - Revenue per customer: ARPU by tier, expansion revenue assumptions
   - Cost of revenue: hosting, support, payment processing, third-party services
   - Gross margin targets by tier and overall
   - Customer Acquisition Cost (CAC) benchmarks for the industry
   - Lifetime Value (LTV) calculation with churn assumptions
   - LTV:CAC ratio targets and payback period
   - Contribution margin per customer by tier

5. PRICING PSYCHOLOGY AND TACTICS
   - Charm pricing vs. round pricing recommendation with rationale
   - anchoring and decoy effects in tier design
   - Price presentation: monthly vs. annual, per-user vs. flat, free vs. freemium
   - Discount strategy: when to discount, how much, who authorizes
   - Price increase strategy: cadence, communication, grandfathering approach
   - Currency and localization considerations for international markets

6. REVENUE OPTIMIZATION STRATEGIES
   - Expansion revenue: upsell paths, cross-sell opportunities, feature gates
   - Retention optimization: how pricing and packaging affect churn
   - Usage-based growth: how to design pricing that grows with customer success
   - Bundling strategy: when to bundle, when to unbundle
   - Promotional strategy: launch pricing, seasonal offers, referral incentives

7. FINANCIAL PROJECTIONS
   - Revenue scenarios: conservative, base, optimistic (with specific assumptions for each)
   - Monthly revenue ramp for first 12 months (assumptions: conversion rate, ARPU, churn)
   - Annual projections for years 2-5
   - Revenue sensitivity analysis: how does revenue change if key variables shift ±20%?
   - Break-even analysis with timeline

8. IMPLEMENTATION ROADMAP
   - Phase 1: launch pricing (what to charge at MVP stage)
   - Phase 2: optimization (when and how to iterate based on data)
   - Phase 3: scale (when to introduce enterprise, annual plans, or new tiers)
   - Key metrics to track: conversion rates by tier, expansion revenue, price elasticity
   - A/B testing plan for pricing experiments
   - Tooling recommendations: billing systems, pricing analytics, experimentation platforms

9. RISKS AND MITIGATIONS
   - Pricing too low: how to detect and correct
   - Pricing too high: signals and recovery strategies
   - Competitor undercutting: response strategies
   - Price sensitivity by segment: how to handle different willingness-to-pay
   - Regulatory or contractual constraints on pricing

Present the output as a structured revenue strategy document with specific numbers, formulas, and actionable recommendations. Include a summary decision matrix at the end that helps the user choose between the top 2-3 pricing options.
```

## Example
### Original Prompt
```text
Help me design a pricing model for my AI writing assistant.
```

### Enhanced Prompt
```text
Act as a monetization strategist. Use web search to research current AI writing tool pricing (Jasper, Copy.ai, Writesonic, Grammarly, Hemingway, Notion AI), typical SaaS pricing tiers for AI tools, usage-based pricing benchmarks for AI API costs, and customer willingness-to-pay data for AI productivity tools. Transform the AI writing assistant concept into a comprehensive revenue model.

1. PRODUCT-MONETIZATION FIT ANALYSIS
   - What specific value does an AI writing assistant deliver? Quantify: time saved per document, quality improvement, output volume increase
   - Who is the buyer: individual creators, marketing teams, enterprise content departments?
   - What are customers currently paying for writing assistance (Grammarly Pro, Jasper, ChatGPT Plus)?
   - What is the cost to serve: API costs per query, infrastructure, support

[Continue through all 9 sections with AI-writing-specific detail, current competitor pricing data from web search, and detailed unit economics calculations.]
```

## Notes
- Web search is essential for pricing data — competitor prices change frequently and training data is unreliable for current pricing
- The enhancer forces founders to articulate the relationship between value delivered and price charged
- Unit economics should be calculated with specific formulas, not just stated as targets
- Encourage users to validate pricing assumptions with real customer willingness-to-pay data (surveys, interviews, A/B tests)
- Pricing is never "set and forget" — the implementation roadmap should include regular review cadences

## Tags
#pricing #revenue-model #monetization #unit-economics #saas #subscription #business-model #financial-planning #pricing-strategy
