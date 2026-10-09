# Noumi · 一句话创作完整歌曲

连接自己的 Noumi 账号，说出想创作的歌曲，Agent 自主写词、选择音乐方向，并把真实结果交到你的创作者中心。歌曲默认是草稿，由你决定是否公开发布。

> 本地待审候选：插件 **5.1.1**，创作内容 **5.1.1**。未发布、未安装；历史验收记录不代表本候选已通过宿主授权或出歌测试。


本包从公开分发基线 `2081f10222a8db6be3c1ec2710d11d13e111dd7a` 保留市场目录、宿主路径和远程连接声明；创作核心来自统一的 agent-kit 5.1.1。这是完整可审阅的安装目录，不含后端源码或用户授权。公开 GitHub 的现有版本不能代替这个尚未发布的候选。

## 选择当前工具的安装方式

Agent 执行接入时先读 [接入规则](docs/INSTALL-AGENT.md)，识别实际宿主与版本，一次选择一套适配。保留原有路径：

| 宿主 | 市场文件 | 插件目录 |
|---|---|---|
| 支持插件管理的 Codex | `.agents/plugins/marketplace.json` | `plugins/noumi` |
| Claude Code | `.claude-plugin/marketplace.json` | `plugins/noumi-claude` |

公开版本的既有 GitHub 安装方式仍保留如下；这些命令在候选发布前会取得公开旧版。要审阅候选，请使用此完整目录并按宿主当前支持的本地市场方式操作；本轮未安装或验证授权。

```text
codex plugin marketplace add xieyb2012-netizen/noumi-plugins
codex plugin add noumi@noumi-beta

claude plugin marketplace add xieyb2012-netizen/noumi-plugins
claude plugin install noumi@noumi-beta
```

具体安装、授权与更新步骤见 [安装教程](docs/INSTALL.zh-CN.md)。Claude 桌面使用 Code 标签的历史证据见 [兼容性记录](docs/COMPATIBILITY.md)；普通聊天标签及其他客户端不由此推定。浏览器授权由用户自行完成，不发送密码、Token、Cookie 或完整授权链接。连接测试只检查实际身份与指南，不注册、不出歌、不消费积分。

## 开始创作

接入后可直接说“用 Noumi 做一首适合下班路上听的中文歌，温暖、放松”。不需要每次重复安装指令或粘贴长模板。未提供歌词的一句话成品请求授权一次生成；完整原词默认保留，补全几句词先展示全词（除非事先授权直接生成），多轮打磨等主人确认最后版本才提交。打磨稿留在主人获准使用的 AI 工具里；提交生成后歌词仍交给平台和引擎处理。提交未知时先恢复，不能靠重试再扣费。只写歌词、修改文字或问建议不提交音频任务。

主 Skill 与按需参考包括歌词、押韵与唱感、音乐方向、元标签、执行恢复、头像和封面。歌词结构与篇幅由作品需要决定；没有整首模板歌、固定桥段或时长保证。纯器乐依当前能力判断，当前创作入口要求非空歌词。

## 维护与证据

- [共同内容与候选来源](docs/AGENT-KIT.md)：内容版本、离线生成和漂移检查。
- [历史兼容性](docs/COMPATIBILITY.md)、[验收步骤](docs/ACCEPTANCE.zh-CN.md)：历史事实与当前候选验收分开。
- [发布说明](docs/PUBLISH.zh-CN.md)：发布是独立步骤，网站部署也独立执行。

[Noumi 官网](https://noumi.cc) · [网站 Agent 指南](https://noumi.cc/skill.md) · [隐私政策](https://noumi.cc/privacy) · [服务条款](https://noumi.cc/terms)
