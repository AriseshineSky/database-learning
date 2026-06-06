# Task: Query Execution (BusTub P3)

**Status:** not started  
**Prerequisite:** P2  
**Registry:** L11–L13, Ch 15–16, P01 (Volcano)

## Goal

Implement query executors using the Volcano (iterator) model: scan, filter, join, sort, aggregate.

## Must Read

- [ ] [Volcano paper](../../papers/volcano.md) ← **read before coding**
- [ ] [Lecture #11 — Sorting & Aggregations](../../lectures/l11-sorting.md)
- [ ] [Lecture #12 — Joins](../../lectures/l12-joins.md)
- [ ] [Lecture #13 — Query Execution I](../../lectures/l13-query-execution.md)
- [ ] Textbook Ch 15.1–15.7
- [ ] BusTub P3 project handout

## Must Understand

- Iterator model: `Init()` → `Next()` → `GetOutput()`
- Physical operators: SeqScan, IndexScan, NestedLoopJoin, HashJoin, Sort, Aggregation
- Tuple / RID / child operator pipeline

## Optional

- [ ] Textbook Ch 16 (query optimization — study only)
- [ ] CMU Lectures #15–#16 (optimizer)

## Output

- [ ] All executor operators implemented
- [ ] P3 tests pass
- [ ] Volcano paper status → `understanding`

## Notes

<!-- Your notes here -->
