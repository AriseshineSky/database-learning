# Task: B+Tree & Indexes (Engineering E1)

**Status:** in progress  
**Track:** engineering — Part 1 (~40% ROI)  
**Registry:** L07 (skim), L08, Ch 14, B02

## Goal

Understand B+Tree indexing well enough to design production indexes — without implementing page splits or buffer pools.

Most SQL performance problems are index problems.

## Must watch (CMU Fall 2025)

- [ ] Lecture #08 — Indexes & Filters I (**start here**)
- [ ] Lecture #07 — Hash Tables (**skim** — contrast with B+Tree for range queries)

## Must read

- [ ] Textbook Ch 14.1–14.5 (B+Tree, hash indexes, composite indexes)

## Must understand

- Why range queries are fast: `WHERE id BETWEEN 1000 AND 2000`
- Why B+Tree ✓ and Hash ✗ for range scans
- Composite index column order: `INDEX(a, b, c)`
- **Leftmost prefix rule** — `WHERE a = 1` uses the index; `WHERE b = 1` does not
- Covering index vs index-only scan
- Page / Tuple at diagram level (no implementation)
- When the optimizer picks seq scan vs index scan (preview — deep dive in E4)

## Hands-on (PostgreSQL)

- [ ] Run `EXPLAIN (ANALYZE, BUFFERS)` on a range query with and without an index
- [ ] Create a composite index; verify plan change with `WHERE a=…`, `WHERE b=…`, `ORDER BY`
- [ ] Document one case where an index existed but was **not** used

## Output

- [ ] Notes: "Index design checklist" for your own projects
- [ ] 3+ EXPLAIN examples saved in `notes/`
- [ ] Can explain leftmost prefix rule with a concrete example

## Skip

- Lecture #03–#05 (storage layout detail)
- Lecture #04 (buffer pool — Clock, LRU-K, frame tables)
- Lecture #10 (index concurrency / latch crabbing)
- BusTub P1 (buffer pool), P2 (B+Tree implementation)
- Textbook Ch 12–13 (replacement policy math)

## Notes

<!-- Your notes here -->
