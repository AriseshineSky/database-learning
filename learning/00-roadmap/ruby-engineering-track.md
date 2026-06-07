# Ruby Engineering Track

**Audience:** Rails 业务开发者 — 会写 Controller/Model/Service，想拆懂 Rails「魔法」。

**Goal:** 把 `has_many`、`validates`、Concern 从「框架特性」还原成普通 Ruby（对象模型、元编程、消息传递）。

**资源原则：** 只用免费公开资料，不买付费课。

**Target ceiling:** 能读 ActiveRecord 源码、手写 mini macro、用 Sandi Metz 思路重构胖 Service — 不是 gem 作者或 CRuby 贡献者。

---

## 与 DB / OS 轨的关系

| 轨 | 每周时间 | 角色 |
|----|----------|------|
| DB E1–E5 | 5–6 h | **主轨** |
| OS O1–O6 | 3–4 h | **副轨 A** |
| Ruby R1–R4 | 2 h | **副轨 B**（有余力再做，不挤压主轨） |

**原则：** Ruby 写在 `parallel-ruby.md`；DB 未完成当天重点时，Ruby 可整周跳过。

---

## 学前水平（你已具备）

- 会写 Rails CRUD、回调、Concern、Service Object
- 会用 `bundle`、`rails console`、基本调试

## 还缺什么

- `self`、 eigenclass、method lookup 直觉
- `define_method` / `method_missing` / `class_eval` 实战
- 读 `activerecord/associations/builder/` 源码
- 消息传递式 OO（vs 抽更多 private method）

---

## 免费核心资料

| 资源 | 用途 | 链接 |
|------|------|------|
| RubyMonk 存档 | 交互教程 R1 | [makandra 大纲](https://makandracards.com/curriculum/35019-advanced-ruby-metaprogramming-dsls-3d) |
| ruby-metaprogramming-tokyo | 一日工作坊 R2 | [GitHub](https://github.com/nusco/ruby-metaprogramming-tokyo) |
| metaprogramming_koans | 填空练习 R2 | [GitHub](https://github.com/sathish316/metaprogramming_koans) |
| metaprogramming-challenges | 浏览器 29 题 | [在线](https://willnet.github.io/metaprogramming-challenges-in-ruby/) |
| RubyEvents.org | Rails 拆魔法 R3 | [rubyevents.org](https://www.rubyevents.org/) |
| Sandi Metz 演讲 | OO 重构 R4 | [YouTube](https://www.youtube.com/watch?v=8bZh5LMaSmE) |
| Ruby 官方文档 | 查阅 | [docs.ruby-lang.org](https://docs.ruby-lang.org/en/master/) |

---

## 阶段时间线

| Phase | 周数 | 产出 |
|-------|------|------|
| R1 RubyMonk Ascent | 2 周 | block/self 笔记；能解释闭包 |
| R2 Metaprogramming Workshop | 2 周 | 手写 mini `belongs_to` |
| R3 Rails Internals | 2 周 | `has_many` 调用链图；读 AR 源码 |
| R4 OO Design | 2 周 | 重构一个胖 Service/Model 方法 |

**Total:** ~8 周 × 2 h/周（与 DB/OS 并行，可弹性延后）

---

## 与 DB/OS 对齐

| 周 | Ruby | DB | OS | 协同 |
|----|------|----|----|------|
| W7–8 | R4 OO + 并发直觉 | E3 事务 | O4 并发 | 锁、对象职责 |
| W9–10 | R3 收尾 + AR 连接池 | E4/E5 | O6/L27 | DB 在 Ruby 层的落点 |

---

## 动手环境

```bash
# 已有 Rails 项目即可；额外准备：
git clone https://github.com/nusco/ruby-metaprogramming-tokyo   # R2
git clone https://github.com/sathish316/metaprogramming_koans    # R2

# 读 Rails 源码
bundle open activerecord
```

笔记目录：`learning/25-ruby/notes/`
