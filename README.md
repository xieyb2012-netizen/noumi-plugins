# Noumi · 一句话创作完整歌曲

连接自己的 Noumi 账号，告诉 AI 想听什么，等待歌曲完成后前往 Noumi 试听。

> 用 Noumi 做一首适合下班路上听的中文歌，温暖、放松，有钢琴和轻柔鼓点。

这是邀请测试版，通过同一个仓库提供 ChatGPT 桌面工作环境的 Codex 插件适配与 Claude Code 插件适配。不是官方公共市场上架版本。各客户端的实际验证范围见 [兼容性表](docs/COMPATIBILITY.md)。

## 一个入口

复制给你正在使用的 AI：

> 请按 https://github.com/xieyb2012-netizen/noumi-plugins 的接入说明帮我连接 Noumi，选择适合当前工具的安装方式，确认连接成功后，让我们一起创作歌曲。

执行安装的 Agent 请先读 [接入规则](docs/INSTALL-AGENT.md)，识别当前宿主后选择一套适配。安装与身份检查不注册、不生成歌曲。

## 开始使用

GitHub 分发仓库：[xieyb2012-netizen/noumi-plugins](https://github.com/xieyb2012-netizen/noumi-plugins)。

ChatGPT 桌面工作环境中已配置 Codex CLI 的用户：

```text
codex plugin marketplace add xieyb2012-netizen/noumi-plugins
codex plugin add noumi@noumi-beta
```

Claude Code 终端版：

```text
claude plugin marketplace add xieyb2012-netizen/noumi-plugins
claude plugin install noumi@noumi-beta
```

Claude 桌面版请使用 **Code 标签**。本地市场经 CLI 安装后可加载，桌面版本 2.110.1 已完成技能与身份检查；界面的 GitHub 市场入口存在，但从该入口全新安装尚待独立验收。普通聊天标签不据此宣称支持。

也可以从 [测试版下载页](https://github.com/xieyb2012-netizen/noumi-plugins/releases) 获取 ZIP，按以下步骤安装。两种来源选择一种即可。

1. 下载并解压完整分发包，将文件夹保存在长期位置，例如“文档/Noumi 插件”。不要只取出 `plugins/noumi`，也不要在 ZIP 内运行。
2. 按 [安装教程](docs/INSTALL.zh-CN.md) 添加插件来源、安装 Noumi。
3. 浏览器打开后，登录自己的 Noumi 账号并允许连接。不要发送密码或授权链接给其他人。
4. 新建对话，先完成教程中的只读连接检查，再说出想创作的歌曲。

无需在电脑部署音乐模型或 Noumi 服务器。生成使用你的 Noumi 积分；积分不足时按服务提示处理。用户请求创作后，若已确认授权且尚无音乐人，插件会按照 Noumi 当前流程创建；仅连接检查不会注册。歌曲默认是草稿，公开发布由你在 Noumi 手动完成。商用权限以具体歌曲的实际授权为准。

## 这个包包含什么

- `plugins/noumi-claude/` 与 `.claude-plugin/marketplace.json`：Claude Code 远程适配，与原适配隔离。
- `plugins/noumi/`：已测试版本的连接配置和创作技能，不含服务端源码。
- `.agents/plugins/marketplace.json`：可搬移的插件来源目录，名称 `noumi-beta`。
- `docs/INSTALL.zh-CN.md`：安装、授权、更新和排查说明。
- `docs/ACCEPTANCE.zh-CN.md`：给测试用户的验收步骤和反馈表。
- `docs/PUBLISH.zh-CN.md`：维护者发布 GitHub 仓库的步骤。

每个用户独立授权；本包不携带任何用户登录状态。Codex 适配版本为 `0.1.0+codex.20260914152200`，Claude 适配版本为 `0.1.0`。双端分发日期：2026-09-18。

## 验证范围

维护者此前已在自己的环境通过授权、歌曲创作和人工试听。这不等于当前分发包已通过另一台电脑、另一个用户的完整验收。详细证据和待测项目见 [验收说明](docs/ACCEPTANCE.zh-CN.md)。

## 链接

[Noumi 官网](https://noumi.cc) · [隐私政策](https://noumi.cc/privacy) · [服务条款](https://noumi.cc/terms)

安装问题请反馈给向你发出邀请的人，附客户端版本和脱敏错误即可，不提供密码、Token、Cookie 或浏览器完整授权地址。
