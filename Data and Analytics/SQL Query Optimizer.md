# SQL Query Optimizer
> Transforms slow or basic SQL queries into optimized, well-documented queries with execution plan analysis, indexing recommendations, and rewrite strategies.

## Purpose
Convert simple or poorly-performing SQL queries into production-optimized versions with detailed explanations of each optimization technique applied, including index recommendations, rewrite strategies, and cost-based reasoning.

## Best For
- Optimizing slow-running queries on large datasets
- Rewriting suboptimal SQL patterns (correlated subqueries, IN clauses)
- Designing indexes for query workload patterns
- Creating query performance documentation

## Prompt Enhancer
```text
You are a senior database performance engineer specializing in SQL optimization across multiple database engines. Transform the following SQL query into an optimized version with detailed performance analysis.

INPUT QUERY:
Database Engine: {database_engine}
Table Sizes: {table_sizes}
Current Execution Time: {current_time}
{original_query}

OUTPUT FORMAT:

1. QUERY ANALYSIS
   - Identify the query's logical purpose in plain English
   - Current execution plan summary (scan types, join methods, sort operations)
   - Estimated vs. actual row counts for each operation
   - Bottleneck identification (which step consumes most time/memory)
   - Cost estimation breakdown

2. OPTIMIZATION STRATEGIES APPLIED
   For each optimization, explain:
   - What was changed and why
   - Expected performance impact (percentage improvement)
   - Trade-offs introduced (storage, write performance, complexity)

   Specific optimizations to evaluate:
   a) JOIN REORDERING
      - Optimal join order based on table sizes and selectivity
      - Join algorithm selection (nested loop, hash, merge)
      - Filter pushdown opportunities

   b) SUBQUERY ELIMINATION
      - Convert correlated subqueries to JOINs
      - Rewrite IN subqueries as EXISTS or JOINs
      - Lateral join opportunities where applicable

   c) WINDOW FUNCTION OPTIMIZATION
      - Replace self-joins with window functions
      - Optimize PARTITION BY and ORDER BY clauses
      - Frame clause optimization (ROWS vs RANGE)

   d) AGGREGATION OPTIMIZATION
      - Pre-aggregation or materialized view candidates
      - GROUP BY ordering for index utilization
      - HAVING vs. WHERE filter placement

   e) INDEX RECOMMENDATIONS
      - Composite index design (column order, included columns)
      - Covering index opportunities
      - Partial/wfiltered indexes for selective queries
      - Index scan vs. seek analysis
      - Statistics update recommendations

   f) PREDICATE OPTIMIZATION
      - SARGable predicate rewrites
      - Function-on-column elimination
      - OR-to-UNION conversion when beneficial
      - NULL handling optimization

   g) SORT AND LIMIT OPTIMIZATION
      - Top-N sort optimization
      - DISTINCT elimination via GROUP BY
      - ORDER BY with LIMIT using index

3. OPTIMIZED QUERY
   Provide the fully rewritten query with:
   - Inline comments explaining each optimization
   - CTE usage for readability where appropriate
   - Consistent formatting and aliasing
   - Execution hints if database-specific (USE INDEX, NOLOCK, etc.)

4. INDEX DDL
   Provide CREATE INDEX statements for recommended indexes with:
   - Column order rationale
   - INCLUDE columns for covering indexes
   - WHERE clause for partial indexes
   - Expected storage overhead estimate
   - Impact on INSERT/UPDATE/DELETE performance

5. ALTERNATIVE APPROACHES
   For complex queries, provide:
   - Materialized view definition if pre-aggregation is beneficial
   - Denormalized table design if joins are the bottleneck
   - Partitioning strategy if data volume is the issue
   - Query splitting for parallel execution

6. PERFORMANCE VALIDATION
   - EXPLAIN/EXPLAIN ANALYZE command to run
   - Expected execution plan changes
   - Benchmarking methodology (run 3x, median result)
   - Key metrics to monitor post-optimization

7. RISK ASSESSMENT
   - Query behavior change risks (different results edge cases)
   - Index maintenance overhead
   - Optimizer hint dependencies across versions
   - Regression testing recommendations

Format the output with the original and optimized queries in SQL code blocks, optimization explanations in numbered sections, and a summary table of expected improvements.
```

## Example
### Original Prompt
```text
This query is slow: SELECT * FROM orders o JOIN customers c ON o.customer_id = c.id WHERE o.year = 2024 AND c.country = 'US'
```

### Enhanced Prompt
```text
You are a senior database performance engineer specializing in SQL optimization across multiple database engines. Transform the following SQL query into an optimized version with detailed performance analysis.

INPUT QUERY:
Database Engine: PostgreSQL 15
Table Sizes: orders (500M rows), customers (10M rows)
Current Execution Time: 45 seconds
SELECT * FROM orders o JOIN customers c ON o.customer_id = c.id WHERE o.year = 2024 AND c.country = 'US'

OUTPUT FORMAT:

1. QUERY ANALYSIS
   - Identify the query's logical purpose in plain English
   - Current execution plan summary (scan types, join methods, sort operations)
   - Estimated vs. actual row counts for each operation
   - Bottleneck identification (which step consumes most time/memory)
   - Cost estimation breakdown

2. OPTIMIZATION STRATEGIES APPLIED
   For each optimization, explain:
   - What was changed and why
   - Expected performance impact (percentage improvement)
   - Trade-offs introduced (storage, write performance, complexity)

   Specific optimizations to evaluate:
   a) JOIN REORDERING
   b) SUBQUERY ELIMINATION
   c) WINDOW FUNCTION OPTIMIZATION
   d) AGGREGATION OPTIMIZATION
   e) INDEX RECOMMENDATIONS
   f) PREDICATE OPTIMIZATION
   g) SORT AND LIMIT OPTIMIZATION

3. OPTIMIZED QUERY
4. INDEX DDL
5. ALTERNATIVE APPROACHES
6. PERFORMANCE VALIDATION
7. RISK ASSESSMENT

Format the output with the original and optimized queries in SQL code blocks, optimization explanations in numbered sections, and a summary table of expected improvements.
```

## Notes
- Always specify the database engine (PostgreSQL, MySQL, SQL Server, Oracle, BigQuery, Snowflake, etc.)
- Include table row counts for accurate cost estimation
- Mention any indexes that already exist
- Note any query result constraints (must return exact same rows)

## Tags
sql, query-optimization, performance, indexing, database, postgresql, mysql, sql-server, execution-plan, tuning
