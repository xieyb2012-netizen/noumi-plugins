# 维护者分发说明

本仓库用于 GitHub 独立分发，不包含 Noumi 后端源码或账号授权。GitHub 发布不等于已上架 OpenAI 官方目录。

## 发布前

1. 完成至少一位外部测试用户的安装、独立授权和试听，记录客户端版本。
2. 确认要使用的 GitHub 账号与独立仓库名称。建议 `noumi-plugins`，不要将整个 Noumi 业务仓库公开。
3. 由维护者确认公开这个目录的具体文件，再创建仓库并推送。不要拷贝本机 Codex 配置、缓存、日志或授权文件。
4. 仓库根目录必须保留 `.agents/plugins/marketplace.json` 与 `plugins/noumi/`。GitHub 网页上传容易漏掉隐藏目录，上传后检查它们存在。
5. 发布 ZIP Release，附 SHA256 和此次实际验证范围。邀请用户使用自己的账号。

## GitHub 用户安装方式

本仓库的安装命令：

```text
codex plugin marketplace add xieyb2012-netizen/noumi-plugins
codex plugin add noumi@noumi-beta
```

Git 来源更新可运行 `codex plugin marketplace upgrade noumi-beta`，然后重新安装插件并在新任务验证。不要同时保留同名本地来源和 Git 来源；迁移时先确认旧来源，再通过 CLI 移除旧来源后添加新来源。

## 官网入口待接入

建议文案：“用你的 AI 创作音乐” → “安装 Noumi 测试版”。按钮应指向实际发布的仓库／Release，旁边注明支持的客户端与安装教程。没有真实下载地址前不要上线空按钮。

本次没有修改或部署 Noumi 官网。后续官网改动应单独预览后再部署。

## 版本与权限

插件运行文件本次原样保留；分发材料单独标记日期。以后修改 Skill 或连接配置，要更新版本、重打包并重新测试，不复用旧 ZIP 声称新版已通过。

此仓库用于分发安装材料。公开源码授权许可证、正式支持渠道和服务条款的变更须由维护者另行决定；本包没有擅自为 Noumi 后端或音乐作品授予开源许可。
