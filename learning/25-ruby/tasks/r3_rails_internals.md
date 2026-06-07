# Task: Rails Internals (R3)

**Status:** not started  
**Track:** ruby-engineering  
**Registry:** RB-T1, RB-T2, RB-T3

## Goal

拆懂 `has_many`、`validates`、Concern — 从宏调用跟到真正执行的 Ruby 代码。

## Must watch

- [ ] [Reflecting on Active Record Associations](https://www.rubyevents.org/talks/reflecting-on-active-record-associations) — 手写 has_many/belongs_to
- [ ] [Rails on Ruby: How Ruby Makes Rails Great](https://www.rubyevents.org/talks/rails-on-ruby-how-ruby-makes-rails-great)
- [ ] [In Defense of Ruby Metaprogramming](https://www.rubyevents.org/talks/in-defense-of-ruby-metaprogramming)

## Must read (源码)

在你当前 Rails 项目的 gem 路径：

- [ ] `bundle open activerecord` → `lib/active_record/associations/builder/has_many.rb`
- [ ] `lib/active_model/validations.rb` — `validates` 入口
- [ ] 任选一个项目 Concern，trace `included` 钩子

## Must understand

- `has_many` 是 class macro：在 class body 执行时动态定义方法
- `CollectionProxy` 为何能链式调用
- `validates` 如何注册 callback / validation 对象
- 何时该用元编程 vs 显式代码（Noel Rappin 演讲要点）

## Hands-on

- [ ] 画一张图：`User.has_many :posts` 从宏到 `user.posts` 的调用链
- [ ] 对照演讲，给现有 Model 加一个简化版 `has_many`（练习用，不必投产）
- [ ] `rails console`：`User.reflect_on_association(:posts)` 看元数据

## Output

- [ ] `notes/r3-rails-internals.md` — 含 has_many 调用链图
- [ ] `notes/r3-validates-chain.md` — validates 链路 5 步以内

## DB 交叉

- ActiveRecord 连接池、`transaction` block ↔ DB E3 事务隔离
- `insert` / `update` SQL 生成 ↔ DB E1 索引设计

## Notes

<!-- Your notes here -->
