# Task: Runtime & Linking (O3)

**Status:** not started  
**Track:** os-engineering  
**Registry:** OS-L09–L12

## Goal

理解 C 程序如何从源码变成可运行进程：libc、动态链接、加载 — 能 debug 一次 `malloc` 调用链。

## Must watch

- [ ] L09 — C 标准库原理
- [ ] L10 — 调试 C 标准库
- [ ] L11 — 链接和加载
- [ ] L12 — 从零开始构建 Linux 应用世界

## Must understand

- libc 介于应用与内核之间：哪些走 syscall，哪些纯用户态
- 静态链接 vs 动态链接；`ld.so` 的角色
- ELF 大致结构（不必背偏移）：代码段、数据段、符号表
- 「从零构建应用世界」在讲什么依赖链（编译器、libc、启动文件）

## Hands-on

- [ ] `gdb` 单步进入 `malloc` 或 `printf`（L10 跟做）
- [ ] `ldd ./a.out` 看动态库依赖
- [ ] `readelf -h -l ./a.out` 或 `objdump -d` 扫一眼
- [ ] 按 L12 思路，用最简工具链编译一个不用 libc 的 hello（可选挑战）

## Output

- [ ] `notes/o3-runtime-linking.md`
- [ ] 能画：源码 → 目标文件 → 可执行文件 → 进程 的流程
- [ ] 记录一次 gdb 调试 libc 的步骤（可截图）

## Notes

<!-- Your notes here -->
