# Task: OS Foundations (O1)

**Status:** not started  
**Track:** os-engineering  
**Registry:** OS-L01–L04

## Goal

建立操作系统的心智模型：从应用和硬件两个视角理解 OS 的角色，为后续进程/内存/并发打地基。

## Must watch

- [ ] L01 — Agentic AI 时代的操作系统课：绪论
- [ ] L02 — 应用视角的操作系统
- [ ] L03 — 硬件视角的操作系统

## Skim / optional

- [ ] L04 — (Aside) LLM, Agents 和 Scaling Law

## Must understand

- OS 作为抽象层：向上提供什么（进程、文件、内存），向下管理什么（CPU、设备）
- 应用视角：系统调用是边界，不是「直接操作硬件」
- 硬件视角：中断、特权级、MMU 的直觉（不必实现）
- 本课与经典 OS 课（xv6/OSTEP）的定位差异

## Hands-on

- [ ] 画一张四层图：Application → libc → Kernel → Hardware
- [ ] 列出你日常用的 5 个「应用」，各自依赖哪些 OS 抽象

## Output

- [ ] `notes/o1-foundations.md` — 3+ 可复述要点
- [ ] 能回答：「为什么需要操作系统？」用 2 分钟口述

## DB 交叉（预习）

- 页（page）概念将在 E1 出现 — 记下 L03 里与内存相关的表述，E1 时对照

## Notes

<!-- Your notes here -->
