# Task: Recovery & PostgreSQL Capstone (Engineering E5)

**Status:** not started  
**Track:** engineering — Part 5 + integration  
**Prerequisite:** e4_query_optimizer  
**Registry:** L21, Ch 19.1–19.4, B03, P06 (LSM-Tree)

## Goal

Close the loop: WAL durability at concept level, then PostgreSQL fluency — EXPLAIN, MVCC, VACUUM, and index design in practice.

## Must watch

- [ ] Lecture #21 — Database Logging (**conceptual** — WAL rule only)

## Must read

- [ ] Textbook Ch 19.1–19.4 (WAL, checkpoint — **concepts only**)
- [ ] [PostgreSQL MVCC blog](../blogs/pg-mvcc.md)
- [ ] [The Log-Structured Merge-Tree](../papers/lsm-tree.md) ← **third required paper**

## Must understand

### Recovery (concepts only)

- WAL rule: **log first, data pages later**
- Why `COMMIT` ≠ durable until WAL is fsync'd
- Checkpoint purpose (shorter recovery time — not a durability shortcut)

### PostgreSQL integration

- How components map: storage → buffer cache → planner → executor → WAL
- MVCC bloat: long transactions block vacuum
- `VACUUM` / autovacuum — why tables grow without it
- Read replica lag at practitioner level

## Hands-on (PostgreSQL capstone)

Complete a full tuning pass on a sample schema:

- [ ] `EXPLAIN ANALYZE` on representative queries — label every operator
- [ ] Design composite indexes for real access patterns; verify with EXPLAIN
- [ ] Two-session isolation demo (write skew or phantom under RR)
- [ ] Inspect `pg_stat_user_tables` for dead tuples; run `VACUUM ANALYZE`
- [ ] Read Postgres docs on `synchronous_commit`, `wal_level` (local dev)

## Output

- [ ] One-page "durability cheat sheet" for your stack
- [ ] PostgreSQL ops checklist: EXPLAIN, MVCC, VACUUM, index review
- [ ] LSM-Tree paper status → `understanding`
- [ ] System design note in `20-architecture/` linking course concepts to your experience

## Skip

- Lecture #22 (ARIES recovery algorithm)
- [ARIES paper](../papers/aries.md)
- ARIES homework-level detail (LSN math, Analysis/Redo/Undo tracing)
- Distributed consensus / Raft implementation
- BusTub recovery code

## Optional (if scaling interest)

- Lecture #23–#24 (distributed OLTP/OLAP — skim)
- [Architecture of a Database System](../papers/architecture.md)

## Notes

<!-- Your notes here -->
