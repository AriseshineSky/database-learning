# Task: Transactions & MVCC (Engineering E3)

**Status:** not started  
**Track:** engineering — Part 3 ★ **most important**  
**Prerequisite:** e2_query_execution  
**Registry:** L17–L18 (skim), L20, Ch 17–18, P04, P05, B03

## Goal

Debug production transaction issues: deadlocks, isolation anomalies, MVCC visibility — without implementing a lock manager.

**This is the phase PostgreSQL users get wrong most often.** Allocate extra time here.

## Must watch

- [ ] Lecture #20 — Multi-Version Concurrency Control (**deep — core lecture**)

## Skim only (conclusions, not algorithms)

- [ ] Lecture #17 — Concurrency Control Theory (anomaly names only)
- [ ] Lecture #18 — Two-Phase Locking (know locks exist; skip graph algorithms)

## Must read

- [ ] [A Critique of ANSI SQL Isolation Levels](../papers/isolation-levels.md) ← **paper #1**
- [ ] [Serializable Isolation for Snapshot Databases](../papers/ssi-snapshot-databases.md) ← **paper #2**
- [ ] Textbook Ch 17–18 (ACID, serializability, isolation levels, deadlocks, MVCC)
- [ ] [PostgreSQL MVCC blog](../blogs/pg-mvcc.md)

## Must understand

- ACID — what each letter means in production (understand, don't prove)
- Isolation levels: Read Committed, Repeatable Read, Serializable — anomalies each allows
- **PostgreSQL:** Repeatable Read ≈ Snapshot Isolation (not full Serializable)
- MVCC: reads don't block writes; writes don't block reads — **why** (snapshot at transaction start)
- Anomalies: dirty read, non-repeatable read, phantom, **write skew**
- Why deadlocks happen; detection; retry patterns
- Long transactions → bloat (xmin/xmax behavior at ops level)
- Lock modes at SQL level (`SELECT FOR UPDATE`, advisory locks)

## Hands-on (PostgreSQL)

- [ ] Two sessions: reproduce phantom under RC, write skew under RR (Snapshot Isolation)
- [ ] Trigger a deadlock; read `pg_locks` / deadlock log
- [ ] Observe `pg_stat_activity` during lock wait
- [ ] Compare `READ COMMITTED` vs `REPEATABLE READ` on the same multi-statement script

## Output

- [ ] "Isolation level chooser" — which level for which business scenario
- [ ] Deadlock / lock-wait debugging checklist
- [ ] Both isolation papers status → `understanding`
- [ ] Can explain write skew to a teammate with a concrete example

## Skip

- 2PL / Strict 2PL / Timestamp Ordering implementation
- BusTub P4 lock manager implementation
- Tuple version chain source-level internals

## Notes

<!-- Your notes here -->
