# Volcano — An Extensible and Parallel Query Evaluation System

**Authors:** Goetz Graefe (1990)  
**Status:** not started  
**Link:** https://dl.acm.org/doi/10.1145/56604.56606  
**PDF (mirror):** https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=10.1.1.132.8176

## Why it matters

- Defines the **iterator / volcano model** used by almost every relational DBMS
- Each operator implements `open → next → close`
- Enables composable query plans as operator trees

## Used in

- [p3_query_execution](../tasks/p3_query_execution.md)
- BusTub P3 executors

## Read when

After Lecture #13, **before** implementing P3.

## Key takeaways

<!-- Fill after reading -->

- Iterator interface separates operators from storage
- Pipelining: parent pulls tuples from child via `next()`
- Volcano enables extensibility — add new operators without changing framework

## My notes

<!-- Your understanding, diagrams, questions -->
