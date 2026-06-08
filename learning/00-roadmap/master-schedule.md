# Master Schedule — DB + OS + Ruby

**Start date:** 2026-06-06  
**Mode:** DB primary + OS parallel A + Ruby parallel B (see `parallel.md` / `parallel-ruby.md`)

---

## Time budget

| Week | DB (primary) | OS (parallel A) | Ruby (parallel B) | Total |
|------|--------------|-----------------|-------------------|-------|
| Typical | 5–6 h | 3–4 h | 0–2 h | 8–12 h |
| Busy | 5–6 h | 1–2 h | 0 h | 6–8 h |

**Priority on conflict:** DB > OS > Ruby > LeetCode

---

## Phase alignment

```
Week    DB track                    OS track              Ruby track            Sync point
─────────────────────────────────────────────────────────────────────────────────────────
W1–2    E1 B+Tree & Indexes         O1 Foundations        R1 RubyMonk           pages / self
W3      E2 Query Execution          O2 Process/Memory     R2 Metaprogramming    dynamic dispatch
W4–5    E3 Transactions & MVCC ★    O3 Runtime/Linking    R3 Rails Internals    AR / SQL
W6      E4 Query Optimizer          O4 Concurrency ★      R4 OO Design          locks / objects
W7      E5 Recovery + PG capstone   O6 I/O & FS ★         R3 wrap-up            WAL / system map
```

★ = intentional cross-track sync week (compare notes in weekly review)

---

## Current status (2026-06-06)

| Track | Current task | Status |
|-------|--------------|--------|
| DB | E1 B+Tree & Indexes | in progress |
| OS | O1 Foundations | not started |
| Ruby | R1 RubyMonk Ascent | not started |

---

## Weekly rhythm (template)

| Day | DB (primary) | OS (parallel A) | Ruby (parallel B) |
|-----|--------------|-----------------|-------------------|
| Mon | CMU lecture + EXPLAIN ANALYZE | — | — |
| Tue | — | jyy lecture + notes | — |
| Wed | Textbook Ch 14–18 / papers | — | RubyMonk 1 chapter |
| Thu | — | jyy or lab | — |
| Fri | Hard topic review | strace/gdb | koans / source |
| Sun | **weekly review** | registry + backlog | |

**Minimum progress:** 1 DB milestone + 2 OS lectures per week; Ruby skippable.

---

## Decision rules

1. **Protect the primary track** — if DB is behind, OS stays at 1 lecture/week; Ruby can skip a week.
2. **E3 is non-negotiable** — Transactions & MVCC gets extra time; don't rush it.
3. **Sync weeks matter** — W4–W7 cross-track alignment; use weekly review to connect notes.
4. **L27 is the OS↔DB milestone** — mark OS prerequisite for E3–E5 complete after O6.
5. **R3↔E3** — read ActiveRecord transaction code alongside isolation level notes.
6. **One output per session** — each track: 3 notes OR 1 small experiment minimum.

---

## Definition of done

### DB track
- E1–E5 output checklists complete
- 3 papers read (Isolation Levels, SSI, LSM-Tree)
- PostgreSQL capstone: EXPLAIN fluency + VACUUM/MVCC checklist

### OS track
- O1–O6 complete; `15-operating-systems/notes/` ≥ 15 bullet points

### Ruby track
- R1–R4 complete; `25-ruby/notes/` includes mini `belongs_to` + has_many chain diagram + one OO refactor log
