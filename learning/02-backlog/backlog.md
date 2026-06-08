# Backlog

Ordered queue. Pull the next item into `01-now/now.md` when the current task is done.

**Active tracks:** DB (primary) + OS (parallel A) + Ruby (parallel B, optional)  
See [engineering-track.md](../00-roadmap/engineering-track.md), [os-engineering-track.md](../00-roadmap/os-engineering-track.md), [ruby-engineering-track.md](../00-roadmap/ruby-engineering-track.md), [master-schedule.md](../00-roadmap/master-schedule.md)

---

## Engineering track

| # | Task | Focus | Status |
|---|------|-------|--------|
| E1 | [B+Tree & Indexes](../10-database/tasks/e1_storage_and_indexes.md) | Part 1 (~40% ROI) | **in progress** ← now |
| E2 | [Query Execution](../10-database/tasks/e2_query_execution.md) | Part 2 (~80% core) | not started |
| E3 | [Transactions & MVCC](../10-database/tasks/e3_transactions_and_isolation.md) | Part 3 ★ most important | not started |
| E4 | [Query Optimizer](../10-database/tasks/e4_query_optimizer.md) | Part 4 | not started |
| E5 | [Recovery & PostgreSQL Capstone](../10-database/tasks/e5_recovery_and_postgresql.md) | Part 5 + integration | not started |

## Foundation (parallel, if rusty)

| # | Task | Status |
|---|------|--------|
| F1 | SQL & relational model (L01–L02, Ch 1–5) | not started |
| F2 | Local PostgreSQL + psql setup for hands-on | not started |

## Optional DB depth (skip for engineering)

| # | Task | Status |
|---|------|--------|
| D1 | [Architecture & Scale](../10-database/tasks/e5_architecture_and_scale.md) | optional |
| D2 | Volcano paper — iterator model | optional |
| D3 | ARIES paper — recovery algorithm detail | skip |

## Optional kernel track (skip for engineering)

| # | Task | Status |
|---|------|--------|
| K0 | Environment setup + BusTub private clone | not started |
| K1 | C++ Primer (BusTub P0) | not started |
| K2 | Buffer Pool Manager (P1) | paused |
| K3 | B+ Tree Index (P2) | not started |
| K4 | Query Execution (P3) | not started |
| K5 | Concurrency Control (P4) | not started |
| K6 | Logging & Recovery (kernel study) | not started |

## OS engineering track (parallel, secondary)

| # | Task | Status |
|---|------|--------|
| O1 | [Foundations](../15-operating-systems/tasks/o1_foundations.md) | **not started** ← parallel |
| O2 | [Process & Memory](../15-operating-systems/tasks/o2_process_and_memory.md) | not started |
| O3 | [Runtime & Linking](../15-operating-systems/tasks/o3_runtime_and_linking.md) | not started |
| O4 | [Concurrency](../15-operating-systems/tasks/o4_concurrency.md) | not started |
| O5 | [Parallel & Async](../15-operating-systems/tasks/o5_parallel_and_async.md) | not started |
| O6 | [I/O, FS & DB Bridge](../15-operating-systems/tasks/o6_io_fs_and_db_bridge.md) | not started |

## Ruby engineering track (parallel B, ~2h/week)

| # | Task | Status |
|---|------|--------|
| R1 | [RubyMonk Ascent](../25-ruby/tasks/r1_rubymonk_ascent.md) | **not started** ← parallel-ruby |
| R2 | [Metaprogramming Workshop](../25-ruby/tasks/r2_metaprogramming_workshop.md) | not started |
| R3 | [Rails Internals](../25-ruby/tasks/r3_rails_internals.md) | not started |
| R4 | [OO Design](../25-ruby/tasks/r4_oo_design.md) | not started |

## LeetCode (parallel, low priority)

See `30-leetcode/backlog.md` — do NOT let this block the engineering tracks.
