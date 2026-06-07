# OS Engineering Track

**Audience:** Backend engineers — 理解进程、内存、并发、I/O、文件系统，能 debug 生产问题，不必写内核。

**Goal:** 建立「应用 ↔ libc ↔ 内核 ↔ 硬件」的行为模型，与 DB 轨互补。

**Target ceiling:** 能读 strace/gdb 输出、解释 fork 后子进程行为、定位并发 bug、理解 fsync 与崩溃一致性 — 不是内核模块开发者。

---

## 与 DB 工程轨的关系

| 轨道 | 每周时间（并行模式） | 角色 |
|------|---------------------|------|
| DB E1–E5 | 5–6 hrs | **主轨** — 当前已在 E1 |
| OS O1–O6 | 3–4 hrs | **副轨** — 按 master-schedule 对齐 |
| LeetCode | ≤2 hrs | 低优先级，不阻塞 |

**原则：** `now.md` 只写一个**主任务**；OS 写在 `parallel.md`，避免双线抢焦点。

---

## 学什么、学到哪

| 主题 | 工程价值 | 深度 |
|------|----------|------|
| 进程 / fork / exec | 理解服务启动、子进程、容器基础 | **Deep** |
| 地址空间 / mmap | 理解内存映射、共享内存、page fault 直觉 | **Deep** |
| 文件描述符 | 理解 socket/pipe/文件统一抽象 | **Deep** |
| libc / 链接加载 | 理解动态库、符号解析、部署问题 | **Deep** |
| 互斥 / 条件变量 / 信号量 | 理解锁、死锁、与 DB 锁的类比 | **Deep** |
| 文件系统 API | open/read/write、崩溃一致性 | **Deep** |
| Shell / 终端 | 日常调试、管道、重定向 | **Deep** |
| 协程 / async | 高并发服务模型 | **Deep** |
| GPU / Token 旅程 | 推理栈、异构计算 | **Skim** |
| 多处理器底层细节 | cache coherence 实现 | **Conceptual** |

---

## 动手练习（替代内核课作业）

用 Linux（本机 WSL / VM / Docker 均可）：

1. **strace** — 跟踪 `fork` + `execve` 一次完整启动
2. **gdb** — 单步过 `malloc` / `free`，对照 L09–L10
3. **小 C 程序** — 父子进程 + pipe；mmap 映射文件
4. **pthread** — 生产者/消费者（mutex + cond）；故意制造 data race 再修
5. **文件实验** — `write` 后不 `fsync` 断电模拟（或对比 `sync`）
6. **笔记** — 每课 3 条「能向别人讲清楚」的要点

笔记目录：`learning/15-operating-systems/notes/`

---

## 环境准备

```bash
# macOS（课程示例偏 Linux，建议 Linux VM 或 Docker）
# 最低工具链
gcc/clang, make, gdb/lldb, strace( Linux ), valgrind(可选)

# 推荐：Ubuntu 22.04+ 虚拟机或容器
docker run -it --name os-lab ubuntu:22.04 bash
apt update && apt install -y build-essential gdb strace valgrind
```

---

## 跳过 / 浅读

- L04 LLM Aside — 兴趣驱动，不阻塞 OS 主线
- L21 Token 旅程 — 与 OS 主线弱相关，可后补
- L20 GPU 细节 — 概念即可
- 手写内核 / xv6 完整实现 — 本轨不要求
