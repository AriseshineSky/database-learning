# Task: Metaprogramming Workshop (R2)

**Status:** not started  
**Track:** ruby-engineering  
**Registry:** RB-M3, RB-W1, RB-K1, RB-C1, RB-G1

## Goal

掌握对象模型与元编程原语 — 能手写 mini `belongs_to`，不再把 `define_method` 当黑魔法。

## Must do

- [ ] Clone [ruby-metaprogramming-tokyo](https://github.com/nusco/ruby-metaprogramming-tokyo)，完成 5 个 module 练习
- [ ] RubyMonk **Metaprogramming Ruby: Ascent** 全部章节
- [ ] [metaprogramming_koans](https://github.com/sathish316/metaprogramming_koans) — `rake` 跑到 `about_define_method` 过关

## Must understand

- eigenclass（singleton class）与 `class << self`
- `define_method` vs `def`；`method_missing` + `respond_to_missing?`
- `class_eval` / `instance_eval` 各自改变什么 `self`
- `send` / `public_send` 动态派发

## Hands-on

- [ ] 实现 mini `belongs_to :author`：`define_method` 生成 reader/writer
- [ ] 实现 `Trackable` concern：用 `included do` + `class_eval` 加 class method
- [ ] [metaprogramming-challenges](https://willnet.github.io/metaprogramming-challenges-in-ruby/) 完成 10 题

## Reference (skim)

- [ ] [Metaprogramming Guide Gist](https://gist.github.com/jamesyang124/9216074) — 当速查表

## Output

- [ ] `notes/r2-metaprogramming.md`
- [ ] `notes/r2-mini-belongs-to.rb` 片段（可放 notes，或私有代码仓）
- [ ] 能向同事解释：为什么 `method_missing` 必须配 `respond_to_missing?`

## DB/OS 交叉

- `define_method` 批量生成方法 ↔ DB schema migration 后动态 API（概念类比）
- Ruby GIL / `Mutex` ↔ OS O4（R3/R4 时再对照）

## Notes

<!-- Your notes here -->
