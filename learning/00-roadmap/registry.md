# Knowledge Registry

Single source of truth. Every entry links to a task in `10-database/tasks/` or `15-operating-systems/tasks/`.

**Status:** `not started` | `reading` | `understanding` | `implemented` | `mastered`  
**Depth (engineering):** `deep` | `conceptual` | `skim` | `skip`

---

## Lectures

| ID | Title | Link | Task | Depth | Status |
|----|-------|------|------|-------|--------|
| L01 | Relational Model & Algebra | [CMU #01](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | foundation | deep | not started |
| L03 | Database Storage I | [CMU #03](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e1_storage_and_indexes | conceptual | not started |
| L04 | Memory Management | [CMU #04](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e1_storage_and_indexes | conceptual | not started |
| L07 | Hash Tables | [CMU #07](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e1_storage_and_indexes | skim | not started |
| L08 | Indexes & Filters I | [CMU #08](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e1_storage_and_indexes | deep | not started |
| L10 | Index Concurrency Control | [CMU #10](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e1_storage_and_indexes | skim | not started |
| L11 | Sorting & Aggregations | [CMU #11](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e2_query_execution_and_optimizer | deep | not started |
| L12 | Joins Algorithms | [CMU #12](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e2_query_execution_and_optimizer | deep | not started |
| L13 | Query Execution I | [CMU #13](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e2_query_execution_and_optimizer | deep | not started |
| L15 | Query Optimization I | [CMU #15](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e2_query_execution_and_optimizer | deep | not started |
| L16 | Query Optimization II | [CMU #16](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e2_query_execution_and_optimizer | deep | not started |
| L17 | Concurrency Control Theory | [CMU #17](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e3_transactions_and_isolation | deep | not started |
| L18 | Two-Phase Locking | [CMU #18](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e3_transactions_and_isolation | conceptual | not started |
| L20 | Multi-Version Concurrency Control | [CMU #20](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e3_transactions_and_isolation | deep | not started |
| L21 | Database Logging | [CMU #21](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e4_recovery_and_durability | conceptual | not started |
| L22 | Database Recovery | [CMU #22](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e4_recovery_and_durability | skim | not started |
| L23 | Distributed OLTP | [CMU #23](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e5_architecture_and_scale | skim | not started |
| L24 | Distributed OLAP | [CMU #24](https://15445.courses.cs.cmu.edu/fall2025/schedule.html) | e5_architecture_and_scale | skim | not started |

Card files: `10-database/lectures/`

---

## Papers

| ID | Title | Card | Task | Depth | Status |
|----|-------|------|------|-------|--------|
| P01 | Volcano — Extensible Query Evaluation | [volcano.md](../10-database/papers/volcano.md) | e2_query_execution_and_optimizer | conceptual | not started |
| P02 | ARIES Recovery Algorithm | [aries.md](../10-database/papers/aries.md) | e4_recovery_and_durability | skim | not started |
| P03 | Architecture of a Database System | [architecture.md](../10-database/papers/architecture.md) | e5_architecture_and_scale | deep | not started |
| P04 | A Critique of ANSI SQL Isolation Levels | [isolation-levels.md](../10-database/papers/isolation-levels.md) | e3_transactions_and_isolation | deep | not started |
| P05 | Serializable Isolation for Snapshot Databases | [ssi-snapshot-databases.md](../10-database/papers/ssi-snapshot-databases.md) | e3_transactions_and_isolation | conceptual | not started |

---

## Textbook chapters

| Chapters | Topic | Task | Depth | Status |
|----------|-------|------|-------|--------|
| Ch 1–2 | Intro, Relational model | foundation | deep | not started |
| Ch 3–5 | SQL | foundation | deep | not started |
| Ch 12 | Storage structure | e1_storage_and_indexes | conceptual | not started |
| Ch 13.1–13.2 | Disk vs memory | e1_storage_and_indexes | conceptual | not started |
| Ch 14 | Indexing | e1_storage_and_indexes | deep | not started |
| Ch 15 | Query processing | e2_query_execution_and_optimizer | deep | not started |
| Ch 16 | Query optimization | e2_query_execution_and_optimizer | deep | not started |
| Ch 18 | Concurrency | e3_transactions_and_isolation | deep | not started |
| Ch 19.1–19.4 | Recovery basics | e4_recovery_and_durability | conceptual | not started |
| Ch 22–23 | Replication, partitioning | e5_architecture_and_scale | skim | not started |

Book: *Database System Concepts*, 7th ed.

---

## Blogs & external

| ID | Title | Card | Task | Depth | Status |
|----|-------|------|------|-------|--------|
| B01 | CMU 15-445 study guide (csdiy) | [csdiy-15445.md](../10-database/blogs/csdiy-15445.md) | foundation | skim | not started |
| B02 | PostgreSQL buffer manager internals | [pg-buffer.md](../10-database/blogs/pg-buffer.md) | e1_storage_and_indexes | conceptual | not started |
| B03 | PostgreSQL MVCC internals | [pg-mvcc.md](../10-database/blogs/pg-mvcc.md) | e3_transactions_and_isolation | deep | not started |

---

## Projects

### Engineering track (active)

| ID | Task | Card | Status |
|----|------|------|--------|
| E1 | Storage & Indexes | [e1_storage_and_indexes.md](../10-database/tasks/e1_storage_and_indexes.md) | in progress |
| E2 | Query Execution & Optimizer | [e2_query_execution_and_optimizer.md](../10-database/tasks/e2_query_execution_and_optimizer.md) | not started |
| E3 | Transactions & Isolation | [e3_transactions_and_isolation.md](../10-database/tasks/e3_transactions_and_isolation.md) | not started |
| E4 | Recovery & Durability | [e4_recovery_and_durability.md](../10-database/tasks/e4_recovery_and_durability.md) | not started |
| E5 | Architecture & Scale | [e5_architecture_and_scale.md](../10-database/tasks/e5_architecture_and_scale.md) | not started |

### Kernel track (optional — BusTub)

| ID | Project | Card | Status |
|----|---------|------|--------|
| BT0 | C++ Primer | [p0_cpp_primer.md](../10-database/tasks/p0_cpp_primer.md) | not started |
| BT1 | Buffer Pool Manager | [p1_buffer_pool.md](../10-database/tasks/p1_buffer_pool.md) | paused |
| BT2 | B+ Tree Index | [p2_b_plus_tree.md](../10-database/tasks/p2_b_plus_tree.md) | not started |
| BT3 | Query Execution | [p3_query_execution.md](../10-database/tasks/p3_query_execution.md) | not started |
| BT4 | Concurrency Control | [p4_concurrency.md](../10-database/tasks/p4_concurrency.md) | not started |

---

## OS Lectures (NJU 2026 / jyy)

Playlist: [Bilibili BV1eqEA6JEZA](https://www.bilibili.com/video/BV1eqEA6JEZA)

| ID | Title | Task | Depth | Status |
|----|-------|------|-------|--------|
| OS-L01 | 绪论 | o1_foundations | deep | not started |
| OS-L02 | 应用视角的操作系统 | o1_foundations | deep | not started |
| OS-L03 | 硬件视角的操作系统 | o1_foundations | deep | not started |
| OS-L04 | LLM, Agents 和 Scaling Law (Aside) | o1_foundations | skim | not started |
| OS-L05 | fork, execve, exit | o2_process_and_memory | deep | not started |
| OS-L06 | mmap, munmap, mprotect | o2_process_and_memory | deep | not started |
| OS-L07 | 文件描述符 | o2_process_and_memory | deep | not started |
| OS-L08 | 终端和 UNIX Shell (Aside) | o2_process_and_memory | deep | not started |
| OS-L09 | C 标准库原理 | o3_runtime_and_linking | deep | not started |
| OS-L10 | 调试 C 标准库 | o3_runtime_and_linking | deep | not started |
| OS-L11 | 链接和加载 | o3_runtime_and_linking | deep | not started |
| OS-L12 | 从零构建 Linux 应用世界 | o3_runtime_and_linking | deep | not started |
| OS-L13 | 多处理器编程 | o4_concurrency | conceptual | not started |
| OS-L14 | 互斥 | o4_concurrency | deep | not started |
| OS-L15 | 条件变量 | o4_concurrency | deep | not started |
| OS-L16 | 信号量 | o4_concurrency | deep | not started |
| OS-L17 | 并发 Bugs | o4_concurrency | deep | not started |
| OS-L18 | 并行算法和数据结构 | o4_concurrency | conceptual | not started |
| OS-L19 | 协程、Goroutine、异步 | o5_parallel_and_async | deep | not started |
| OS-L20 | CPU、SIMD 和 GPU | o5_parallel_and_async | conceptual | not started |
| OS-L21 | 一个 Token 的旅程 | o5_parallel_and_async | skim | not started |
| OS-L22 | I/O 设备和驱动 | o6_io_fs_and_db_bridge | conceptual | not started |
| OS-L23 | 存储设备原理 | o6_io_fs_and_db_bridge | deep | not started |
| OS-L24 | 文件系统 API (1) | o6_io_fs_and_db_bridge | deep | not started |
| OS-L25 | 文件系统 API (2) | o6_io_fs_and_db_bridge | deep | not started |
| OS-L26 | 文件系统与崩溃一致性 | o6_io_fs_and_db_bridge | deep | not started |
| OS-L27 | 数据库系统 | o6_io_fs_and_db_bridge | deep | not started |

Card files: `15-operating-systems/lectures/` (add as you watch)

---

## OS Projects (engineering track)

| ID | Task | Card | Status |
|----|------|------|--------|
| O1 | Foundations | [o1_foundations.md](../15-operating-systems/tasks/o1_foundations.md) | not started |
| O2 | Process & Memory | [o2_process_and_memory.md](../15-operating-systems/tasks/o2_process_and_memory.md) | not started |
| O3 | Runtime & Linking | [o3_runtime_and_linking.md](../15-operating-systems/tasks/o3_runtime_and_linking.md) | not started |
| O4 | Concurrency | [o4_concurrency.md](../15-operating-systems/tasks/o4_concurrency.md) | not started |
| O5 | Parallel & Async | [o5_parallel_and_async.md](../15-operating-systems/tasks/o5_parallel_and_async.md) | not started |
| O6 | I/O, FS & DB Bridge | [o6_io_fs_and_db_bridge.md](../15-operating-systems/tasks/o6_io_fs_and_db_bridge.md) | not started |
