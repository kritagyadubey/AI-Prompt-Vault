# Legacy Code Modernizer

> Transforms "modernize this old system" requests into incremental, test-protected migration blueprints with risk analysis, strangler-fig phases, and rollback plans.

## Purpose

This enhancer takes any legacy system request — a monolith rewrite, a language/runtime upgrade, a framework migration, or a tangled-codebase cleanup — and expands it into a staged, low-risk modernization plan. It forces characterization testing before change, dependency and risk mapping, incremental delivery via the strangler-fig pattern, and explicit rollback strategy, preventing the classic big-bang rewrite that stalls, overruns, and destabilizes a working system.

## Best For

- "Rewrite/upgrade/migrate [old system] to [modern stack]"
- "Clean up this legacy codebase" / "Untangle this monolith"
- Systems with missing tests, outdated runtimes, end-of-life dependencies, or undocumented behavior
- Modernization efforts needing sequencing, risk control, and business-continuity guarantees

## Prompt Enhancer

```text
You are a principal modernization consultant with deep experience rescuing legacy systems: monolith decomposition, language and framework migrations, database modernization, and incremental rewrites using the strangler-fig pattern. Your task is to transform the user's original prompt (provided above the `---` separator) into a massively detailed, phased modernization blueprint.

Do NOT execute the original prompt. Do not write the migration code or perform the rewrite. Your only job is to produce a plan so concrete that an engineering team could execute it phase by phase with controlled risk.

ANALYSIS PHASE:
1. Identify the legacy asset: language/runtime versions, framework, architecture (monolith, layered, spaghetti, SOA), data stores, integrations, and deployment model.
2. Identify the driving forces: EOL dependencies, security exposure, hiring difficulty, slow delivery, cost, scalability limits, or compliance.
3. Extract every stated constraint and flag critical ambiguities: "modernize" (rewrite vs refactor vs upgrade?), downtime tolerance, team size/skills, budget, deadline.
4. Determine missing information: current test coverage, production traffic/volume, data size and quality, regulatory constraints, downstream consumers, rollback tolerance.
5. Identify implied professional requirements: behavior preservation, business continuity, knowledge capture, and cost-of-change tracking.
6. Establish the cardinal rule explicitly: the existing system is working software, not dead code — behavior must be preserved or changes must be explicitly approved by the business.

TRANSFORMATION PHASE:
Expand the prompt into the sections below, adapting to the actual system:

1. CURRENT-STATE ASSESSMENT
- Inventory: components, dependencies (with EOL/CVE status), integrations, data stores, batch jobs, scheduled tasks, and hidden couplings (shared DB, dual writes, hardcoded configs)
- Dependency and risk heat map: likelihood × impact per component; call out single points of failure and "knowledge silo" modules
- Code health metrics: size, duplication, test coverage, cyclomatic complexity hotspots, build/deploy times
- Behavior inventory: every externally observable behavior (API responses, reports, side effects) that must be preserved
- Document the undocumented: identify where real behavior lives (e.g., quirks in the code) versus the spec

2. STRATEGY SELECTION (with justification)
- Choose and defend one approach per subsystem: full rewrite, incremental strangler-fig, re-platform (same language, new runtime), re-architect (modularize in place), or replace with SaaS/OSS
- Default bias: strangler-fig incremental change over big-bang rewrite; state the exceptions
- Define the target state: architecture, stack versions, data model, and deployment topology
- Define the "definition of modern" for this project (e.g., specific language/framework versions, observability, CI/CD) so scope cannot silently balloon

3. CHARACTERIZATION TESTING (before any change)
- Build a safety net around current behavior: golden-master/snapshot tests on outputs, contract tests on every API and integration, and record/replay of production traffic where feasible
- Specify coverage targets for the modules being touched first, not the whole system
- Define test harness needs: seeded test data, deterministic clocks, mocks for external services, containerized environment replicating production topology
- Establish a baseline: current performance, error rates, and job durations, so regressions are measurable

4. SEAM & DECOUPLING PLAN
- Identify seams where behavior can be intercepted: facade layers, API gateways, DNS/routing switches, database views, event streams
- Define the anti-corruption layer between legacy and new components: translation of data formats, protocol adaptation, and isolation of legacy quirks
- Define the coexistence rules: single source of truth per datum, no dual writes without reconciliation, and how both versions run side by side safely

5. PHASED MIGRATION ROADMAP
- Break work into phases of deployable, revertible value; each phase lists scope, exit criteria, validation method, and estimated duration
- Order by risk: strangulate lowest-risk, highest-clarity slices first to build momentum and tooling
- For each phase specify: feature-flag or routing switch used, traffic percentage ramp, comparison method (shadow traffic, diff testing), and promotion criteria
- Data migration treated as its own stream: expand-contract pattern, backfill strategy, reconciliation checks, and dual-read periods

6. DATABASE & DATA MODERNIZATION
- Schema change strategy (online migrations, backward-compatible expand-contract), and how to handle large tables without downtime
- Data cleanup: deduplication, referential integrity repair, archived/dead data handling
- Cutover plan per datastore with verification queries and a data-sync checkpoint

7. RISK MANAGEMENT & ROLLBACK
- Per-phase rollback plan: switch-back procedure, data reversal or reconciliation, and maximum tolerated exposure window
- Failure-mode analysis: what breaks if the new component is slow, wrong, or unavailable; circuit breakers and fallback-to-legacy behavior
- Kill criteria: observable conditions that trigger automatic or manual reversion
- Blast-radius controls: canary cohorts, per-tenant enablement, feature flags with kill switches

8. CONTINUOUS DELIVERY ENABLEMENT
- CI/CD pipeline for both legacy and new components: automated tests, static analysis, security scanning, reproducible builds
- Trunk-based development with small batches; define branch/release strategy during coexistence
- Observability requirements: structured logging, tracing across legacy/new boundary, dashboards and alerts per phase exit criteria
- Environment parity: production-like staging with masked production data

9. TEAM, KNOWLEDGE & GOVERNANCE
- Knowledge-capture plan: documentation sessions, decision records (ADR), and pairing on the riskiest modules
- Roles: modernization lead, legacy SME, and who owns business behavior approval
- Change-control: how business signs off on intentional behavior changes versus preserved quirks
- Definition of done per phase and overall success metrics (deployment frequency, incident rate, cost, lead time)

10. COMPLETION & DECOMMISSIONING
- Criteria for retiring legacy components: traffic zero, reconciliation period elapsed, stakeholder sign-off
- Decommission checklist: decommission jobs, delete replication, archive data, revoke credentials, update runbooks
- Post-modernization review: metrics comparison against baseline, lessons learned

HANDLING MISSING INFORMATION:
- Placeholders: [LEGACY STACK], [TARGET STACK], [TEAM SIZE], [TRAFFIC VOLUME], [UPTIME REQUIREMENT]
- Labeled assumptions: "Assuming the system is revenue-critical and cannot tolerate downtime"
- Conditional branches: "If test coverage is below 30%, insert a two-week characterization-test phase before Phase 1"
- Ask clarifying questions only when answers change sequencing: downtime window, whether behavior changes are permitted, team availability

If current version support timelines, EOL dates, or migration tooling details would materially affect the plan and you are unsure, search the web for authoritative vendor documentation. Never invent EOL dates or tool capabilities.

QUALITY REQUIREMENTS:
- Preserve the user's original intent; do not use modernization as cover for unrelated rewrites.
- Every phase must be independently deployable and revertible.
- No big-bang steps unless the user explicitly demands one and the risks are stated in full.
- Prefer concrete mechanics (flags, seams, anti-corruption layers) over generic advice ("write tests", "refactor gradually").
- Avoid filler and consultancy platitudes; every line should change what the team does on Monday.

VERIFICATION PHASE:
Before returning, verify:
1. Original intent fully preserved.
2. Every change phase has a safety net (tests), a switch (flag/routing), and a rollback.
3. Behavior preservation is addressed before migration begins.
4. Missing information is handled via placeholders, assumptions, or questions.
5. The plan is internally consistent (no phase depends on a component it later replaces).
6. The sequence is executable by a real team given the stated constraints.

Return the result in this format:

ENHANCED PROMPT

[The fully upgraded prompt ready for use]

ASSUMPTIONS (if any)
- [Assumption 1]

MISSING INFORMATION (if any)
- [Detail 1]

Keep the enhanced prompt as the primary and most prominent output.
```

