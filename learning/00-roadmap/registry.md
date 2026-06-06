# Knowledge Registry

Single source of truth. Every entry must link to a task in `10-database/tasks/`.

**Status:** `not started` | `reading` | `understanding` | `implemented` | `mastered`

---

## Lectures

| ID | Title | Link | Task | Status |
|----|-------|------|------|--------|
| L01 | Relational Model & Algebra | [CMU #01](https://15445.courses.cs.cmu.edu/spring2026/) | setup | not started |
| L04 | Memory Management | [CMU #04](https://15445.courses.cs.cmu.edu/spring2026/) | p1_buffer_pool | reading |
| L07 | Hash Tables | [CMU #07](https://15445.courses.cs.cmu.edu/spring2026/) | p2_b_plus_tree | not started |
| L08 | Indexes & Filters I | [CMU #08](https://15445.courses.cs.cmu.edu/spring2026/) | p2_b_plus_tree | not started |
| L10 | Index Concurrency Control | [CMU #10](https://15445.courses.cs.cmu.edu/spring2026/) | p2_b_plus_tree | not started |
| L11 | Sorting & Aggregations | [CMU #11](https://15445.courses.cs.cmu.edu/spring2026/) | p3_query_execution | not started |
| L12 | Joins Algorithms | [CMU #12](https://15445.courses.cs.cmu.edu/spring2026/) | p3_query_execution | not started |
| L13 | Query Execution I | [CMU #13](https://15445.courses.cs.cmu.edu/spring2026/) | p3_query_execution | not started |
| L17 | Concurrency Control Theory | [CMU #17](https://15445.courses.cs.cmu.edu/spring2026/) | p4_concurrency | not started |
| L18 | Two-Phase Locking | [CMU #18](https://15445.courses.cs.cmu.edu/spring2026/) | p4_concurrency | not started |
| L19 | MVCC I | [CMU #19](https://15445.courses.cs.cmu.edu/spring2026/) | p4_concurrency | not started |
| L22 | Database Logging | [CMU #22](https://15445.courses.cs.cmu.edu/spring2026/) | recovery_study | not started |
| L23 | Database Recovery | [CMU #23](https://15445.courses.cs.cmu.edu/spring2026/) | recovery_study | not started |

Card files: `10-database/lectures/`

---

## Papers

| ID | Title | Card | Task | Status |
|----|-------|------|------|--------|
| P01 | Volcano — Extensible Query Evaluation | [volcano.md](../10-database/papers/volcano.md) | p3_query_execution | not started |
| P02 | ARIES Recovery Algorithm | [aries.md](../10-database/papers/aries.md) | recovery_study | not started |
| P03 | Architecture of a Database System | [architecture.md](../10-database/papers/architecture.md) | capstone | not started |
| P04 | A Critique of ANSI SQL Isolation Levels | [isolation-levels.md](../10-database/papers/isolation-levels.md) | p4_concurrency | not started |

---

## Textbook chapters

| Chapters | Topic | Task | Status |
|----------|-------|------|--------|
| Ch 1–2 | Intro, Relational model | setup | not started |
| Ch 3–5 | SQL | setup | not started |
| Ch 12–13 | Storage, Buffer pool | p1_buffer_pool | reading |
| Ch 14 | Indexing | p2_b_plus_tree | not started |
| Ch 15 | Query processing | p3_query_execution | not started |
| Ch 16 | Query optimization | p3_query_execution | not started |
| Ch 18 | Concurrency | p4_concurrency | not started |
| Ch 19 | Recovery | recovery_study | not started |

Book: *Database System Concepts*, 7th ed.

---

## Blogs & external

| ID | Title | Card | Task | Status |
|----|-------|------|------|--------|
| B01 | CMU 15-445 study guide (csdiy) | [csdiy-15445.md](../10-database/blogs/csdiy-15445.md) | setup | not started |
| B02 | PostgreSQL buffer manager internals | [pg-buffer.md](../10-database/blogs/pg-buffer.md) | p1_buffer_pool | not started |
| B03 | PostgreSQL MVCC internals | [pg-mvcc.md](../10-database/blogs/pg-mvcc.md) | p4_concurrency | not started |

---

## Projects (BusTub)

| ID | Project | Card | Status |
|----|---------|------|--------|
| BT0 | C++ Primer | [p0_cpp_primer.md](../10-database/tasks/p0_cpp_primer.md) | not started |
| BT1 | Buffer Pool Manager | [p1_buffer_pool.md](../10-database/tasks/p1_buffer_pool.md) | in progress |
| BT2 | B+ Tree Index | [p2_b_plus_tree.md](../10-database/tasks/p2_b_plus_tree.md) | not started |
| BT3 | Query Execution | [p3_query_execution.md](../10-database/tasks/p3_query_execution.md) | not started |
| BT4 | Concurrency Control | [p4_concurrency.md](../10-database/tasks/p4_concurrency.md) | not started |
