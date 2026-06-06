# Database Learning System

Task-driven knowledge system for CMU 15-445 — tuned for **backend engineers** who want to use databases better, not build database kernels.

**Not a file dump.** Every material must be linked to a task.

## Who this is for

You want Staff-level database fluency: complex SQL, schema design, index tuning, transaction debugging, and scale decisions — without implementing buffer pools or lock managers.

Read the full philosophy: [learning/00-roadmap/engineering-track.md](learning/00-roadmap/engineering-track.md)

## Daily workflow

```bash
# 1. What to do today
cat learning/01-now/now.md

# 2. Find materials for the task
cat learning/00-roadmap/registry.md

# 3. Execute the task checklist
cat learning/10-database/tasks/<task>.md
```

## Structure

```
learning/
├── 00-roadmap/     # roadmap, registry, engineering-track.md
├── 01-now/         # ONE current task only
├── 02-backlog/     # queued tasks (engineering + optional kernel)
├── 10-database/    # CMU 15-445
│   ├── tasks/      # e1–e5 engineering tasks (start here)
│   ├── papers/     # paper cards (links + your notes)
│   ├── lectures/   # lecture cards
│   ├── blogs/      # blog cards
│   └── notes/      # EXPLAIN examples, playbooks, case studies
├── 20-architecture/
└── 30-leetcode/
```

## Rules

1. **Only one task in `now.md`** — finish or pause before switching.
2. **New material → must link to a task** — otherwise it is dead weight.
3. **Store cards, not PDFs** — link to source + write your understanding.
4. **Status must flow:** `not started → reading → understanding → mastered`
5. **Hands-on = PostgreSQL + EXPLAIN** — not BusTub coding (unless kernel track).
6. **Weekly review** — use `learning/00-roadmap/weekly-review.md`

## Course resources

| Resource | Link |
|----------|------|
| CMU 15-445 (Fall 2025) | https://15445.courses.cs.cmu.edu/fall2025/ |
| Course schedule + per-lecture videos | https://15445.courses.cs.cmu.edu/fall2025/schedule.html |
| Textbook | Database System Concepts, 7th ed. (Silberschatz) |
| Lectures (YouTube, Fall 2025) | https://www.youtube.com/playlist?list=PLSE8ODhjZXjYMAgsGH-GtY5rJYZ6zjsd5 |
| Hands-on DB | PostgreSQL (local or Docker) |

## Optional kernel track

BusTub (P0–P4) tasks remain for implementation depth. CMU asks students **not to publish BusTub solutions** on public GitHub — keep code in a private repo if you pursue this path.

This repo stores only learning notes, task plans, and paper/lecture cards.
