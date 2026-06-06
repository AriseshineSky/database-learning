# Paper: Serializable Isolation for Snapshot Databases

**Status:** not started  
**Depth:** conceptual (engineering track)  
**Link:** https://www.postgresql.org/docs/current/transaction-iso.html (Postgres SSI docs) + original paper if linked from CMU reading list

## Why it matters (engineering)

- Explains why PostgreSQL **Serializable** can abort transactions
- Snapshot isolation alone is not serializable — write skew remains
- SSI adds detection overhead — you choose isolation level with eyes open

## Used in

- [e3_transactions_and_isolation](../tasks/e3_transactions_and_isolation.md)

## What to remember

- SI prevents dirty read / non-repeatable read but **not** all serializable anomalies
- Serializable in Postgres uses SSI — expect retries in application code
- You do **not** need to implement SSI

## My notes

<!-- -->
