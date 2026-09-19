# Dashboard Creator
> Transforms basic reporting requests into complete dashboard specifications with layout design, visual encoding choices, interactive elements, and performance optimization strategies.

## Purpose
Convert simple requests like "make a sales dashboard" into detailed dashboard design documents that specify every visualization, its data source, interaction pattern, color system, responsive behavior, and performance constraints—eliminating ambiguity before development begins.

## Best For
- Designing executive, operational, or analytical dashboards
- Planning BI tool implementations (Tableau, Power BI, Looker, Metabase)
- Creating dashboard wireframes and specification documents
- Defining KPI hierarchies and metric visualizations

## Prompt Enhancer
```text
You are a senior BI architect and data visualization expert. Transform the following basic reporting request into a comprehensive dashboard design specification.

INPUT REQUEST:
{user_request}

OUTPUT A COMPLETE DASHBOARD SPECIFICATION INCLUDING:

1. DASHBOARD PURPOSE AND AUDIENCE
   - Primary business question this dashboard answers
   - Target audience (C-suite, managers, analysts, customers)
   - Decision-making context (monitor, investigate, report)
   - Expected viewing frequency (real-time, hourly, daily, weekly)
   - Device targets (desktop, tablet, mobile, large screen/TV)

2. KPI HIERARCHY
   - Primary KPIs (top-level metrics, max 5-7)
   - Secondary KPIs (supporting metrics for drill-down)
   - Tertiary KPIs (diagnostic metrics)
   - Each KPI must include:
     * Definition and formula
     * Data source and freshness
     * Target/benchmark value
     * Trend direction (higher-is-better, lower-is-better, stable-is-better)
     * Red/yellow/green thresholds

3. VISUALIZATION DESIGN PER PANEL
   For each visualization on the dashboard, specify:
   - Panel ID and position (grid coordinates)
   - Visualization type (bar, line, scatter, heatmap, table, KPI card, map, gauge, funnel, sankey, treemap)
   - Specific chart configuration (stacked vs. grouped, horizontal vs. vertical, etc.)
   - Data source query or metric definition
   - X-axis, Y-axis, color encoding, size encoding, tooltip fields
   - Aggregation method (sum, avg, count, distinct, percentile)
   - Time granularity (minute, hour, day, week, month, quarter, year)
   - Comparison overlay (period-over-period, target-vs-actual)
   - Sort order and top-N filtering

4. LAYOUT AND GRID DESIGN
   - Grid system (e.g., 12-column, 24-column)
   - Panel dimensions and aspect ratios
   - Visual hierarchy (most important panels above the fold)
   - White space and breathing room
   - Responsive breakpoints (desktop, tablet, mobile)
   - Collapsible/expandable sections

5. COLOR SYSTEM
   - Primary palette (brand colors if applicable)
   - Sequential palettes (for continuous data)
   - Diverging palettes (for positive/negative or above/below target)
   - Categorical palettes (for discrete groups, max 8-10 colors)
   - Color-blind safe alternatives
   - Semantic colors (success green, warning amber, error red)
   - Dark mode variant if applicable

6. INTERACTION DESIGN
   - Cross-filtering behavior (which panels filter which)
   - Drill-down paths (metric → category → subcategory → detail)
   - Tooltips (content, formatting, sparklines)
   - Date range picker (default range, available ranges, comparison options)
   - Parameter controls (dropdowns, sliders, toggles)
   - Export options (PNG, PDF, CSV, shareable link)
   - Bookmark/snapshot capability

7. DATA LAYER SPECIFICATION
   - Underlying data model (star schema, snowflake, wide table)
   - Required joins and relationships
   - Aggregation tables or materialized views needed
   - Real-time vs. cached data strategy
   - Data freshness requirements per panel
   - Fallback behavior when data is stale

8. PERFORMANCE REQUIREMENTS
   - Maximum acceptable load time (target: <3 seconds)
   - Query optimization strategy (pre-aggregation, indexing, caching)
   - Data volume thresholds and pagination strategy
   - Lazy loading for below-fold panels
   - CDN and caching headers

9. ACCESSIBILITY AND USABILITY
   - WCAG 2.1 AA compliance checklist
   - Screen reader annotations for each panel
   - Keyboard navigation patterns
   - Minimum font sizes and contrast ratios
   - Alt text for each visualization
   - Data table alternative for every chart

10. IMPLEMENTATION PLAN
    - Recommended BI tool and version
    - Data pipeline requirements
    - Estimated development effort (panels × complexity)
    - Testing strategy (UAT, performance, accessibility)
    - Rollout phases (MVP → full feature)

11. SUCCESS METRICS
    - Dashboard adoption targets (DAU/MAU, session duration)
    - Business impact metrics (decisions influenced, time saved)
    - Performance benchmarks (load time, query time)

Format the output as a structured design specification with ASCII wireframe layouts, color hex codes, and SQL snippets for underlying queries.
```

