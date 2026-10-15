<!-- Generated from agent-kit; content 5.1.3. Edit canonical sources, then run node scripts/build-agent-kit.mjs. -->

# 共同创作核心与分发内容

> 最近一次公开发布：插件与创作内容 **5.1.3**（2026-10-15，GitHub 本仓库）；本地 MCP 包为 npm `noumi-mcp@5.1.1`。已安装的副本不会自动更新，以宿主里实际显示的版本为准；发布不等于每个宿主都已实测通过，实测范围见兼容性记录。

公开分发基线：[2081f10222a8db6be3c1ec2710d11d13e111dd7a](https://github.com/xieyb2012-netizen/noumi-plugins/tree/2081f10222a8db6be3c1ec2710d11d13e111dd7a)。两个 marketplace、安装目录与 HTTP MCP 声明保留。

网站指南、六份网站参考、Codex create-music、Claude song 及按需参考来自同一套 agent-kit 核心。Claude songwriting、setup、status 只表达任务和宿主差异。现场工具 schema 与 runtime capabilities 优先于打包快照。README、接入规则和安装教程由生成器按统一连接口径输出。

生成器在业务源仓库的 scripts/build-agent-kit.mjs，输入 agent-kit/manifest.json、agent-kit/skills/create-music/SKILL.md、references/*.md，以及经 Git blob 哈希校验的公开分发基线快照。它只使用 Node 内置模块，输出 public 指南和本完整目录，不联网、不安装、不调用音乐服务或 Git。

`--check` 在内存重建并比较文件，缺失、改动或多余分发文件均报漂移，不改文件。输出包含 distribution-manifest.json，用于检查版本、发布状态和材料哈希；它不是宿主安装证明，也不是生产发布记录。
