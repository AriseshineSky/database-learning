# Engineering Track

**Audience:** Backend engineers who want to use databases better — not build database kernels.

**Goal:** Build a mental model of database behavior so you can explain, predict, and optimize SQL, transactions, and performance in production.

**Target ceiling:** Senior / Staff-level database user — schema design, query tuning, transaction debugging, scaling to 10M–100M rows. Not query optimizer author or storage engine engineer.

---

## What you will be able to do

- Write non-trivial SQL and design high-quality schemas
- Choose and verify indexes (not guess)
- Diagnose slow queries and wrong execution plans
- Understand transaction anomalies, deadlocks, and isolation levels
- Avoid lock explosions and design sensible partitioning / sharding
- Map production symptoms to database-layer causes (I/O, cache, locks, bloat)

---

## What CMU 15-445 is for (engineering lens)

Not: "teach me to build a database."

Yes: "teach me why the database behaves this way."

| Topic | Engineering value | Depth |
|-------|-------------------|-------|
| Storage & indexes | Why B+ trees are fast, why indexes miss, composite index design | **Deep** |
| Query execution | NLJ / hash / sort-merge join → how you write SQL | **Deep** |
| Query optimizer | Why plans go wrong, statistics, index selection | **Deep** |
| Transactions | Deadlocks, RC / RR / Serializable, MVCC behavior | **Deep** |
| Recovery / WAL | Durability guarantees, why fsync matters | **Conceptual** |
| Buffer pool / lock manager internals | Implementation details | **Skip** |
| BusTub projects (P0–P4) | Kernel practice | **Skip** |

---

## Learning boundaries

### Learn deeply

- B+ tree properties and index design (including composite, covering, partial)
- Join algorithms and when each wins
- Optimizer basics: cost model, statistics, plan shapes
- Isolation levels, anomalies (dirty read, phantom, write skew)
- MVCC at the behavior level (snapshots, visibility, vacuum/bloat)
- EXPLAIN / EXPLAIN ANALYZE as a daily tool

### Understand conclusions only (no implementation)

- WAL rule and checkpoint purpose
- ARIES phases (Analysis → Redo → Undo) — whiteboard level
- Why PostgreSQL Serializable can abort transactions (SSI intuition)
- Read replicas, sharding trade-offs (lectures #23–#24)

### Skip or skim

- Buffer pool frame tables, LRU list implementation
- Lock manager source code, latch crabbing
- Tuple version chain implementation
- Distributed consensus / new storage engine papers
- BusTub P0–P4 coding projects

---

## Paper reading (engineering edition)

Papers are for **design rationale**, not reproduction.

| Paper | Purpose | Depth |
|-------|---------|-------|
| [A Critique of ANSI SQL Isolation Levels](../10-database/papers/isolation-levels.md) | SI ≠ Serializable; write skew | **Must read** |
| Serializable Isolation for Snapshot Databases | Why SSI aborts; Serializable cost | Conceptual |
| [Volcano](../10-database/papers/volcano.md) | Iterator model → plan pipeline intuition | Conceptual |
| [Architecture of a Database System](../10-database/papers/architecture.md) | Full-system map after core topics | Capstone |
| [ARIES](../10-database/papers/aries.md) | Why WAL + recovery exist | Skim |

---

## Phase timeline (engineering track)

| Phase | Duration | Key output |
|-------|----------|------------|
| E1 — Storage & indexes | 2 weeks | Index design checklist; EXPLAIN fluency |
| E2 — Query execution & optimizer | 2 weeks | Join/plan intuition; tuning playbook |
| E3 — Transactions & isolation | 2 weeks | Isolation level guide; deadlock playbook |
| E4 — Recovery & durability | 3 days | WAL / durability mental model |
| E5 — Architecture & scale | 1 week | System map; sharding / replica notes |

**Total:** ~7–8 weeks at 8–10 hrs/week (no BusTub coding)

---

## Hands-on practice (replace BusTub)

Use a real database (PostgreSQL recommended):

1. **EXPLAIN ANALYZE** on every study session — tie lectures to observed plans
2. **Index experiments** — add/remove indexes, measure seq scan vs index scan
3. **Isolation demos** — two sessions, reproduce phantom / write skew / deadlock
4. **Slow query journal** — log one production-like query per week with root cause
5. **Schema review** — redesign one table for access patterns and partitioning

Keep notes in `learning/10-database/notes/`.

---

## BusTub policy

BusTub tasks remain in the repo as **optional kernel track** reference. Engineering track does not require cloning or implementing BusTub.

If you ever want kernel depth later, pull from `02-backlog/backlog.md` kernel section.
