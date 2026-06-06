# Task: Query Execution & Optimizer (Engineering)

**Status:** not started  
**Track:** engineering  
**Prerequisite:** e1_storage_and_indexes  
**Registry:** L11–L16, Ch 15–16, P01 (Volcano)

## Goal

Understand how queries execute and how the optimizer chooses plans — so you can write SQL that matches efficient physical operators.

## Must watch

- [ ] Lecture #11 — Sorting & Aggregations
- [ ] Lecture #12 — Join Algorithms
- [ ] Lecture #13 — Query Execution I
- [ ] Lecture #15 — Query Optimization I
- [ ] Lecture #16 — Query Optimization II

## Must read

- [ ] [Volcano paper](../papers/volcano.md) — **conclusions only** (iterator pipeline)
- [ ] Textbook Ch 15.1–15.7 (relational algebra execution, joins, aggregation)
- [ ] Textbook Ch 16.1–16.4 (optimizer, statistics, cost-based plans)

## Must understand

- Iterator / volcano model at diagram level (`Init` → `Next` → output)
- Nested loop join — when it wins (small inner, index on inner)
- Hash join — when it wins (equi-join, large tables, memory)
- Sort-merge join — sorted inputs / large joins
- Filter pushdown, projection, predicate selectivity
- Statistics: row counts, distinct values, histograms → plan choice
- Why bad estimates → nested loop on huge table

## Hands-on (PostgreSQL)

- [ ] Same join query: force or observe NLJ vs hash join (`enable_nestloop`, etc.)
- [ ] Run `ANALYZE` after bulk load; compare plan before/after
- [ ] Fix one "slow query" by rewriting join order or adding index

## Output

- [ ] "SQL tuning playbook" — join type → when to expect it
- [ ] Volcano paper status → `understanding` (not `implemented`)
- [ ] 2 before/after EXPLAIN ANALYZE case studies

## Skip

- BusTub P3 executor implementation
- Implementing physical operators in C++

## Notes

<!-- Your notes here -->
