# Systems Learning System

Task-driven knowledge system for **backend engineers**:

- **DB 主轨** — CMU 15-445（用库、调优、事务，不写内核）
- **OS 副轨** — [NJU 2026 操作系统原理](https://www.bilibili.com/video/BV1eqEA6JEZA)（蒋炎岩 / jyy）

**Not a file dump.** Every material must be linked to a task.

## Who this is for

You want Staff-level database fluency: complex SQL, schema design, index tuning, transaction debugging, and scale decisions — without implementing buffer pools or lock managers.

Read the full philosophy: [learning/00-roadmap/engineering-track.md](learning/00-roadmap/engineering-track.md)

## Daily workflow

```bash
# 1. 今天主任务（DB）
cat learning/01-now/now.md

# 2. 主任务完成后 — 副轨（OS）
cat learning/01-now/parallel.md

# 3. 查资料 registry
cat learning/00-roadmap/registry.md

# 4. 双轨时间表
cat learning/00-roadmap/master-schedule.md

# 5. 执行具体 checklist
cat learning/10-database/tasks/<task>.md
cat learning/15-operating-systems/tasks/<task>.md
```

## Structure

```
learning/
├── 00-roadmap/           # roadmap, registry, master-schedule
│   ├── engineering-track.md      # DB 工程轨
│   ├── os-engineering-track.md   # OS 工程轨
│   ├── os-roadmap.md             # OS 27 讲映射
│   └── master-schedule.md        # DB+OS 双轨对齐
├── 01-now/
│   ├── now.md            # 主任务（DB）— 只有一个焦点
│   └── parallel.md       # 副任务（OS）
├── 02-backlog/
├── 10-database/          # CMU 15-445
│   ├── tasks/            # e1–e5
│   ├── papers/ lectures/ blogs/ notes/
├── 15-operating-systems/ # NJU 2026 OS (jyy)
│   ├── tasks/            # o1–o6
│   ├── lectures/         # 视频卡片（边看边建）
│   └── notes/            # strace/gdb/并发实验笔记
├── 20-architecture/
└── 30-leetcode/
```

## Rules

1. **Only one primary task in `now.md`** — OS 放 `parallel.md`，主轨完成后再做副轨。
2. **New material → must link to a task** — otherwise it is dead weight.
3. **Store cards, not PDFs** — link to source + write your understanding.
4. **Status must flow:** `not started → reading → understanding → mastered`
5. **Hands-on = PostgreSQL + EXPLAIN** — not BusTub coding (unless kernel track).
6. **Weekly review** — use `learning/00-roadmap/weekly-review.md`

## Course resources

### Database (primary)

| Resource | Link |
|----------|------|
| CMU 15-445 (Fall 2025) | https://15445.courses.cs.cmu.edu/fall2025/ |
| Course schedule + per-lecture videos | https://15445.courses.cs.cmu.edu/fall2025/schedule.html |
| Textbook | Database System Concepts, 7th ed. (Silberschatz) |
| Lectures (YouTube, Fall 2025) | https://www.youtube.com/playlist?list=PLSE8ODhjZXjYMAgsGH-GtY5rJYZ6zjsd5 |
| Hands-on DB | PostgreSQL (local or Docker) |

### Operating Systems (parallel)

| Resource | Link |
|----------|------|
| NJU 2026 OS (jyy) Bilibili | https://www.bilibili.com/video/BV1eqEA6JEZA |
| Course wiki | https://jyywiki.cn |
| Hands-on env | Linux (VM / Docker / WSL) + gcc, gdb, strace |

## Optional kernel track

BusTub (P0–P4) tasks remain for implementation depth. CMU asks students **not to publish BusTub solutions** on public GitHub — keep code in a private repo if you pursue this path.

This repo stores only learning notes, task plans, and paper/lecture cards.
