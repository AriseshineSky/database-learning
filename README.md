# Database Learning System

Task-driven knowledge system for CMU 15-445 (Database Systems) + BusTub.

**Not a file dump.** Every material must be linked to a task.

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
├── 00-roadmap/     # roadmap + registry (single source of truth)
├── 01-now/         # ONE current task only
├── 02-backlog/     # queued tasks
├── 10-database/    # CMU 15-445 + BusTub
│   ├── tasks/      # task checklists (start here)
│   ├── papers/     # paper cards (links + your notes)
│   ├── lectures/   # lecture cards
│   ├── blogs/      # blog cards
│   └── notes/      # your summaries
├── 20-architecture/
└── 30-leetcode/
```

## Rules

1. **Only one task in `now.md`** — finish or pause before switching.
2. **New material → must link to a task** — otherwise it is dead weight.
3. **Store cards, not PDFs** — link to source + write your understanding.
4. **Status must flow:** `not started → reading → understanding → implemented → mastered`
5. **Weekly review** — use `learning/00-roadmap/weekly-review.md`

## Course resources

| Resource | Link |
|----------|------|
| CMU 15-445 (Fall 2025) | https://15445.courses.cs.cmu.edu/fall2025/ |
| Course schedule + per-lecture videos | https://15445.courses.cs.cmu.edu/fall2025/schedule.html |
| BusTub (do NOT fork publicly) | https://github.com/cmu-db/bustub |
| Textbook | Database System Concepts, 7th ed. (Silberschatz) |
| Lectures (YouTube, Fall 2025) | https://www.youtube.com/playlist?list=PLSE8ODhjZXjYMAgsGH-GtY5rJYZ6zjsd5 |

## BusTub warning

CMU asks students **not to publish BusTub solutions** on public GitHub. This repo stores only:

- learning notes
- task plans
- paper/lecture cards
- your own understanding

Keep your BusTub code in a **private** repo.
