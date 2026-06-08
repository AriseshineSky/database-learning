# Task: Architecture & Scale (Optional)

**Status:** not started  
**Track:** optional — skip unless you need distributed/scale depth  
**Prerequisite:** e5_recovery_and_postgresql  
**Registry:** L23–L24, P03 (Architecture paper)

> **Note:** Not required for the engineering track. Complete [e5_recovery_and_postgresql.md](./e5_recovery_and_postgresql.md) first.

## Goal

Map database internals to real systems: replication, sharding, read models — and finish with a full-system mental model.

## Must watch

- [ ] Lecture #23 — Distributed OLTP (skim consensus details)
- [ ] Lecture #24 — Distributed OLAP / column stores (optional)

## Must read

- [ ] [Architecture of a Database System](../papers/architecture.md) ← **capstone**
- [ ] Textbook Ch 22–23 (overview: replication, partitioning — selective)

## Must understand

- How Postgres / MySQL map to: storage, buffer cache, planner, executor, WAL
- Read replica lag — what is and isn't guaranteed
- Sharding vs partitioning — when each applies
- CQRS / read models as engineering pattern (not DB internals)
- CAP at practitioner level (not proof level)

## Hands-on

- [ ] Draw your current (or a sample) backend on top of DB components
- [ ] Document one sharding or partition decision for a hypothetical 100M-row table

## Output

- [ ] Architecture paper status → `understanding`
- [ ] System design note in `20-architecture/` linking course concepts to your experience

## Skip

- Distributed transaction protocol papers
- Consensus implementation (Raft/Paxos coding)
- New storage engine design papers

## Notes

<!-- Your notes here -->
