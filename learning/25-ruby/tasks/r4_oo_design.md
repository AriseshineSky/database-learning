# Task: OO Design (R4)

**Status:** not started  
**Track:** ruby-engineering  
**Registry:** RB-T4, RB-T5, RB-T6  
**Sync with:** DB E3 + OS O4（建议 W7–8 对齐）

## Goal

用消息传递式 OO 重构自己的 Rails 代码 — 减少胖 Model、神秘 Service、长条件分支。

## Must watch

- [ ] [All the Little Things](https://www.youtube.com/watch?v=8bZh5LMaSmE) — Sandi Metz
- [ ] [Nothing is Something](https://www.youtube.com/watch?v=OMPfEXIlTVE)
- [ ] [Polly Want a Message](https://www.youtube.com/watch?v=XXi_FBrZQiU)

## Must understand

- 对象通过**消息**协作，不是共享大量状态
- 用多态替代 `case` / `if type ==`
- Null Object、单一职责、组合优于继承
- 「简单代码」≠ 少文件，而是**易改**

## Hands-on（用自己项目）

- [ ] 选一个 80+ 行的 Service 或 Model 方法
- [ ] 列出它响应的「消息」和依赖的「知识」
- [ ] 拆成 2–3 个小对象（Plain Old Ruby Object，不必上 gem）
- [ ] 写最少测试证明行为不变

## Output

- [ ] `notes/r4-oo-refactor.md` — before/after 对比 + 拆对象理由
- [ ] 能口述：为什么 `case order.status` 往往是设计气味

## DB/OS 交叉

- 小对象边界 ↔ 事务边界（哪些操作应在同一 transaction）
- 对象间消息 ↔ 进程间通信直觉（OS O2，概念级）

## Skip

- 购买 POOD-I 付费课 — 三个免费演讲 + 自己代码练习已够

## Notes

<!-- Your notes here -->