## Example
### Original Prompt
```text
Build me a dashboard showing our marketing performance.
```

### Enhanced Prompt
```text
You are a senior BI architect and data visualization expert. Transform the following basic reporting request into a comprehensive dashboard design specification.

INPUT REQUEST:
Build a dashboard showing marketing performance for the executive team.

OUTPUT A COMPLETE DASHBOARD SPECIFICATION INCLUDING:

1. DASHBOARD PURPOSE AND AUDIENCE
   - Primary business question this dashboard answers
   - Target audience (C-suite, managers, analysts, customers)
   - Decision-making context (monitor, investigate, report)
   - Expected viewing frequency (real-time, hourly, daily, weekly)
   - Device targets (desktop, tablet, mobile, large screen/TV)

2. KPI HIERARCHY
   - Primary KPIs (top-level metrics, max 5-7)
   - Secondary KPIs (supporting metrics for drill-down)
   - Tertiary KPIs (diagnostic metrics)
   - Each KPI must include:
     * Definition and formula
     * Data source and freshness
     * Target/benchmark value
     * Trend direction (higher-is-better, lower-is-better, stable-is-better)
     * Red/yellow/green thresholds

3. VISUALIZATION DESIGN PER PANEL
   For each visualization on the dashboard, specify:
   - Panel ID and position (grid coordinates)
   - Visualization type (bar, line, scatter, heatmap, table, KPI card, map, gauge, funnel, sankey, treemap)
   - Specific chart configuration (stacked vs. grouped, horizontal vs. vertical, etc.)
   - Data source query or metric definition
   - X-axis, Y-axis, color encoding, size encoding, tooltip fields
   - Aggregation method (sum, avg, count, distinct, percentile)
   - Time granularity (minute, hour, day, week, month, quarter, year)
   - Comparison overlay (period-over-period, target-vs-actual)
   - Sort order and top-N filtering

4. LAYOUT AND GRID DESIGN
   - Grid system (e.g., 12-column, 24-column)
   - Panel dimensions and aspect ratios
   - Visual hierarchy (most important panels above the fold)
   - White space and breathing room
   - Responsive breakpoints (desktop, tablet, mobile)
   - Collapsible/expandable sections

5. COLOR SYSTEM
   - Primary palette (brand colors if applicable)
   - Sequential palettes (for continuous data)
   - Diverging palettes (for positive/negative or above/below target)
   - Categorical palettes (for discrete groups, max 8-10 colors)
   - Color-blind safe alternatives
   - Semantic colors (success green, warning amber, error red)
   - Dark mode variant if applicable

6. INTERACTION DESIGN
   - Cross-filtering behavior (which panels filter which)
   - Drill-down paths (metric → category → subcategory → detail)
   - Tooltips (content, formatting, sparklines)
   - Date range picker (default range, available ranges, comparison options)
   - Parameter controls (dropdowns, sliders, toggles)
   - Export options (PNG, PDF, CSV, shareable link)
   - Bookmark/snapshot capability

7. DATA LAYER SPECIFICATION
   - Underlying data model (star schema, snowflake, wide table)
   - Required joins and relationships
   - Aggregation tables or materialized views needed
   - Real-time vs. cached data strategy
   - Data freshness requirements per panel
   - Fallback behavior when data is stale

8. PERFORMANCE REQUIREMENTS
   - Maximum acceptable load time (target: <3 seconds)
   - Query optimization strategy (pre-aggregation, indexing, caching)
   - Data volume thresholds and pagination strategy
   - Lazy loading for below-fold panels
   - CDN and caching headers

9. ACCESSIBILITY AND USABILITY
   - WCAG 2.1 AA compliance checklist
   - Screen reader annotations for each panel
   - Keyboard navigation patterns
   - Minimum font sizes and contrast ratios
   - Alt text for each visualization
   - Data table alternative for every chart

10. IMPLEMENTATION PLAN
    - Recommended BI tool and version
    - Data pipeline requirements
    - Estimated development effort (panels × complexity)
    - Testing strategy (UAT, performance, accessibility)
    - Rollout phases (MVP → full feature)

11. SUCCESS METRICS
    - Dashboard adoption targets (DAU/MAU, session duration)
    - Business impact metrics (decisions influenced, time saved)
    - Performance benchmarks (load time, query time)

Format the output as a structured design specification with ASCII wireframe layouts, color hex codes, and SQL snippets for underlying queries.
```

## Notes
- Specify the BI tool in the original request for tool-specific recommendations
- Include the number of expected end users for capacity planning
- Mention any brand guidelines or existing design systems
- Real-time requirements significantly impact architecture choices

## Tags
dashboard, bi, visualization, tableau, power-bi, looker, kpi, data-visualization, analytics, reporting
