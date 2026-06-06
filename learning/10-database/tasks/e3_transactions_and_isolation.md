# Task: Transactions & Isolation (Engineering)

**Status:** not started  
**Track:** engineering  
**Prerequisite:** e2_query_execution_and_optimizer  
**Registry:** L17–L20, Ch 18, P04, B03

## Goal

Debug production transaction issues: deadlocks, isolation anomalies, MVCC visibility — without implementing a lock manager.

## Must watch

- [ ] Lecture #17 — Concurrency Control Theory
- [ ] Lecture #18 — Two-Phase Locking (understand locks, skip implementation)
- [ ] Lecture #20 — Multi-Version Concurrency Control

## Must read

- [ ] [A Critique of ANSI SQL Isolation Levels](../papers/isolation-levels.md) ← **core paper**
- [ ] Serializable Isolation for Snapshot Databases (SSI — conclusions only)
- [ ] Textbook Ch 18.1–18.7 (ACID, serializability, isolation levels, deadlocks)
- [ ] [PostgreSQL MVCC blog](../blogs/pg-mvcc.md)

## Must understand

- ACID and what each letter means in production
- Isolation levels: Read Uncommitted, RC, RR, Serializable — anomalies each allows
- Snapshot isolation vs serializable — **write skew**
- Why deadlocks happen; detection vs prevention; retry patterns
- MVCC: snapshot, xmin/xmax behavior (Postgres), long transactions → bloat
- Lock modes at SQL level (`SELECT FOR UPDATE`, advisory locks)

## Hands-on (PostgreSQL)

- [ ] Two sessions: reproduce dirty read blocked, phantom under RR, write skew under SI
- [ ] Trigger a deadlock; read `pg_locks` / deadlock log
- [ ] Observe `pg_stat_activity` during lock wait

## Output

- [ ] "Isolation level chooser" — which level for which business scenario
- [ ] Deadlock / lock-wait debugging checklist
- [ ] Isolation paper status → `understanding`

## Skip

- BusTub P4 lock manager implementation
- 2PL graph algorithms in code
- Tuple version chain implementation

## Notes

<!-- Your notes here -->