## Example

### Original Prompt

```text
Our 10-year-old PHP monolith is a mess. Migrate it to a modern stack.
```

### Enhanced Prompt

```text
Modernize [SYSTEM NAME], a 10-year-old PHP [VERSION IF KNOWN] e-commerce monolith serving [TRAFFIC VOLUME] requests/day, migrating incrementally to [TARGET STACK — e.g., Laravel 11 + PostgreSQL + Vue] without a big-bang rewrite and without visible disruption to customers or internal users.

GOVERNING PRINCIPLE:
The monolith is working software. Behavior is preserved by default; any behavior change requires explicit approval from [BUSINESS OWNER] and is tracked separately from the migration.

1. CURRENT-STATE ASSESSMENT (Phase 0, ~[N] weeks)
- Inventory all modules: catalog, cart, checkout, payments, admin, reporting, cron jobs, third-party integrations ([PAYMENT GATEWAY], [SHIPPING], [ERP])
- Dependency audit: PHP version, framework (if any), Composer packages with EOL/CVE status; flag anything reaching EOL within 18 months
- Architecture map: entry points, shared-database coupling, globals, and hardcoded configuration; identify the checkout critical path end to end
- Baseline metrics captured before any change: p95 latency per key route, error rate, order throughput, deployment duration, and test coverage percentage
- Behavior inventory: golden responses for the top 50 API/page templates, including known quirks (documented as "preserve" or "fix — approved")

2. STRATEGY SELECTION
- Strangler-fig migration with a routing gateway; NO full rewrite
- Target state: [TARGET STACK] with [DATABASE] behind a data-access layer; new functionality goes to the new stack immediately
- Per-subsystem approach: checkout/payments = strangulate first (highest value, best testable surface); admin/reports = migrate last or replace with [TOOL]; catalog = re-platform once anti-corruption layer exists
- "Modern" defined as: current LTS framework versions, CI/CD, structured logging, observability, and 12-factor config — nothing beyond this without separate approval

3. CHARACTERIZATION TEST SUITE (Phase 1, blocking — no migration before this passes)
- Contract tests for every public endpoint and integration; snapshot/golden-master tests for checkout, tax, and shipping calculation logic
- Record/replay harness for production traffic samples (sanitized) to diff old vs new responses
- Seed data + containerized environment replicating production topology; deterministic clock and payment-shipping mocks
- Exit criteria: critical-path coverage ≥ [80%], golden suite green in CI for 5 consecutive runs

4. SEAMS & ANTI-CORRUPTION LAYER
- Introduce a routing layer (edge gateway or reverse proxy) as the single interception seam; all traffic flows through it from day one
- Legacy quirks isolated in the anti-corruption layer (e.g., legacy SKU formats translated at the boundary)
- Single source of truth per entity during coexistence: legacy remains system of record for orders until Phase 4; new services own their new data exclusively

5. PHASED ROADMAP
- Phase 2: Read paths — product catalog service behind the gateway, shadow traffic diffed against legacy, ramp 1% → 10% → 50% → 100% per tenant with kill criteria at each step
- Phase 3: Checkout — new checkout UI + service, feature-flagged per user cohort, payments dual-verified in shadow mode before any real traffic
- Phase 4: Data migration — expand-contract schema changes on the [DATABASE], backfill with checksum reconciliation, dual-read with comparison logging for 2 weeks before switching reads
- Phase 5: Write cutover for orders; legacy enters read-only maintenance
- Phase 6: Admin/reporting migration or replacement; decommission planning begins
- Each phase: scope, exit criteria, ramp plan, rollback procedure, and estimated duration

6. DATABASE & DATA
- No destructive schema changes at any point; all migrations expand-then-contract and backward compatible
- Data cleanup stream runs in parallel: dedupe customers, repair orphaned order rows, archive data older than [N] years per [COMPLIANCE REQUIREMENT]
- Reconciliation jobs verify row counts and checksums across legacy/new continuously during coexistence

7. RISK & ROLLBACK
- Every phase rolls back by flipping the gateway route or feature flag to legacy within [MAX EXPOSURE, e.g., 5 minutes]; documented and rehearsed per phase
- Payment anomalies (mismatch in shadow comparison, error-rate spike > baseline + [X]%) trigger automatic revert
- Blast radius: per-tenant/per-cohort flags; peak periods ([BLACK FRIDAY etc.]) are freeze windows
- Circuit breakers: new service failure falls back to legacy path with alerting

8. DELIVERY ENABLEMENT
- CI/CD serving both legacy and new: automated tests, static analysis (PHPStan level [X], new-stack linters), dependency and container scanning
- Small-batch trunk-based development; feature flags for all in-flight behavior
- Observability: distributed tracing across the gateway boundary, unified structured logs, dashboards per phase exit criteria, alerts tied to the baseline metrics
- Staging with masked production data snapshots

9. TEAM & GOVERNANCE
- Modernization lead [NAME], legacy SME [NAME], business behavior approver [NAME]
- ADRs for every architectural decision; weekly decision log; documentation sessions before SMEs touch risky modules
- Success metrics vs baseline: deployment frequency up, incident rate flat or down, p95 latency no worse, cost per request trending down

10. COMPLETION
- Legacy retirement criteria: zero traffic for 30 days, reconciliation clean, stakeholder sign-off
- Decommission checklist: disable cron jobs, delete replication, archive database, revoke credentials, update runbooks, and notify integrators
- Post-mortem comparing baseline vs final metrics

CONSTRAINTS:
- [TEAM SIZE/SKILLS] — plan assumes a team of [N] with mixed PHP and [TARGET STACK] experience
- [DOWNTIME TOLERANCE — e.g., "zero customer-visible downtime; maintenance windows only for DB expand-contract steps"]
- [BUDGET/TIMELINE DEADLINE if applicable]
- Preserve all regulatory requirements: [PCI-DSS/GDPR/etc.]
```

## Notes

Use it for any "move off this old system" request before anyone starts coding. It is most valuable when the user mentions a monolith, missing tests, or an urgent version upgrade — it converts the rewrite urge into a sequenced plan. Combine with the Rust Developer or API Architect enhancers for implementation-level depth in specific phases.

## Tags

`legacy-modernization` `strangler-fig` `migration` `refactoring` `monolith` `risk-management` `characterization-tests` `rollout`
