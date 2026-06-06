# ARIES: A Transaction Recovery Method

**Authors:** Mohan, Haderle, Lindsay, Pirahesh, Schwarz (1992)  
**Status:** not started  
**Link:** https://people.eecs.berkeley.edu/~brewer/cs262/Aries.pdf

## Why it matters

- Industry-standard crash recovery algorithm (DB2, PostgreSQL WAL concepts)
- Introduces **repeating history** during redo
- Handles steal/no-force, fuzzy checkpoints, nested rollback

## Used in

- [recovery_study](../tasks/recovery_study.md)
- CMU Lectures #22–#23

## Read when

After finishing P4, during recovery study week.

## Key takeaways

<!-- Fill after reading -->

- **Analysis:** scan WAL → build ATT (active txns) + DPT (dirty pages)
- **Redo:** repeat all history from earliest needed LSN (even loser txns)
- **Undo:** rollback uncommitted transactions
- Every page has a **pageLSN** linking page state to log

## My notes

<!-- Your understanding -->
