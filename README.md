# Systems Learning System

Task-driven knowledge system for **Rails / Java / Go backend engineers**:

- **DB primary track** — CMU 15-445 (selected lectures): indexes, EXPLAIN, transactions, MVCC, optimizer — not kernel development
- **OS parallel A** — [NJU 2026 操作系统原理](https://www.bilibili.com/video/BV1eqEA6JEZA)（蒋炎岩 / jyy）
- **Ruby parallel B** — Rails advanced topics, all free resources (demystify magic, metaprogramming, OO design)

**Not a file dump.** Every material must be linked to a task.

## Who this is for

You want advanced backend fluency: read EXPLAIN, design indexes, debug transactions, tune PostgreSQL — without building database kernels or publishing papers.

**Target:** Database knowledge > 95% of application developers, < database kernel engineers.

Read track philosophies:

- [DB engineering track](learning/00-roadmap/engineering-track.md)
- [OS engineering track](learning/00-roadmap/os-engineering-track.md)
- [Ruby engineering track](learning/00-roadmap/ruby-engineering-track.md)

## Daily workflow

```bash
# 1. 今天主任务（DB）
cat learning/01-now/now.md

# 2. 主任务完成后 — 副轨
cat learning/01-now/parallel.md        # OS（优先）
cat learning/01-now/parallel-ruby.md   # Ruby（有余力）

# 3. 查资料 registry
cat learning/00-roadmap/registry.md

# 4. 三轨时间表
cat learning/00-roadmap/master-schedule.md

# 5. 执行 checklist
cat learning/10-database/tasks/<task>.md
cat learning/15-operating-systems/tasks/<task>.md
cat learning/25-ruby/tasks/<task>.md
```

## Structure

```
learning/
├── 00-roadmap/
│   ├── engineering-track.md      # DB
│   ├── os-engineering-track.md   # OS
│   ├── ruby-engineering-track.md # Ruby
│   ├── master-schedule.md        # 三轨对齐
│   └── registry.md
├── 01-now/
│   ├── now.md            # 主任务（DB）
│   ├── parallel.md       # 副轨 A（OS）
│   └── parallel-ruby.md  # 副轨 B（Ruby）
├── 02-backlog/
├── 10-database/          # CMU 15-445
├── 15-operating-systems/ # NJU OS (jyy)
├── 25-ruby/              # Rails 进阶（免费资料）
│   ├── tasks/            # r1–r4
│   ├── talks/            # 演讲卡片
│   └── notes/
├── 20-architecture/
└── 30-leetcode/
```

## Rules

1. **Only one primary task in `now.md`** — OS / Ruby 放 parallel 文件，主轨完成后再做。
2. **Priority:** DB > OS > Ruby > LeetCode.
3. **New material → must link to a task** — otherwise it is dead weight.
4. **Store cards, not PDFs** — link to source + write your understanding.
5. **Status must flow:** `not started → reading → understanding → mastered`
6. **Weekly review** — `learning/00-roadmap/weekly-review.md`

## Course resources

### Database (primary)

| Resource | Link |
|----------|------|
| CMU 15-445 (Fall 2025) | https://15445.courses.cs.cmu.edu/fall2025/ |
| Lectures (YouTube) | https://www.youtube.com/playlist?list=PLSE8ODhjZXjYMAgsGH-GtY5rJYZ6zjsd5 |
| Hands-on | PostgreSQL |

### Operating Systems (parallel A)

| Resource | Link |
|----------|------|
| NJU 2026 OS (jyy) | https://www.bilibili.com/video/BV1eqEA6JEZA |
| Course wiki | https://jyywiki.cn |

### Ruby (parallel B, all free)

| Resource | Link |
|----------|------|
| RubyMonk 存档 | via [makandra curriculum](https://makandracards.com/curriculum/35019-advanced-ruby-metaprogramming-dsls-3d) |
| Paolo workshop | https://github.com/nusco/ruby-metaprogramming-tokyo |
| Metaprogramming koans | https://github.com/sathish316/metaprogramming_koans |
| Browser challenges | https://willnet.github.io/metaprogramming-challenges-in-ruby/ |
| Conference talks | https://www.rubyevents.org/ |

## Optional kernel track

BusTub (P0–P4) tasks remain for DB implementation depth. Keep BusTub **code in a private repo** — CMU discourages public solutions.

This repo stores only learning notes, task plans, and material cards.
