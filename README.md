# Noumi · 一句话创作完整歌曲

连接自己的 Noumi 账号，告诉 AI 想听什么，等待歌曲完成后前往 Noumi 试听。

> 用 Noumi 做一首适合下班路上听的中文歌，温暖、放松，有钢琴和轻柔鼓点。

这是邀请测试版，面向支持本地／仓库插件来源的 Codex 或 ChatGPT 桌面工作环境。不是官方公共市场上架版本；普通 ChatGPT 网页、手机及其他 AI 客户端尚未验证。功能入口仍受账号、地区和工作区政策影响。

## 开始使用

GitHub 分发仓库：[xieyb2012-netizen/noumi-plugins](https://github.com/xieyb2012-netizen/noumi-plugins)。

已配置 Codex CLI 的用户可直接安装：

```text
codex plugin marketplace add xieyb2012-netizen/noumi-plugins
codex plugin add noumi@noumi-beta
```

也可以从 [测试版下载页](https://github.com/xieyb2012-netizen/noumi-plugins/releases) 获取 ZIP，按以下步骤安装。两种来源选择一种即可。

1. 下载并解压完整分发包，将文件夹保存在长期位置，例如“文档/Noumi 插件”。不要只取出 `plugins/noumi`，也不要在 ZIP 内运行。
2. 按 [安装教程](docs/INSTALL.zh-CN.md) 添加插件来源、安装 Noumi。
3. 浏览器打开后，登录自己的 Noumi 账号并允许连接。不要发送密码或授权链接给其他人。
4. 新建对话，先完成教程中的只读连接检查，再说出想创作的歌曲。

无需在电脑部署音乐模型或 Noumi 服务器。生成使用你的 Noumi 积分；积分不足时按服务提示处理。新用户授权后若尚无音乐人，插件会按照 Noumi 当前流程创建。歌曲默认是草稿，公开发布由你在 Noumi 手动完成。商用权限以具体歌曲的实际授权为准。

## 这个包包含什么

- `plugins/noumi/`：已测试版本的连接配置和创作技能，不含服务端源码。
- `.agents/plugins/marketplace.json`：可搬移的插件来源目录，名称 `noumi-beta`。
- `docs/INSTALL.zh-CN.md`：安装、授权、更新和排查说明。
- `docs/ACCEPTANCE.zh-CN.md`：给测试用户的验收步骤和反馈表。
- `docs/PUBLISH.zh-CN.md`：维护者发布 GitHub 仓库的步骤。

每个用户独立授权；本包不携带任何用户登录状态。安装包中的创作技能版本为 `0.1.0+codex.20260914152200`，本次分发整理日期为 2026-09-15。

## 验证范围

维护者此前已在自己的环境通过授权、歌曲创作和人工试听。这不等于当前分发包已通过另一台电脑、另一个用户的完整验收。详细证据和待测项目见 [验收说明](docs/ACCEPTANCE.zh-CN.md)。

## 链接

[Noumi 官网](https://noumi.cc) · [隐私政策](https://noumi.cc/privacy) · [服务条款](https://noumi.cc/terms)

安装问题请反馈给向你发出邀请的人，附客户端版本和脱敏错误即可，不提供密码、Token、Cookie 或浏览器完整授权地址。
