# Task: Process & Memory (O2)

**Status:** not started  
**Track:** os-engineering  
**Registry:** OS-L05–L08

## Goal

理解进程生命周期、地址空间、文件描述符 — 能 trace 一次 `fork` + `execve`，解释 mmap 做了什么。

## Must watch

- [ ] L05 — 程序和进程；fork, execve, exit
- [ ] L06 — 进程的地址空间；mmap, munmap, mprotect
- [ ] L07 — 访问操作系统对象；文件描述符
- [ ] L08 — (Aside) 终端和 UNIX Shell

## Must understand

- `fork` 后父子进程各自有什么（代码、堆、fd 表）
- `execve` 替换的是什么
- 虚拟地址空间 vs 物理内存；mmap 映射文件 vs 匿名映射
- fd 是统一抽象：文件、socket、pipe 都是 fd
- Shell 管道、重定向如何对应 fd 操作

## Hands-on

- [ ] `strace -f ./your_program` 观察 fork/execve（Linux）
- [ ] 写最小 C 程序：`fork` 后父子各 `write` 不同消息
- [ ] `mmap` 映射一个小文件，修改后 `msync` 或观察行为
- [ ] Shell 实验：`ls | wc -l`、`cmd > file 2>&1` 各做了什么

## Output

- [ ] `notes/o2-process-memory.md`
- [ ] 1 份 strace 截图或日志 + 5 行解读
- [ ] 能解释：为什么多进程服务比多线程更容易隔离故障

## DB 交叉

- mmap + page cache ↔ DB buffer pool 行为（E1 conceptual）

## Notes

<!-- Your notes here -->
