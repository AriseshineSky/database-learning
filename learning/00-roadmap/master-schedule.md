# Master Schedule — DB + OS 双轨

**起始日：** 2026-06-06  
**模式：** 主轨 DB + 副轨 OS 并行（见 `01-now/parallel.md`）

---

## 时间预算

| 周 | DB（主） | OS（副） | 合计 |
|----|----------|----------|------|
| 典型周 | 5–6 h | 3–4 h | 8–10 h |

---

## 阶段对齐（关键）

```
周次    DB 轨                    OS 轨                    协同点
─────────────────────────────────────────────────────────────────
W1–2    E1 Storage & Indexes     O1 Foundations           页 / 存储直觉
W3–4    E1 收尾 → E2 Query       O2 Process & Memory      进程即资源容器
W5–6    E2 Query                 O3 Runtime & Linking     服务启动链路
W7–8    E3 Transactions ★        O4 Concurrency ★         锁 / 死锁 / 同步
W9      E4 Recovery ★            O6 I/O & FS (前半) ★     WAL / 崩溃一致性
W10     E5 Architecture          O6 L27 DB bridge ★       系统全景闭合
```

★ = 两轨应刻意对齐，同一周做 weekly review 时对照笔记。

---

## 当前状态（2026-06-06）

| 轨 | 当前任务 | 状态 |
|----|----------|------|
| DB | E1 Storage & Indexes | in progress |
| OS | O1 Foundations | not started |

---

## 每周节奏（模板）

| 天 | DB（主） | OS（副） |
|----|----------|----------|
| Mon | 1 CMU lecture + EXPLAIN 练习 | — |
| Tue | — | 1 jyy lecture + 笔记 |
| Wed | 教材章节 / 论文 | — |
| Thu | — | 1 jyy lecture 或动手实验 |
| Fri | weekly 难点补课 | OS 小实验（strace/gdb/pthread） |
| Sun | **weekly review** | 更新 registry + backlog |

可根据工作周灵活调换，但**每周至少完成：1 个 DB 里程碑 + 2 集 OS 视频**。

---

## 决策规则

1. **冲突时保主轨** — DB `now.md` 任务未完成，OS 只维持最低进度（1 集/周）。
2. **汇合周不可跳过** — W7–10 的双轨对齐是设计好的，尽量遵守。
3. **L27 是里程碑** — 完成 O6 且看完 L27 后，在 DB backlog 中标记 E3–E5 的 OS 先修已完成。
4. **一课一输出** — 每集 OS 视频至少留下：3 条笔记 OR 1 个小实验，否则算「看过」不算「学过」。

---

## 完成定义

### DB 轨（已有）
- E1–E5 各任务 Output checklist 全勾

### OS 轨
- O1–O6 各任务 Output checklist 全勾
- `15-operating-systems/notes/` 至少 15 条可复述要点
- 能独立完成：strace 跟踪进程启动、pthread 生产者消费者、解释 fsync 与崩溃一致性
