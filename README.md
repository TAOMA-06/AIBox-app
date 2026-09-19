<div align="center">

# 智盒AI · AIBox

**一个 App，接入所有主流大模型。**

<sub>BYOK · 统一会话 · Agent 优先 · 三协议原生工具调用 · iOS 系统级入口</sub><br>
<sub>你的 Key 在 Keychain，你的会话在设备上，你的数据不属于任何厂商。</sub>

<br>

[![iOS](https://img.shields.io/badge/iOS-18.0+-000000?style=flat-square&logo=apple&logoColor=white)](https://github.com/TAOMA-06/AIBox-app/releases)
[![Version](https://img.shields.io/badge/version-2.0.0-0A84FF?style=flat-square)](https://github.com/TAOMA-06/AIBox-app/releases)
[![Swift](https://img.shields.io/badge/Swift_6-SwiftUI_·_SwiftData-F05138?style=flat-square&logo=swift&logoColor=white)](https://github.com/TAOMA-06/AIBox-app/releases)
[![Backend](https://img.shields.io/badge/backend-none-34C759?style=flat-square)](https://github.com/TAOMA-06/AIBox-app/releases)
[![Analytics](https://img.shields.io/badge/tracking-none-34C759?style=flat-square)](https://github.com/TAOMA-06/AIBox-app/releases)

<br>

**[⬇ 下载安装（TestFlight）](https://github.com/TAOMA-06/AIBox-app/releases)** ·
**[隐私政策](Docs/privacy-policy.md)** ·
**[用户协议](Docs/terms-of-use.md)** ·
**[隐私清单](Docs/PrivacyInfo.xcprivacy)**

</div>

---

## ◈ 为什么是 AIBox

各家官方 AI App 的聊天记录互不互通，你的对话被锁在厂商的围墙里。
AIBox 把所有模型放进同一条时间线——**一条会话，中途可换供应商和模型，每条回复标注来源。**

```text
你 ──► AIBox ──► 你选的供应商 API
        │
        └─ Key 存 Keychain · 会话存设备 · 无后端 · 无账号 · 无追踪
```

## ✦ 核心能力

| | |
|:--|:--|
| **7+ 供应商 · 3 协议** | DeepSeek / 通义千问 / Kimi / 智谱 / OpenAI / Anthropic / Gemini 预设 + 任意 OpenAI 兼容端点 |
| **统一会话** | 跨供应商保留历史，会话内切换模型，助手消息标注来源 |
| **Agent（手机端 OpenCode）** | 会话即入口：斜杠命令 · 三协议原生工具调用（OpenAI / Anthropic / Gemini）· 工具留痕可折叠回看 |
| **工具权限** | 副作用操作执行前确认：允许一次 / 总是允许 / 拒绝，拒绝如实回填模型 |
| **自定义 Agent** | 名称 / 提示词 / 工具集 / 绑定模型全可定制，内置通用·聊天·写作·研究 |
| **工作区文件** | Agent 可读 / 搜 / 改指定文件夹（含 Files App 目录），替换前匹配原文 |
| **上下文与费用** | 超窗口自动摘要压缩旧历史；每条消息显示 token 用量与费用估算 |
| **MCP 客户端** | Streamable HTTP 接入远程 MCP 服务器，远程工具与本地工具同权调用 |
| **多模型对比** | 同一问题并发发 2–4 个模型，并排流式展示（Pro） |
| **多模态** | 图片输入，自动压缩至 1536px / JPEG 0.8（Pro） |
| **系统入口** | 分享扩展 · AI 自定义键盘（润色/译英/总结选中文字）· 快捷指令 · 桌面小组件 · `aibox://` 深链 · 语音直达 |
| **导出备份** | 会话 Markdown 导出 · 全量 JSON 备份（Android 端可导入） |

## ▍隐私立场

- **零后端**：没有我们的服务器，你的输入只发给你自己配置的供应商接口
- **零追踪**：无分析 SDK、无广告、无账号系统
- **Key 不出设备**：API Key 仅存 iOS Keychain
- **数据在你手里**：SwiftData 本地存储，JSON 备份由你掌控去向

详见 [隐私政策](Docs/privacy-policy.md) · [用户协议](Docs/terms-of-use.md) · [隐私清单](Docs/PrivacyInfo.xcprivacy)

## ▍安装

| 渠道 | 状态 |
|:--|:--|
| Android 预览包 | **[⬇ AIBox-2.0.0-debug.apk](https://github.com/TAOMA-06/AIBox-app/releases/download/v2.0.0/AIBox-2.0.0-debug.apk)**（debug 签名，需允许「未知来源」） |
| iOS（TestFlight） | v2.0.0 IPA 已产出，公测通道筹备中 — 关注 [Releases](https://github.com/TAOMA-06/AIBox-app/releases) |
| App Store | 审核筹备中 |

本仓库为产品主页与发布渠道，源码闭源。商业合作/问题反馈请开 [Issue](https://github.com/TAOMA-06/AIBox-app/issues)。

---

<div align="center">
<sub>智盒AI · Built for people who use every model, not just one.</sub>
</div>
