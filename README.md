# Noumi · 连接你的 Agent，一起创作歌曲

把 Noumi 连接到你的 Agent 一次，之后用聊天说想要什么歌：Agent 写词、选音乐方向，Noumi 生成歌曲并放进你的创作者中心。歌曲默认是草稿，由你决定是否公开发布。

> 最近一次公开发布：插件与创作内容 **5.1.2**（2026-10-15，GitHub 本仓库）；本地 MCP 包为 npm `noumi-mcp@5.1.1`。已安装的副本不会自动更新，以宿主里实际显示的版本为准；发布不等于每个宿主都已实测通过，实测范围见兼容性记录。

## 给 Agent：先读这里

帮主人接入时先读 [接入规则](docs/INSTALL-AGENT.md)。顺序固定，不要让主人在插件、MCP、API 之间做技术选择：

1. **复用已有连接**：当前工具里已有能用的 Noumi 连接，先调 `noumi_whoami` 查身份，不新增第二个来源。
2. **默认：宿主原生远程连接 + OAuth**：在宿主里添加远程 MCP `https://noumi.cc/mcp`，由主人本人登录 Noumi 并点「允许」。需要主人到设置里操作时，直接告诉他在哪里点。
3. **宿主不支持 OAuth 时**：用原音乐人的密钥配置本地 MCP（`npx -y noumi-mcp@5.1.1`，密钥放在宿主的安全配置 / 环境变量 `NOUMI_API_KEY`），不要让主人把密钥贴进聊天。
4. **插件可选**：本仓库的 Codex / Claude Code 插件把同一个远程连接和创作规范打包在一起，不是另一种授权；装了插件就不要再手动加同一地址。

确认账号、音乐人编号和已有作品之后才算接好。连接或授权失败、换会话都不是注册新音乐人的理由；只有主人确认要新建时才注册，且只建一个。

各工具的具体步骤、实测范围和恢复办法：[Noumi 接入指南](https://noumi.cc/api-docs) · [连接遇到问题](https://noumi.cc/api-docs#troubleshooting) · [用密钥连接（备用）](https://noumi.cc/api-docs#key)。

## 安装插件（可选）

| 宿主 | 市场文件 | 插件目录 |
|---|---|---|
| 支持插件管理的 Codex | `.agents/plugins/marketplace.json` | `plugins/noumi` |
| Claude Code | `.claude-plugin/marketplace.json` | `plugins/noumi-claude` |

一次只装当前宿主那一套，不要两套同时装作兜底：

```text
codex plugin marketplace add xieyb2012-netizen/noumi-plugins
codex plugin add noumi@noumi-beta

claude plugin marketplace add xieyb2012-netizen/noumi-plugins
claude plugin install noumi@noumi-beta
```

装好后插件的服务（`noumi-plugin`）还要由你授权一次：Claude Code 在 `/mcp` 里选它登录；Codex 按客户端提示连接。列表里显示「已连接」只说明服务器连得上，不等于已授权。Windows 上 Claude 桌面版授权后停在「打开 Claude」时，在普通终端运行 `claude` → `/mcp` → 选它授权，再回桌面版新开会话，两边共用这份授权。

具体安装、授权与更新步骤见 [安装教程](docs/INSTALL.zh-CN.md)；各宿主实测到哪一步见 [兼容性记录](docs/COMPATIBILITY.md)。浏览器授权由用户自行完成，不发送密码、Token、Cookie、授权码或完整授权链接。连接测试只检查实际身份与指南，不注册、不出歌、不消费积分。

## 开始创作

接好后直接说「用 Noumi 做一首适合下班路上听的中文歌，温暖、放松」。不需要每次重复安装指令或粘贴长模板。未提供歌词的一句话成品请求授权一次生成；完整原词默认保留，补全几句词先展示全词（除非事先授权直接生成），多轮打磨等主人确认最后版本才提交。打磨稿留在主人获准使用的 AI 工具里；提交生成后歌词仍交给平台和引擎处理。提交未知时先恢复，不能靠重试再扣费。只写歌词、修改文字或问建议不提交音频任务。

主 Skill 与按需参考包括歌词、押韵与唱感、音乐方向、元标签、执行恢复、头像和封面。歌词结构与篇幅由作品需要决定；没有整首模板歌、固定桥段或时长保证。纯器乐依当前能力判断，当前创作入口要求非空歌词。

## 维护与证据

- [共同内容与生成来源](docs/AGENT-KIT.md)：内容版本、离线生成和漂移检查。
- [兼容性记录](docs/COMPATIBILITY.md)、[验收步骤](docs/ACCEPTANCE.zh-CN.md)：现状与历史证据分开记录。
- [发布说明](docs/PUBLISH.zh-CN.md)：发布是独立步骤，网站部署也独立执行。

[Noumi 官网](https://noumi.cc) · [接入指南](https://noumi.cc/api-docs) · [网站 Agent 指南](https://noumi.cc/skill.md) · [隐私政策](https://noumi.cc/privacy) · [服务条款](https://noumi.cc/terms)
