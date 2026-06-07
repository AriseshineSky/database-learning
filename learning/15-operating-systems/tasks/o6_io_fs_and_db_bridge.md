# Task: I/O, Filesystem & DB Bridge (O6)

**Status:** not started  
**Track:** os-engineering  
**Registry:** OS-L22–L27  
**Sync with DB:** E4 Recovery + E5 Architecture（建议对齐）

## Goal

理解 I/O 栈、存储设备、文件系统 API 与崩溃一致性；**L27 与 DB 轨汇合** — 把 OS 层动机与 DB 层实现连起来。

## Must watch

- [ ] L22 — 输入输出设备和驱动（conceptual）
- [ ] L23 — 存储设备原理
- [ ] L24 — 文件系统 API (1)
- [ ] L25 — 文件系统 API (2)
- [ ] L26 — 文件系统实现和崩溃一致性
- [ ] L27 — 数据库系统 ★

## Must understand

- 块设备 vs 字符设备；驱动的大致位置
- 顺序写 vs 随机写；为什么 DB 关心 WAL 顺序写
- VFS、inode、dentry 直觉
- 崩溃一致性：journal、fsync、ordering
- L27 如何把文件系统/存储栈接到数据库抽象

## Hands-on

- [ ] `dd` / `iostat` 观察顺序写 vs 随机写（可选）
- [ ] 实验：`write` 后 `fsync` vs 不 fsync 的差异（文档化）
- [ ] 对照 DB E4：画 WAL ↔ FS journal 类比图

## Output

- [ ] `notes/o6-io-fs-db-bridge.md`
- [ ] `notes/db-os-bridge.md` — L27 + E4/E5 联合总结（本轨毕业产出）
- [ ] 能向同事解释：为什么 PostgreSQL 强调 `fsync` 和 WAL

## DB 交叉（毕业周）

- L26 ↔ E4 ARIES / WAL
- L27 ↔ E5 Architecture of a Database System
- 完成后在 registry 标记 OS 轨 `mastered`

## Notes

<!-- Your notes here -->
