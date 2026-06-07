# Master Schedule — DB + OS + Ruby

**起始日：** 2026-06-06  
**模式：** 主轨 DB + 副轨 OS + 副轨 Ruby（见 `parallel.md` / `parallel-ruby.md`）

---

## 时间预算

| 周 | DB（主） | OS（副 A） | Ruby（副 B） | 合计 |
|----|----------|------------|--------------|------|
| 典型周 | 5–6 h | 3–4 h | 0–2 h | 8–12 h |
| 忙碌周 | 5–6 h | 1–2 h | 0 h | 6–8 h |

**冲突优先级：** DB > OS > Ruby > LeetCode

---

## 阶段对齐

```
周次    DB 轨                 OS 轨                 Ruby 轨               协同点
──────────────────────────────────────────────────────────────────────────────────
W1–2    E1 Storage            O1 Foundations        R1 RubyMonk           页 / self
W3–4    E1→E2 Query           O2 Process/Memory     R2 Metaprogramming    动态方法
W5–6    E2 Query              O3 Runtime/Linking     R3 Rails Internals    AR / SQL
W7–8    E3 Transactions ★     O4 Concurrency ★      R4 OO Design ★        锁 / 对象
W9      E4 Recovery ★         O6 I/O & FS ★         R3 收尾               WAL
W10     E5 Architecture       O6 L27 DB bridge ★    —                     系统闭合
```

★ = 三轨刻意对齐周（weekly review 对照笔记）

---

## 当前状态（2026-06-06）

| 轨 | 当前任务 | 状态 |
|----|----------|------|
| DB | E1 Storage & Indexes | in progress |
| OS | O1 Foundations | not started |
| Ruby | R1 RubyMonk Ascent | not started |

---

## 每周节奏（模板）

| 天 | DB（主） | OS（副 A） | Ruby（副 B） |
|----|----------|------------|--------------|
| Mon | CMU lecture + EXPLAIN | — | — |
| Tue | — | jyy lecture + 笔记 | — |
| Wed | 教材 / 论文 | — | RubyMonk 1 章 |
| Thu | — | jyy 或实验 | — |
| Fri | 难点补课 | strace/gdb | koans / 源码 |
| Sun | **weekly review** | registry + backlog | |

**最低进度：** 每周 1 个 DB 里程碑 + 2 集 OS；Ruby 可跳过。

---

## 决策规则

1. **冲突时保主轨** — DB 未完成，OS 维持 1 集/周，Ruby 可整周跳过。
2. **汇合周不可跳过** — W7–10 双轨/三轨对齐尽量遵守。
3. **L27 是 OS↔DB 里程碑** — 完成后标记 E3–E5 OS 先修。
4. **R3↔E3** — 读 AR 事务代码时对照 DB 隔离级别笔记。
5. **一课一输出** — 每轨至少：3 条笔记 OR 1 个小实验。

---

## 完成定义

### DB 轨
- E1–E5 各任务 Output checklist 全勾

### OS 轨
- O1–O6 全勾；`15-operating-systems/notes/` ≥ 15 条要点

### Ruby 轨
- R1–R4 全勾；`25-ruby/notes/` 含 mini `belongs_to` + has_many 链路图 + 一次 OO 重构记录
