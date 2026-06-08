# Learning Roadmap

CMU 15-445 self-study path for **Rails / Java / Go backend engineers** — build a database behavior model, not a database kernel.

See [engineering-track.md](./engineering-track.md) for goals, five-part structure, boundaries, and what to skip.

## Overview

```
B+Tree & Indexes              ← Part 1 (~40% ROI) — most perf issues are index issues
        ↓
Query Execution               ← Part 2 (~80% core) — read EXPLAIN ANALYZE
        ↓
Transactions & MVCC ★         ← Part 3 (most important) — PostgreSQL's sharp edge
        ↓
Query Optimizer               ← Part 4 — statistics, cost model, index not chosen
        ↓
Recovery (WAL only)             ← Part 5 — log before data; skip ARIES
        ↓
PostgreSQL capstone             ← EXPLAIN, MVCC, VACUUM, index design in practice
```

## Phase timeline (engineering track)

| Phase | Duration | Focus | Key output |
|-------|----------|-------|------------|
| E1 B+Tree & indexes | 2 weeks | Part 1 | Index checklist; leftmost prefix |
| E2 Query execution | 1.5 weeks | Part 2 | Join types; EXPLAIN operator fluency |
| E3 Transactions & MVCC ★ | 2 weeks | Part 3 | Isolation guide; write skew playbook |
| E4 Query optimizer | 1 week | Part 4 | Statistics; why index wasn't picked |
| E5 Recovery + PG capstone | 1 week | Part 5 + practice | WAL cheat sheet; PostgreSQL ops |

**Total:** ~7–8 weeks at 8–10 hrs/week

## Lecture map (CMU Fall 2025)

| Lectures | Topic | Task | Depth |
|----------|-------|------|-------|
| #01–#02 | Relational model, SQL | foundation | read if rusty |
| #07 | Hash tables | e1_storage_and_indexes | skim (contrast with B+Tree) |
| #08 | Indexes & B+Tree | e1_storage_and_indexes | **deep** |
| #10 | Index concurrency | e1_storage_and_indexes | **skip** (latch idea only) |
| #11–#13 | Sort, joins, execution | e2_query_execution | **deep** |
| #15–#16 | Query optimization | e4_query_optimizer | **deep** |
| #17–#18 | Concurrency theory, 2PL | e3_transactions_and_isolation | **skip** (conclusions only) |
| #20 | MVCC | e3_transactions_and_isolation | **deep** ★ |
| #21 | Logging / WAL | e5_recovery_and_postgresql | conceptual |
| #22 | Recovery (ARIES) | e5_recovery_and_postgresql | **skip** |
| #23–#24 | Distributed DB | optional | skim |

**Skip entirely:** #03–#05 (storage layout detail), #04 (buffer pool implementation), #10 (latch crabbing)

Videos: [Fall 2025 YouTube playlist](https://www.youtube.com/playlist?list=PLSE8ODhjZXjYMAgsGH-GtY5rJYZ6zjsd5)

## Textbook (*Database System Concepts*, Ch 14–18)

| Chapters | Topic | Task | Depth |
|----------|-------|------|-------|
| Ch 14 | Indexing (B+Tree, hash, composite) | E1 | deep |
| Ch 15 | Query processing (joins, aggregation) | E2 | deep |
| Ch 16 | Query optimization (statistics, cost) | E4 | deep |
| Ch 17–18 | Transactions, concurrency, MVCC | E3 | deep |

Skip: Ch 12–13 (storage/buffer replacement policies), Ch 19+ (recovery detail beyond WAL concept)

## Paper reading order (three papers only)

If time is limited, read **only these three**:

1. **A Critique of ANSI SQL Isolation Levels** → E3 (dirty read, phantom, write skew)
2. **Serializable Isolation for Snapshot Databases** → E3 (why SI ≠ Serializable)
3. **The Log-Structured Merge-Tree** → E5 (B+Tree vs LSM; why RocksDB is fast)

Optional: Volcano (iterator intuition), Architecture of a Database System (system map), ARIES (skip)

## PostgreSQL practice (throughout + capstone)

Apply theory immediately after each phase:

| Operator / topic | When to drill |
|------------------|---------------|
| Seq Scan, Index Scan, Bitmap Scan | E1, E4 |
| Nested Loop, Hash Join, Sort, Aggregate | E2 |
| Isolation demos, `pg_locks`, write skew | E3 |
| `ANALYZE`, bad row estimates, plan flip | E4 |
| WAL settings, MVCC bloat, `VACUUM` | E5 |

## Optional kernel track

BusTub projects (P0–P4) remain in `10-database/tasks/p*.md` for anyone who later wants implementation depth. **Not required** for the engineering track.
