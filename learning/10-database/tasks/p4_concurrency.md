# Task: Concurrency Control (BusTub P4)

**Status:** not started  
**Prerequisite:** P3  
**Registry:** L17–L20, Ch 18, P04, B03

## Goal

Implement lock manager + two-phase locking. Understand MVCC design (study, may not fully implement).

## Must Read

- [ ] [Lecture #17 — Concurrency Control Theory](../../lectures/l17-concurrency-theory.md)
- [ ] [Lecture #18 — Two-Phase Locking](../../lectures/l18-2pl.md)
- [ ] [Lecture #20 — MVCC](../../lectures/l19-mvcc.md)
- [ ] Textbook Ch 18.1–18.9
- [ ] BusTub P4 project handout

## Must Understand

- ACID, serializability, conflict serializability
- 2PL: growing / shrinking phase, deadlock detection
- Lock modes: shared, exclusive, intention locks
- MVCC: version chains, snapshot isolation (conceptual)

## Optional

- [ ] [Isolation Levels paper](../../papers/isolation-levels.md)
- [ ] [PostgreSQL MVCC blog](../../blogs/pg-mvcc.md)
- [ ] CMU Lecture #19 (Timestamp Ordering) — optional

## Output

- [ ] Lock manager implemented
- [ ] 2PL working
- [ ] P4 tests pass

## Notes

<!-- Your notes here -->
