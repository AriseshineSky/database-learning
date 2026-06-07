# Task: Concurrency (O4)

**Status:** not started  
**Track:** os-engineering  
**Registry:** OS-L13–L18  
**Sync with DB:** E3 Transactions & Isolation（建议同周进行）

## Goal

掌握 pthread 级并发原语，能写正确的生产者/消费者，识别 data race / deadlock — 并与 DB 事务/锁建立类比。

## Must watch

- [ ] L13 — 多处理器编程：从入门到放弃（conceptual）
- [ ] L14 — 并发控制：互斥
- [ ] L15 — 并发控制：条件变量和万能同步方法
- [ ] L16 — 并发控制：信号量
- [ ] L17 — 并发 Bugs 和应对
- [ ] L18 — 并行算法和数据结构（conceptual）

## Must understand

- mutex 保护不变量；hold lock 时不能阻塞过久
- 条件变量：为什么需要「while 而不是 if」
- 信号量 vs mutex + cond 的等价关系
- 常见 bug：lost wakeup、ABA（了解）、死锁四条件
- 并行算法与并发控制的区别

## Hands-on

- [ ] pthread 生产者/消费者（bounded buffer）
- [ ] 故意引入 data race，用 TSAN 或逻辑推理定位
- [ ] 制造死锁，再用 lock ordering 修复
- [ ] 对照 DB：把「两个事务抢两行」画成抢两把锁

## Output

- [ ] `notes/o4-concurrency.md`
- [ ] 生产者/消费者代码片段（放 notes 或私有代码仓）
- [ ] 一张对照表：mutex ↔ row lock，deadlock ↔ DB deadlock

## DB 交叉（重点周）

- 与 E3 同步：2PL、MVCC、隔离异常 ↔ OS 锁与共享状态
- weekly review 时合写一节「并发双视角」

## Notes

<!-- Your notes here -->
