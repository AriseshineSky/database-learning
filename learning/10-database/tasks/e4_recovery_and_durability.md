# Task: Recovery & Durability (Engineering)

**Status:** not started  
**Track:** engineering  
**Prerequisite:** e3_transactions_and_isolation  
**Registry:** L21–L22, Ch 19, P02 (ARIES — skim)

## Goal

Understand durability guarantees and recovery at the whiteboard level — enough to reason about fsync, WAL, and crash safety in ops conversations.

## Must watch

- [ ] Lecture #21 — Database Logging
- [ ] Lecture #22 — Database Recovery (**conceptual** — skip algorithm tracing)

## Must read

- [ ] Textbook Ch 19.1–19.4 (WAL, checkpoint, steal/no-force **concepts**)
- [ ] [ARIES paper](../papers/aries.md) — skim: three phases and **why**, not LSN math

## Must understand

- WAL rule: log before page write
- Why `commit` ≠ "on disk" until WAL fsync
- Checkpoint purpose (recovery time, not durability magic)
- STEAL / NO-FORCE — what they mean for performance vs recovery
- ARIES: Analysis → Redo → Undo (one sentence each)

## Hands-on (PostgreSQL)

- [ ] Read Postgres docs on `synchronous_commit`, `wal_level`, replication lag
- [ ] Optional: compare `commit` latency with sync on vs off (local dev only)

## Output

- [ ] One-page "durability cheat sheet" for your stack
- [ ] Can explain crash recovery to a teammate in 2 minutes

## Skip

- ARIES homework-level detail
- Implementing log manager or recovery
- BusTub recovery code

## Notes

<!-- Your notes here -->
