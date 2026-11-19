# README

## 这套代码出自哪门课程

本仓库是教学数据库 SimpleDB 的 Java 版本代码，源自美国波士顿学院（Boston College）Edward Sciore 教授的《Database Design and Implementation》（数据库设计与实现，第二版，Springer）一书，以及该书配套的数据库系统课程。

- 教材 / 课程：Boston College 的数据库课程教材 *Database Design and Implementation, 2nd Edition*（[Springer 书页](https://link.springer.com/book/10.1007/978-3-030-33836-7)）。全书以逐步实现一个名为 SimpleDB 的小型关系数据库为主线，讲解磁盘/文件管理、缓冲池、事务与恢复、记录与元数据管理、查询处理、SQL 解析与规划、JDBC 接口、索引等内容。
- 官方原版：SimpleDB version 3.4，由作者以 Java 源码 zip 形式发布，包含 `simpledb`（服务端）、`simpleclient`、`derbyclient` 三个包（[原版下载地址](http://www.cs.bc.edu/~sciore/simpledb/)）。原版本身就是 Java 实现的，所以本仓库并非把别的语言版本翻译成 Java。
- 本仓库做了什么：在原版 3.4 源码基础上用 Maven 重新组织工程（`org.simpledb:simpledb2`，JDK 21），为关键代码补充中文注释，并把原书 Part 3 / Part 4 的主要章节译为中文放在 `docs/` 下，同时按实现步骤整理了 `docs/step/` 笔记。仓库根目录的 [README.md](../../README.md) 有完整的功能说明与架构图。

## 关于"同名"的提醒

"SimpleDB" 这个名称也被其他数据库课程使用，最典型的是 MIT 6.830 *Database Systems* 的 Java 实验框架。它与本仓库不是同一套代码：MIT 版的结构是 `Database` / `BufferPool` / `HeapFile` / `Tuple` / `DbIterator` 等，而本仓库的包结构是 Sciore 版的 `simpledb.file` / `buffer` / `tx` / `record` / `metadata` / `query` / `parse` / `plan` / `jdbc` / `server`。阅读或检索资料时请认准作者 Edward Sciore 与书名，避免找错配套材料。

此外，社区还基于这本书移植出了其他语言版本，如 [Rust 版](https://github.com/cutsea110/simpledb) 和 [Go 版](https://github.com/tyabu12/simpledb)，本仓库对应的是其中的 Java 版本。

