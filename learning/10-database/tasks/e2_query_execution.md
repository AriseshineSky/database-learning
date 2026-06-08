# Task: Query Execution (Engineering E2)

**Status:** not started  
**Track:** engineering — Part 2 (~80% core)  
**Prerequisite:** e1_storage_and_indexes  
**Registry:** L11–L13, Ch 15

## Goal

Understand how queries execute — so when you see `EXPLAIN ANALYZE`, you know what the database is doing.

This is the skill most application engineers lack.

## Must watch

- [ ] Lecture #11 — Sorting & Aggregations
- [ ] Lecture #12 — Join Algorithms
- [ ] Lecture #13 — Query Execution I

## Must read

- [ ] Textbook Ch 15.1–15.7 (relational algebra execution, joins, aggregation)

## Must understand

| Operator | Mental model | When it hurts |
|----------|--------------|---------------|
| **Nested Loop Join** | One outer row → scan inner table | Large inner without index on join key |
| **Hash Join** | Build hash table on one side → probe with other | Memory pressure; non-equi joins |
| **Sort-Merge Join** | Sort both inputs → merge | Know it exists; less common in daily tuning |

Also:

- Filter pushdown, projection, predicate selectivity
- Sort and Aggregate nodes in plans
- Seq Scan vs Index Scan vs Bitmap Scan (observe in EXPLAIN)

## Hands-on (PostgreSQL)

- [ ] Same join query: observe NLJ vs Hash Join (`enable_nestloop`, `enable_hashjoin`)
- [ ] Identify Sort, Aggregate, and scan type in 5 different `EXPLAIN ANALYZE` outputs
- [ ] Fix one slow query by adding an index that helps nested loop on the inner side

## Output

- [ ] "EXPLAIN operator cheat sheet" — what each node means
- [ ] 3+ annotated `EXPLAIN ANALYZE` examples in `notes/`
- [ ] Can explain why nested loop on a large unindexed table is catastrophic

## Skip

- BusTub P3 executor implementation
- Volcano paper (optional — iterator model intuition only)
- Optimizer / statistics (E4)

## Notes

<!-- Your notes here -->
