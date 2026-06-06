# Task: Storage & Indexes (Engineering)

**Status:** not started  
**Track:** engineering  
**Registry:** L03–L08, L10 (conceptual), Ch 12–14, B02

## Goal

Understand how data is stored and indexed well enough to design schemas and indexes in production — without implementing a buffer pool or B+ tree.

## Must watch (CMU Fall 2025)

- [ ] Lecture #03 — Database Storage I (pages, slotted pages — **conceptual**)
- [ ] Lecture #04 — Memory Management (buffer pool **behavior**, skip implementation)
- [ ] Lecture #08 — Indexes & Filters I
- [ ] Lecture #10 — Index Concurrency Control (**skim** — latch idea only)

## Must read

- [ ] Textbook Ch 12 (storage structure — overview)
- [ ] Textbook Ch 13.1–13.2 (disk vs memory — skip replacement policy math)
- [ ] Textbook Ch 14.1–14.5 (B+ tree, hash indexes, composite indexes)

## Must understand

- Page / heap file / slotted page (conceptual)
- Why B+ trees suit range scans and ordered access
- Composite index column order and left-prefix rule
- Covering index vs index-only scan
- When the optimizer picks seq scan vs index scan
- Index bloat / maintenance at ops level (VACUUM, REINDEX — Postgres)

## Hands-on (PostgreSQL)

- [ ] Run `EXPLAIN (ANALYZE, BUFFERS)` on a range query with and without an index
- [ ] Create a composite index; verify plan change with different `WHERE` / `ORDER BY`
- [ ] Document one case where an index was **not** used and why

## Optional

- [ ] [PostgreSQL buffer manager blog](../blogs/pg-buffer.md) — behavior only
- [ ] Lecture #07 — Hash Tables (contrast with B+ tree)

## Output

- [ ] Notes: "Index design checklist" for your own projects
- [ ] 3+ EXPLAIN examples saved in `notes/`
- [ ] Can explain why `ORDER BY` on unindexed column is expensive

## Skip

- BusTub P1 (buffer pool implementation)
- BusTub P2 (B+ tree implementation)
- LRU / Clock replacement implementation details

## Notes

<!-- Your notes here -->
