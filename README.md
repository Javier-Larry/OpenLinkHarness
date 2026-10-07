# OpenLinkHarness
一个基于opencode开发的harness，目标是集各家harness所长
# Open Link Dev1

> 基于 [opencode](https://github.com/anomalyco/opencode)（MIT License）二次开发的 macOS 桌面 AI 编程助手。
> 这是 **ad-hoc 签名** 的开发版 macOS 应用包。

## 特性

- 🖥️ **原生桌面 GUI**：Electron + SolidJS，会话浏览、多标签、命令面板
- 🖱️ **Computer use**：agent 可操控你的 Mac 上其它 App，每步执行前弹权限确认，可随时中止
- 🗜️ **上下文压缩**：工具结果去重/折叠 + 熔断策略
- 🎨 **三主题**：苔绿（默认）/ 冷蓝紫 / 霓虹磷光
- 🔐 **无内置凭据**：provider key 只在软件内自己添加，绝不打进安装包

## 安装

1. 从 [Releases](../../releases) 下载 `Open-Link-Dev1-*-mac-arm64.dmg`，双击挂载。
2. 把 **Open Link Dev1** 拖进 `Applications`。
3. **首次运行**：未公证，macOS 会拦截。拖入 Applications 后，在「启动台/应用」里 **右键 Open Link Dev1 → 打开**。或在终端执行一次：
   ```bash
   xattr -d com.apple.quarantine "/Applications/Open Link Dev1.app"
   ```

## 使用

打开应用后，在「设置 → 提供商」里添加你的 API key（OpenRouter / OpenAI / Anthropic / …），或通过环境变量提供。软件本身不含任何内置 key。

## About

- 源码为对 [anomalyco/opencode](https://github.com/anomalyco/opencode) 的 fork 增强，MIT 协议，原作者署名保留。
- 本 GitHub 仓库仅对外发布 README 与安装包；完整二次开发的源码/构建脚本在本地工作区维护。
- 如果 macOS 权限（辅助功能 / 屏幕录制）在同一构建里被反复要求，是正常现象（ad-hoc 签名按内容 hash 标识）；在「系统设置 → 隐私与安全性」勾一次即可，**同一构建内授权保持有效**。
