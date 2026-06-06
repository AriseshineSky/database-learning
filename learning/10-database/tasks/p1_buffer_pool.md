# Task: Buffer Pool Manager (BusTub P1)

**Status:** in progress  
**Prerequisite:** P0  
**Registry:** L04, Ch 12–13, B02

## Goal

Implement in-memory page cache over disk pages: fetch, flush, pin/unpin, LRU eviction.

## Must Read

- [ ] [Lecture #04 — Memory Management](../../lectures/l04-memory-management.md)
- [ ] Textbook Ch 13.2–13.5 (Buffer pool, replacement policies)
- [ ] BusTub P1 project handout

## Must Understand

- Page vs frame vs page table
- Pin count (page cannot be evicted while pinned)
- Dirty page tracking
- LRU replacement (list + hash map)
- Disk scheduler / `DiskManager` API in BusTub

## Optional

- [ ] [PostgreSQL buffer manager blog](../../blogs/pg-buffer.md)
- [ ] CMU Lecture #03 — Database Storage I

## Watch

- CMU 15-445 Lecture #04 (YouTube playlist, Fall 2022 #04)

## Output

- [ ] `BufferPoolManager` implemented
- [ ] LRU eviction working
- [ ] All P1 tests pass

## Notes

### Key concepts

- **Page ID** = `{pool_id, page_no}` uniquely identifies a page on disk
- **Frame** = slot in buffer pool memory
- **Eviction** only when pin_count == 0

### My implementation log

<!-- date: what you did, what failed, what fixed -->
