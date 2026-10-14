<!-- Generated from agent-kit; content 5.1.2. Edit canonical sources, then run node scripts/build-agent-kit.mjs. -->

# 连接 Noumi

> 最近一次公开发布：插件与创作内容 **5.1.2**（2026-10-15，GitHub 本仓库）；本地 MCP 包为 npm `noumi-mcp@5.1.1`。已安装的副本不会自动更新，以宿主里实际显示的版本为准；发布不等于每个宿主都已实测通过，实测范围见兼容性记录。

连接只需要做一次：之后直接用聊天告诉你的 Agent 想要什么歌。已经能用的连接直接继续用，不用重装。

## 按你用的工具

- **Claude（claude.ai / 桌面版）**：优先在 claude.ai 网页打开 Customize → Connectors → Add custom connector，名称 Noumi，地址 `https://noumi.cc/mcp`，点 Connect，登录 Noumi 并点「允许」。之后在对话里用「+」→ Connectors 打开它。
- **Claude Code**：用 claude.ai 账号登录的，账户连接器已经在 `/mcp` 里，直接用；否则运行 `claude mcp add --transport http noumi https://noumi.cc/mcp`，再在 `/mcp` 里选它授权。也可以改装本仓库的插件（可选）。
- **Codex**：运行 `codex mcp add noumi --url https://noumi.cc/mcp`，再运行 `codex mcp login noumi` 授权；也可以改装插件（可选）。已有同名条目时不要重复添加。
- **WorkBuddy 等不支持授权的工具**：用原音乐人的密钥配置本地 MCP，见 [用密钥连接（备用）](https://noumi.cc/api-docs#key)。
- **其他工具**：见 [接入指南](https://noumi.cc/api-docs)，那里写了每个工具的步骤和我们实测到哪一步。

授权都由你本人在浏览器里完成。登录 Noumi 网站不等于授权，一定要在授权页上点「允许」。

## 安装插件（可选）

插件把同一个远程连接和创作规范打包在一起，并不是另一种授权。装了插件就不要再手动加同一地址。

```text
codex plugin marketplace add xieyb2012-netizen/noumi-plugins
codex plugin add noumi@noumi-beta

claude plugin marketplace add xieyb2012-netizen/noumi-plugins
claude plugin install noumi@noumi-beta
```

装好后插件的服务（`noumi-plugin`）还要由你授权一次：Claude Code 在 `/mcp` 里选它登录；Codex 按客户端提示连接。列表里显示「已连接」只说明服务器连得上，不等于已授权。Windows 上 Claude 桌面版授权后停在「打开 Claude」时，在普通终端运行 `claude` → `/mcp` → 选它授权，再回桌面版新开会话，两边共用这份授权。

不要安装多个来源的 Noumi 插件以免工具重复；已经装过的，先确认旧版本来源再更新。

## 第一次连接检查

新建会话，发送：

> 请调用 Noumi 的 noumi_whoami 和 noumi_get_guide：告诉我连上的 Noumi 账号、要用的音乐人（名字和编号）和它已有几首作品。只做检查，不注册音乐人、不生成歌曲。

通过标准：报出你自己的账号、你要用的那个音乐人和它的作品，指南有实际内容。只看见工具名称、授权成功页面或「已连接」，不算通过。

## 常见问题

- **显示已连接，但它不认识我**：还没授权或授权已失效。按上面你那种工具重新授权；不要为此重新注册音乐人。
- **Windows 上 Claude 桌面版授权后停在「打开 Claude」**：关掉那次授权。用账户连接器的，改到 claude.ai 网页完成；用 Claude Code / 插件的，在普通终端运行 `claude` → `/mcp` 授权，再回桌面版新开会话。
- **我的工具根本不出授权页**：有的工具要你显式点「连接 / 登录」。确实不支持授权、但能运行本地程序的，改用密钥备用。
- **原来的音乐人没列出来**：先确认登录的是不是原来那个账号。音乐人认领在你账号下，授权后就会列出，不管当初怎么建的。不要新注册。
- **没有音乐人**：只读检查不会注册，这是正常的。你明确要建一个时，确认名字后只建一个。
- **积分不足**：按 Noumi 返回说明处理，Agent 不会自动购买积分。
- **生成较慢或任务中断**：让 Agent 继续查询原任务编号，不重新提交同一首歌。

## 更新和卸载插件

更新：按宿主的插件更新方式操作，更新后新开会话确认版本。卸载可在客户端插件页面操作，或运行 `codex plugin remove noumi@noumi-beta` / `claude plugin uninstall noumi@noumi-beta`。卸载插件不会删除你的 Noumi 歌曲或账号。

更多细节和每个工具的实测范围见 [接入指南](https://noumi.cc/api-docs)。
