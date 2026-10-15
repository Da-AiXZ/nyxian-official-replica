# nyxian-official-replica

审计实验仓：**官方 emexlab/Nyxian 构建流程原样复刻**。

- 本仓不含任何 Nyxian 源码副本——workflow 直接 checkout 官方仓 `emexlab/Nyxian`（官方绿跑 commit `0587c30`，可切换 ref）+ recursive submodules。
- 构建步骤逐字照抄官方 build.yml：`brew install ldid dpkg libarchive` → `CHECK_DEPS=0 make all` → 上传 `Nyxian.ipa`。
- 无缓存、无修补、无自研合并、无输出截断；完整日志由 GitHub Actions 全量保留。
- 对照基准：官方绿跑 run `36919965048`（2026-10-01，Nyxian.ipa = 112,522,815 bytes，SHA256 `7451b54d…`）。

Nyxian 源码许可证：AGPL-3.0-or-later（本仓仅引用官方仓构建，不修改、不再分发源码）。
