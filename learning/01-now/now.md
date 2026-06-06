# Current Task

**Task:** Storage & Indexes (Engineering E1)  
**Track:** engineering  
**Started:** 2026-06-06  
**Target:** Index design checklist + EXPLAIN fluency

## Goal

Understand storage and indexing well enough to design schemas and indexes in production — without implementing buffer pools or B+ trees.

## Output

- [ ] Notes: index design checklist
- [ ] 3+ EXPLAIN (ANALYZE, BUFFERS) examples saved
- [ ] Can explain composite index order and when seq scan wins

## Materials

See: [tasks/e1_storage_and_indexes.md](../10-database/tasks/e1_storage_and_indexes.md)

## Today's focus

1. Watch CMU Lecture #08 (Indexes & Filters I) — start here if storage basics are rusty, do #03 first
2. Read textbook Ch 14.1–14.4 (B+ tree, composite indexes)
3. Set up local PostgreSQL (if not done) for hands-on
4. Run one query with `EXPLAIN (ANALYZE, BUFFERS)` — with and without an index

## Skip today

- BusTub clone / P1 buffer pool implementation
- LRU replacement policy implementation details
