# Engineering Track

**Audience:** Rails / Java / Go backend engineers using PostgreSQL or MySQL.

**Not for:** Database kernel developers, paper authors, or anyone implementing storage engines.

**Goal:** Build a mental model of database behavior so you can explain, predict, and optimize SQL, transactions, and performance in production.

**Target ceiling:** Advanced backend engineer with database awareness clearly stronger than typical application developers — but not a query optimizer author or storage engine engineer.

> **Outcome bar:** Database knowledge > 95% of application developers, < database kernel engineers.  
> High ROI for Rails, GitLab, SaaS, and e-commerce backend work.

---

## What you will be able to do

- Read `EXPLAIN` / `EXPLAIN ANALYZE` and know what the database is doing
- Design indexes (including composite indexes) and predict when they apply
- Understand transactions, isolation levels, and MVCC behavior
- Debug slow queries and fix wrong execution plans
- Design sensible schemas for real access patterns
- Understand PostgreSQL-specific behavior (snapshots, vacuum, bloat)

---

## You do not need to finish all of CMU 15-445

If your goal is backend engineering — not database kernel development — skip implementation depth. Focus on the five parts below.

---

## Five parts (by ROI)

### Part 1 — B+Tree (~40% of practical gains)

**Must learn.** Most SQL performance problems are index problems.

**Understand:**

- Why range queries are fast: `WHERE id BETWEEN 1000 AND 2000`
- Why B+Tree ✓ and Hash ✗ for range scans
- Composite indexes: `INDEX(a, b, c)`
- Leftmost prefix rule — `WHERE a = 1` can use the index; `WHERE b = 1` cannot
- Page / Tuple at conceptual level only

**Do not study:**

- Page split implementation code
- Latch / crabbing implementation
- Clock algorithm, LRU-K, buffer pool frame tables

**CMU:** Lectures #08 (indexes), #07 (hash contrast — skim)  
**Textbook:** Ch 14 (indexing)

---

### Part 2 — Query Execution (~80% core)

**Most engineers lack this.** Required to read execution plans.

**Understand:**

| Operator | Mental model | When it hurts |
|----------|--------------|---------------|
| **Nested Loop Join** | Outer row → scan inner table | Large inner without index |
| **Hash Join** | Build hash table → probe | Best for large equi-joins |
| **Sort-Merge Join** | Sort both sides → merge | Know it exists; less common in daily tuning |

**Goal:** When you see `EXPLAIN ANALYZE`, you know what the database is doing.

**CMU:** Lectures #11–#13 (sort, joins, execution)  
**Textbook:** Ch 15 (query processing)

---

### Part 3 — Transactions + MVCC (most important)

**The part that bites PostgreSQL users hardest.**

**Understand:**

