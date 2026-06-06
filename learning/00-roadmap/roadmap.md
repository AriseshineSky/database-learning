# Learning Roadmap

CMU 15-445 self-study path. Each phase maps to BusTub projects + lectures + papers.

## Overview

```
SQL & Relational Model
        ↓
Storage (Buffer Pool, Pages, Disk)
        ↓
Indexes (B+ Tree, Hash)
        ↓
Query Execution (Volcano model, Joins, Sort)
        ↓
Query Optimization
        ↓
Concurrency (2PL, Timestamp, MVCC)
        ↓
Recovery (WAL, ARIES)
        ↓
Distributed Systems
```

## Phase timeline (estimate)

| Phase | Duration | Key output |
|-------|----------|------------|
| Setup + P0 | 1 week | C++ ready, BusTub compiles |
| P1 Buffer Pool | 2 weeks | LRU replacement working |
| P2 B+ Tree | 3 weeks | Index insert/search/delete |
| P3 Query Execution | 3 weeks | Iterator model executors |
| P4 Concurrency | 3 weeks | Lock manager + 2PL |
| Recovery study | 1 week | ARIES paper + notes |
| Architecture paper | 1 week | Full-system mental model |

**Total:** ~3–4 months at 10–15 hrs/week

## Lecture map (CMU Spring 2026)

| Lectures | Topic | BusTub Project |
|----------|-------|----------------|
| #01–#02 | Relational model, SQL | — |
| #03–#05 | Storage, Memory Mgmt | P1 |
| #06–#10 | Indexes, B+ Tree | P2 |
| #11–#16 | Query execution & optimization | P3 |
| #17–#21 | Concurrency, MVCC | P4 |
| #22–#23 | Logging, Recovery | study |
| #24–#25 | Distributed DB | study |

## Paper reading order

Papers are **not** read in isolation — each is tied to a task:

1. **Volcano** → before/during P3 (query execution)
2. **ARIES** → during recovery study (after P4)
3. **Architecture of a Database System** → after all projects (capstone overview)

Optional (later):
- What Goes Around Comes Around (data models)
- A Critique of ANSI SQL Isolation Levels
