<div align="center">

# 智盒AI · AIBox

**一个 App，接入所有主流大模型。**

<sub>BYOK · 统一会话 · 聊天/工作双模式 Agent · iOS 系统级入口</sub><br>
<sub>你的 Key 在 Keychain，你的会话在设备上，你的数据不属于任何厂商。</sub>

<br>

[![iOS](https://img.shields.io/badge/iOS-18.0+-000000?style=flat-square&logo=apple&logoColor=white)](https://github.com/TAOMA-06/AIBox-app/releases)
[![Version](https://img.shields.io/badge/version-1.1.0-0A84FF?style=flat-square)](https://github.com/TAOMA-06/AIBox-app/releases)
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
| **工作模式 Agent** | 多轮工具循环：剪贴板 · 计算器 · 日历 · 提醒事项 · 工作区文件 · URL 抓取，全程留痕可折叠回看 |
| **MCP 客户端** | Streamable HTTP 接入远程 MCP 服务器，远程工具与本地工具同权调用 |
| **多模型对比** | 同一问题并发发 2–4 个模型，并排流式展示（Pro） |
| **多模态** | 图片输入，自动压缩至 1536px / JPEG 0.8（Pro） |
| **系统入口** | 分享扩展 · AI 自定义键盘（润色/译英/总结选中文字）· 快捷指令 · 桌面小组件 · `aibox://` 深链 · 语音直达 |
| **导出备份** | 会话 Markdown 导出 · 全量 JSON 备份恢复 |

## ▍隐私立场

- **零后端**：没有我们的服务器，你的输入只发给你自己配置的供应商接口
- **零追踪**：无分析 SDK、无广告、无账号系统
- **Key 不出设备**：API Key 仅存 iOS Keychain
- **数据在你手里**：SwiftData 本地存储，JSON 备份由你掌控去向

详见 [隐私政策](Docs/privacy-policy.md) · [用户协议](Docs/terms-of-use.md) · [隐私清单](Docs/PrivacyInfo.xcprivacy)

## ▍安装

| 渠道 | 状态 |
|:--|:--|
| TestFlight 公开测试 | 即将开放 — 关注 [Releases](https://github.com/TAOMA-06/AIBox-app/releases) |
| App Store | 审核筹备中 |

本仓库为产品主页与发布渠道，源码闭源。商业合作/问题反馈请开 [Issue](https://github.com/TAOMA-06/AIBox-app/issues)。

---

<div align="center">
<sub>智盒AI · Built for people who use every model, not just one.</sub>
</div>
