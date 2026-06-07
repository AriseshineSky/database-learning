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

---

## Parallel track (after today's DB focus)

OS 副轨 A：[`parallel.md`](./parallel.md) — 本周 O1，看 L01–L02。  
Ruby 副轨 B：[`parallel-ruby.md`](./parallel-ruby.md) — 有余力时 R1 RubyMonk。  
总表：[`master-schedule.md`](../00-roadmap/master-schedule.md)