- What a transaction is (`BEGIN` … `COMMIT`) and why it exists
- ACID — Atomicity, Consistency, Isolation, Durability (understand, don't memorize proofs)
- MVCC: reads don't block writes; writes don't block reads — **why**
- Snapshot: each transaction sees a consistent snapshot at start
- Isolation levels: Read Committed, Repeatable Read, Serializable
- **PostgreSQL:** Repeatable Read ≈ Snapshot Isolation (not full Serializable)
- Anomalies: dirty read, non-repeatable read, phantom, **write skew**

**Do not study:**

- 2PL / Strict 2PL / Timestamp Ordering implementation
- Lock manager source code
- Tuple version chain internals

Just know: **MVCC is the modern mainstream approach.**

**CMU:** Lecture #20 (MVCC — deep); #17–#18 (theory / 2PL — skim conclusions only)  
**Textbook:** Ch 18 (concurrency control)

---

### Part 4 — Query Optimizer (high value)

**Understand:**

- Cost-based optimizer — the database does **not** execute in the order you wrote SQL
- Statistics: row counts, distinct values, histograms
- Why `ANALYZE` matters after bulk loads or schema changes
- **Having an index ≠ the optimizer will use it** — it estimates cost

**CMU:** Lectures #15–#16  
**Textbook:** Ch 16 (query optimization)

---

### Part 5 — Recovery (concepts only)

**Understand:**

- WAL (Write-Ahead Log): log first, data pages later
- Why `COMMIT` durability depends on WAL fsync
- Checkpoint purpose (recovery time, not a durability shortcut)

**Do not study:**

- ARIES algorithm details
- Log Sequence Number math
- Physiological logging
- Recovery implementation code

**CMU:** Lecture #21 (logging — conceptual); #22 (recovery — skip)  
**Textbook:** Ch 19.1–19.4 (WAL basics only)

---

## What CMU 15-445 is for (engineering lens)

| Topic | Engineering value | Depth |
|-------|-------------------|-------|
| B+Tree & indexes | Range scans, composite design, leftmost prefix | **Deep** |
| Query execution | NLJ / hash / sort-merge → read EXPLAIN | **Deep** |
| Transactions & MVCC | Isolation, write skew, PostgreSQL RR behavior | **Deep** ★ |
| Query optimizer | Statistics, cost model, index not chosen | **Deep** |
| Recovery / WAL | Durability guarantees | **Conceptual** |
| Buffer pool internals | Implementation | **Skip** |
| Concurrency algorithms (2PL, etc.) | Historical context | **Skip** |
| BusTub projects (P0–P4) | Kernel practice | **Skip** |
| Distributed DB (#23–#24) | Scale patterns | **Optional skim** |

★ Part 3 is the highest-priority phase — allocate extra time here.

---

## Learning boundaries

### Learn deeply

- B+Tree properties, composite indexes, leftmost prefix rule
- Join algorithms and when each wins or fails
- Optimizer: cost model, statistics, plan shapes
- Isolation levels and anomalies (especially write skew)
- MVCC at behavior level: snapshots, visibility, vacuum/bloat
- `EXPLAIN ANALYZE` as a daily tool

### Understand conclusions only

- WAL rule and checkpoint purpose
- Why PostgreSQL Serializable can abort transactions (SSI intuition)
- Buffer pool exists — database manages its own cache
- Page / Tuple storage layout (diagram level)

### Skip or skim

- Buffer pool: Clock algorithm, LRU-K, frame table implementation
- Index concurrency: latch crabbing, page split code
- 2PL / Strict 2PL / Timestamp Ordering algorithms
- ARIES recovery phases in detail
- Tuple version chain implementation
- BusTub P0–P4 coding projects
- Volcano iterator implementation
- Distributed consensus papers

---

## Paper reading (three papers — time-boxed)

Papers are for **design rationale**, not reproduction. If time is limited, read only these three.

| # | Paper | Purpose | When |
|---|-------|---------|------|
| 1 | [A Critique of ANSI SQL Isolation Levels](../10-database/papers/isolation-levels.md) | Dirty read, phantom, write skew; SI ≠ Serializable | E3 |
| 2 | [Serializable Isolation for Snapshot Databases](../10-database/papers/ssi-snapshot-databases.md) | Why SI is not Serializable; SSI aborts | E3 |
| 3 | [The Log-Structured Merge-Tree](../10-database/papers/lsm-tree.md) | Why RocksDB is fast; B+Tree vs LSM trade-offs | E5 capstone |

**Optional (skip if time-constrained):**

- Volcano — iterator model intuition
- Architecture of a Database System — full-system map
- ARIES — recovery algorithm detail

---

## Phase timeline (engineering track)

| Phase | Duration | Focus | Key output |
|-------|----------|-------|------------|
| E1 — B+Tree & indexes | 2 weeks | Part 1 | Index design checklist; leftmost prefix fluency |
| E2 — Query execution | 1.5 weeks | Part 2 | Join intuition; read EXPLAIN operators |
| E3 — Transactions & MVCC ★ | 2 weeks | Part 3 | Isolation guide; write skew + deadlock playbook |
| E4 — Query optimizer | 1 week | Part 4 | Statistics + cost model; tuning playbook |
| E5 — Recovery + PostgreSQL capstone | 1 week | Part 5 + integration | WAL cheat sheet; PostgreSQL ops fluency |

**Total:** ~7–8 weeks at 8–10 hrs/week (no BusTub coding)

---

## PostgreSQL hands-on (apply theory immediately)

Practice after **every** study session — this is how theory becomes skill.

**Core drills:**

1. `EXPLAIN ANALYZE` — observe these operators until they feel familiar:
   - Seq Scan, Index Scan, Bitmap Scan
   - Nested Loop, Hash Join
   - Sort, Aggregate
2. **Index experiments** — add/remove indexes; measure plan changes
3. **Isolation demos** — two sessions; reproduce phantom, write skew, deadlock
4. **MVCC & VACUUM** — long transactions → bloat; read `pg_stat_user_tables`
5. **Slow query journal** — one production-like query per week with root cause

Keep notes in `learning/10-database/notes/`.

---

## Final route (in order)

```
1. CMU 15-445 (selected lectures)
   B+Tree → Query Execution → Transactions → MVCC → Optimizer → WAL (concept)

2. Database System Concepts — Ch 14–18
   Indexing → Query processing → Optimization → Concurrency

3. PostgreSQL practice
   EXPLAIN ANALYZE → MVCC → VACUUM → Index design

4. Three classic papers
   ANSI Isolation Levels → SSI → LSM-Tree
```

---

## BusTub policy

BusTub tasks remain in the repo as **optional kernel track** reference. Engineering track does not require cloning or implementing BusTub.

If you ever want kernel depth later, pull from `02-backlog/backlog.md` kernel section.
