# Task: Query Optimizer (Engineering E4)

**Status:** not started  
**Track:** engineering — Part 4  
**Prerequisite:** e3_transactions_and_isolation  
**Registry:** L15–L16, Ch 16

## Goal

Understand the cost-based optimizer — why the database doesn't execute SQL in the order you wrote it, and why having an index doesn't guarantee it gets used.

## Must watch

- [ ] Lecture #15 — Query Optimization I
- [ ] Lecture #16 — Query Optimization II

## Must read

- [ ] Textbook Ch 16.1–16.4 (optimizer, statistics, cost-based plans)

## Must understand

- Cost-based optimizer chooses physical plan by estimated cost — not your SQL text order
- Statistics: row counts, distinct values (NDV), histograms → plan choice
- Why `ANALYZE` matters after bulk load, migration, or major data change
- **Index exists ≠ index used** — optimizer may prefer seq scan if it estimates fewer pages
- Bad row estimates → wrong join algorithm (e.g., nested loop on huge table)
- Selectivity and cardinality estimation at intuition level

## Hands-on (PostgreSQL)

- [ ] Run `ANALYZE` after bulk load; compare plan before/after
- [ ] Document one query where an index existed but seq scan was chosen — explain why
- [ ] Use `EXPLAIN (ANALYZE, BUFFERS)` to compare estimated vs actual row counts

## Output

- [ ] "SQL tuning playbook" — symptoms → likely optimizer mistake
- [ ] 2 before/after EXPLAIN ANALYZE case studies (plan flip after ANALYZE or index change)

## Skip

- Implementing optimizer rules or cost functions
- Volcano paper (optional skim)

## Notes

<!-- Your notes here -->
