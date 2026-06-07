# Operating Systems Roadmap

NJU 2026 操作系统原理（蒋炎岩 / jyy）— 与 CMU 15-445 工程轨并行。

**课程主页：** https://jyywiki.cn  
**视频合集：** [Bilibili BV1eqEA6JEZA](https://www.bilibili.com/video/BV1eqEA6JEZA)

See [os-engineering-track.md](./os-engineering-track.md) for goals, depth, and DB 交叉点。

## Overview

```
绪论 & 双视角 (应用 / 硬件)
        ↓
进程 & 地址空间 (fork, mmap, fd)
        ↓
C 运行时世界 (libc, 链接, 从零构建 Linux 应用)
        ↓
并发控制 (mutex, cv, semaphore, bugs)
        ↓
并行 & 异步 (协程, SIMD/GPU — 选学)
        ↓
I/O & 存储 & 文件系统
        ↓
数据库系统 (L27) ──→ 衔接 DB E3/E4/E5
```

## Phase timeline (engineering track)

| Phase | Duration | Lectures | Key output |
|-------|----------|----------|------------|
| O1 Foundations | 1 week | #01–#04 | OS 心智模型；能画应用↔内核↔硬件图 |
| O2 Process & memory | 2 weeks | #05–#08 | 能 trace fork/mmap；理解 fd 抽象 |
| O3 Runtime & linking | 2 weeks | #09–#12 | 能 debug libc；理解链接加载 |
| O4 Concurrency | 2 weeks | #13–#18 | 能写正确 pthread；并发 bug 清单 |
| O5 Parallel & async | 1 week | #19–#21 | 协程/async 直觉；GPU 概念级 |
| O6 I/O, FS & DB bridge | 2 weeks | #22–#27 | 文件系统 API；与 DB 轨汇合 |

**Total:** ~10 weeks at 4–5 hrs/week（与 DB 轨并行时）

## Lecture map (NJU 2026)

| # | Title | Task | Depth | ~时长 |
|---|-------|------|-------|-------|
| 01 | Agentic AI 时代的操作系统课：绪论 | o1_foundations | deep | 1:36 |
| 02 | 应用视角的操作系统 | o1_foundations | deep | 1:28 |
| 03 | 硬件视角的操作系统 | o1_foundations | deep | 1:35 |
| 04 | (Aside) LLM, Agents 和 Scaling Law | o1_foundations | skim | 1:22 |
| 05 | 程序和进程；fork, execve, exit | o2_process_and_memory | deep | 1:25 |
| 06 | 进程的地址空间；mmap, munmap, mprotect | o2_process_and_memory | deep | 1:19 |
| 07 | 访问操作系统对象；文件描述符 | o2_process_and_memory | deep | 1:29 |
| 08 | (Aside) 终端和 UNIX Shell | o2_process_and_memory | deep | 1:35 |
| 09 | C 标准库原理 | o3_runtime_and_linking | deep | 1:25 |
| 10 | 调试 C 标准库 | o3_runtime_and_linking | deep | 1:21 |
| 11 | 链接和加载 | o3_runtime_and_linking | deep | 1:29 |
| 12 | 从零开始构建 Linux 应用世界 | o3_runtime_and_linking | deep | 1:26 |
| 13 | 多处理器编程：从入门到放弃 | o4_concurrency | conceptual | 1:23 |
| 14 | 并发控制：互斥 | o4_concurrency | deep | 1:26 |
| 15 | 并发控制：条件变量和万能同步方法 | o4_concurrency | deep | 1:17 |
| 16 | 并发控制：信号量 | o4_concurrency | deep | 1:26 |
| 17 | 并发 Bugs 和应对 | o4_concurrency | deep | 1:29 |
| 18 | 并行算法和数据结构 | o4_concurrency | conceptual | 1:27 |
| 19 | 协程、Goroutine、异步编程 | o5_parallel_and_async | deep | 1:23 |
| 20 | CPU、SIMD 和 GPU | o5_parallel_and_async | conceptual | 1:30 |
| 21 | 一个 Token 的旅程 | o5_parallel_and_async | skim | 1:31 |
| 22 | 输入输出设备和驱动 | o6_io_fs_and_db_bridge | conceptual | 1:27 |
| 23 | 存储设备原理 | o6_io_fs_and_db_bridge | deep | 1:20 |
| 24 | 文件系统 API (1) | o6_io_fs_and_db_bridge | deep | 1:19 |
| 25 | 文件系统 API (2) | o6_io_fs_and_db_bridge | deep | 1:23 |
| 26 | 文件系统实现和崩溃一致性 | o6_io_fs_and_db_bridge | deep | 1:27 |
| 27 | 数据库系统 | o6_io_fs_and_db_bridge | deep | 1:23 |

Playlist: https://www.bilibili.com/video/BV1eqEA6JEZA

## 与 DB 轨的交叉点

| OS 内容 | DB 轨对应 | 价值 |
|---------|-----------|------|
| L06 mmap / 地址空间 | E1 存储、页概念 | 理解 page cache 为何存在 |
| L14–17 并发 | E3 事务与隔离 | 锁、条件变量 ↔ 2PL、死锁 |
| L23 存储设备 | E1/E4 | 磁盘、顺序写、fsync |
| L26 崩溃一致性 | E4 Recovery | WAL / journaling 的 OS 层动机 |
| L27 数据库系统 | E3–E5 汇合 | 两门课在此闭合 |

**建议同步窗口：** DB E3 进行时，OS 推到 O4；DB E4 时，OS 推到 O6。
