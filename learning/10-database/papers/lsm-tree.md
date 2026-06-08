# The Log-Structured Merge-Tree (LSM-Tree)

**Authors:** O'Neil, Cheng, Gawlick, O'Neil (1996)  
**Status:** not started  
**Link:** https://www.cs.umb.edu/~poneil/lsmtree.pdf

## Why it matters

- Explains write-optimized storage used by RocksDB, LevelDB, Cassandra, and many analytics systems
- Contrasts with B+Tree: LSM favors write throughput; B+Tree favors read latency and range scans
- Helps you reason about when PostgreSQL (B+Tree) vs embedded KV stores (LSM) fit

## Used in

- [e5_recovery_and_postgresql](../tasks/e5_recovery_and_postgresql.md) — capstone context

## Read when

After E1 (B+Tree) and E4 (optimizer). One of the **three required papers** for the engineering track.

## Key takeaways

<!-- Fill after reading -->

- LSM = append writes to memtable → flush sorted runs → periodic compaction
- Reads may touch multiple levels → read amplification
- Writes are sequential → high ingest throughput
- B+Tree: in-place updates, better point/range read latency

## My notes

<!-- Your understanding -->
