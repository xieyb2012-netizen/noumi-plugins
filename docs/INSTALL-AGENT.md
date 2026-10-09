<!-- Generated from agent-kit; content 5.1.1. Edit canonical sources, then run node scripts/build-agent-kit.mjs. -->

> 本地待审候选：插件 **5.1.1**，创作内容 **5.1.1**。未发布、未安装；历史验收记录不代表本候选已通过宿主授权或出歌测试。

# Agent 接入规则

状态：双端邀请测试。当前验收边界见 COMPATIBILITY.md。

1. 识别当前宿主、版本及安装权限，不能仅凭模型名判断。检查现有插件、工具来源和技能，已在别的客户端安装不算。不要自动关闭、覆盖或移除现有服务。
2. ChatGPT 桌面工作环境中具备 Codex 插件管理能力时，使用仓库 `.agents/plugins/marketplace.json`、`plugins/noumi`；Claude Code 使用 `.claude-plugin/marketplace.json`、`plugins/noumi-claude`。一次只选当前宿主的适配，不能同时安装两套作为兜底。
3. 从 GitHub 安装：Codex CLI 执行 `codex plugin marketplace add xieyb2012-netizen/noumi-plugins`，再执行 `codex plugin add noumi@noumi-beta`；Claude Code CLI 执行 `claude plugin marketplace add xieyb2012-netizen/noumi-plugins`，再执行 `claude plugin install noumi@noumi-beta`。执行前查看当前版本帮助与已有配置，来源已存在时不要重复添加或覆盖。桌面 Claude Code 已验证可加载 CLI 装入的本地插件，不能把这个结果说成桌面 GitHub 安装路径已通过。保留实际版本、来源与工具来源。
4. 安装后报告实际生效条件：Claude 摘要提示 reload 时，在交互会话执行 `/reload-plugins`，否则新会话验证；Codex 侧新任务检查，必要时重启客户端，不承诺热加载。
5. Claude CLI 授权在交互会话的 `/mcp` 中选择实际插件服务（可能显示带插件前缀的 `noumi-plugin`）。桌面应用账户连接器目录不能代替该入口。宿主要求登录时由用户自行登录。
6. 用户在浏览器确认账号与授权内容；授权超时回客户端重新发起，不催促跳过阅读。不要读取或传递密码、Token、Cookie、完整授权链接。已有连接但身份不明时检查实际来源；重新授权仅针对明确选中的服务。
7. 只调用 `noumi_whoami`、`noumi_get_guide` 完成只读验收。须有实际返回，且确认来源是安装的插件。工具前缀由宿主呈现，不凭推测拼接；手动 MCP 成功不能替代插件验收。
8. 报告真实结果，再问用户想写什么歌。身份未知不等于音乐人为空。接入测试不注册、不提交歌曲、不消费积分；正式创作按技能处理复用、选择与注册。

如果宿主不能自行安装，只提供其已验证的设置入口和 `https://noumi.cc/mcp`；该产品形态未验证时明确说明，不能编造菜单或宣称兼容。连接器接通也不代表已安装技能。

同一 URL 有多个来源时不假设自动去重，不自动清除凭据。需要配置调整时先报告具体影响并取得授权。

## 本候选的版本边界

两宿主插件版本均为 5.1.1，共同创作内容为 5.1.1。当前材料仅在本地生成与检查；原有证据保留原日期。GitHub 安装命令在候选发布前不会取得它。连接检查与正式创作分开；不把手动 MCP 来源当作插件来源。
