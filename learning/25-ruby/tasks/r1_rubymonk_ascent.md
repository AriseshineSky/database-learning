# Task: RubyMonk Ascent (R1)

**Status:** not started  
**Track:** ruby-engineering  
**Registry:** RB-M1, RB-M2

## Goal

补齐 block、self、闭包直觉 — Rails 回调和 Concern 都建立在这上面。

## Must read (RubyMonk 存档)

通过 [makandra 大纲](https://makandracards.com/curriculum/35019-advanced-ruby-metaprogramming-dsls-3d) 的 archive.org 链接：

- [ ] Ruby Primer: Ascent — 全部章节
- [ ] Metaprogramming Ruby — 前半（到 method 定义之前）

每章做完：**用 IRB 复现一次课上概念**。

## Must understand

- `self` 在 instance method / class method / module 内的变化
- block 是闭包：外部局部变量在 block 内可见
- `yield` 与 `&block` 的关系
- `proc` vs `lambda` 参数检查差异（概念级）

## Hands-on

- [ ] 写一个 `Logger.around { ... }` 用 block 计时（模仿 Rails around_action 直觉）
- [ ] 在 `rails console` 里对任意 Model 查 `.methods.grep(/valid/)` 感受动态方法

## Optional

- [ ] [metaprogramming-challenges](https://willnet.github.io/metaprogramming-challenges-in-ruby/) 做 3 道基础题

## Output

- [ ] `notes/r1-rubymonk.md` — 至少 5 条可复述要点
- [ ] 能画：`class User; def foo; self; end; end` 中三处 `self` 各指什么

## Skip

- 重学 Ruby 基础语法（if/for/Array）— 你已会 Rails

## Notes

<!-- Your notes here -->
