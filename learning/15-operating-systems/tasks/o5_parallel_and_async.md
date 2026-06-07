# Task: Parallel & Async (O5)

**Status:** not started  
**Track:** os-engineering  
**Registry:** OS-L19–L21

## Goal

理解协程/Goroutine/异步模型与多线程的差异；建立 SIMD/GPU 概念；LLM Token 旅程可选。

## Must watch

- [ ] L19 — 协程、Goroutine、异步编程

## Conceptual / skim

- [ ] L20 — CPU、SIMD 和 GPU
- [ ] L21 — 一个 Token 的旅程（兴趣驱动）

## Must understand

- 协程：用户态切换、无抢占（典型模型）
- async/await 解决的是什么问题（回调地狱、并发 I/O）
- Goroutine + channel 与 mutex 的风格差异
- GPU 适合数据并行；与 CPU 分支密集任务的分工

## Hands-on

- [ ] 用一门熟悉语言写一个简单的 async I/O 或 goroutine demo（Go 优先）
- [ ] 对比：同样逻辑用 thread vs goroutine 的资源占用直觉

## Output

- [ ] `notes/o5-parallel-async.md`
- [ ] 能解释：为什么高并发网关常用 async 而不是「一请求一线程」

## Notes

<!-- Your notes here -->
