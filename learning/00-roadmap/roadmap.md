# Learning Roadmap

CMU 15-445 self-study path for **backend engineers** — build a database behavior model, not a database kernel.

See [engineering-track.md](./engineering-track.md) for goals, boundaries, and what to skip.

## Overview

```
SQL & Relational Model (foundation)
        ↓
Storage & Indexes          ← deep (behavior + EXPLAIN)
        ↓
Query Execution & Optimizer ← deep (joins, plans, statistics)
        ↓
Transactions & Isolation   ← deep (MVCC, deadlocks, anomalies)
        ↓
Recovery & Durability      ← conceptual (WAL, checkpoints)
        ↓
Architecture & Scale       ← capstone (replicas, sharding, system map)
```

## Phase timeline (engineering track)

| Phase | Duration | Key output |
|-------|----------|------------|
| E1 Storage & indexes | 2 weeks | Index design checklist; EXPLAIN fluency |
| E2 Query & optimizer | 2 weeks | Join/plan intuition; tuning playbook |
| E3 Transactions | 2 weeks | Isolation guide; deadlock playbook |
| E4 Recovery | 3 days | WAL / durability cheat sheet |
| E5 Architecture | 1 week | Full-system map; scale notes |

**Total:** ~7–8 weeks at 8–10 hrs/week

## Lecture map (CMU Fall 2025)

| Lectures | Topic | Engineering task | Depth |
|----------|-------|------------------|-------|
| #01–#02 | Relational model, SQL | foundation | read if rusty |
| #03–#05 | Storage, memory | e1_storage_and_indexes | deep (behavior) |
| #06–#10 | Indexes, B+ tree | e1_storage_and_indexes | deep |
| #11–#16 | Execution & optimization | e2_query_execution_and_optimizer | deep |
| #17–#20 | Concurrency, MVCC | e3_transactions_and_isolation | deep |
| #21–#22 | Logging, recovery | e4_recovery_and_durability | conceptual |
| #23–#24 | Distributed DB | e5_architecture_and_scale | skim |

Videos: [Fall 2025 YouTube playlist](https://www.youtube.com/playlist?list=PLSE8ODhjZXjYMAgsGH-GtY5rJYZ6zjsd5)

## Paper reading order (engineering)

Papers explain **why** systems are designed this way — not homework to implement.

1. **A Critique of ANSI SQL Isolation Levels** → during E3 (isolation anomalies)
2. **Serializable Isolation for Snapshot Databases** → during E3 (SSI intuition)
3. **Volcano** → during E2 (iterator / plan pipeline — conceptual)
4. **Architecture of a Database System** → during E5 (capstone overview)
5. **ARIES** → during E4 (skim — WAL + recovery phases)

## Optional kernel track

BusTub projects (P0–P4) remain in `10-database/tasks/p*.md` for anyone who later wants implementation depth. **Not required** for the engineering track.
