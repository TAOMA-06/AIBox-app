# AIBox 送审合规包（privacy-review）

应用：智盒AI ｜ Bundle：`com.taoma.aibox` ｜ 版本：0.1.0（Build 1）｜ iOS 18+

## 1. 隐私说明（数据去哪、存哪、一键删）

- 数据去哪：用户输入文本仅发送到用户自行选择的第三方 AI 供应商（DeepSeek/通义千问/Kimi/智谱/自定义）接口用于生成回答；不经过自建服务器，不做埋点与广告 SDK 上报。
- 存哪：
  - API Key：本机 Keychain（service `com.taoma.aibox.apikey`），另镜像一份到本机共享偏好（`aibox.deepseek.apikey`）供分享扩展/快捷指令/小组件读取，不离机。
  - 历史记录：本机 SwiftData（`Conversation`/`Message`），不上传。
  - 最近一条结果：本机共享偏好（`aibox.lastResult`），供小组件显示。
  - 模型选择：本机 `UserDefaults`（`aibox.model`）。
- 一键删：设置页"删除"按钮清 Keychain Key；历史页"清空"/设置页"清除全部历史"删全部本地记录；卸载 App 即清全部本机数据。
- 第三方声明：AI 回答由用户自行选择的供应商生成，为第三方 AI 生成内容，仅供参考（各输出页顶部均有标识）。
- 隐私清单：`PrivacyInfo.xcprivacy` 中 Tracking=false、无收集数据类型；Required Reason API 仅声明 UserDefaults（CA92.1）与 FileTimestamp（C617.1）。

## 2. AI 标识位置（审核可复核路径）

- 首屏：对话页顶部常驻"由当前供应商提供，为第三方 AI 生成内容"。
- 输出页：写作页、总结页、语音直达页顶部同一文案常驻。
- 设置页：试用说明段 +「隐私说明」内页末尾"AI 回答由 DeepSeek 提供，为第三方 AI 生成内容，仅供参考"。
- 分享扩展：面板标题"智盒AI · 分享总结"，结果区为单次生成文本，用户可复制核验。
- 快捷指令：三个 Intent 使用当前供应商生成，Siri 朗读结果即模型输出。

## 3. 权限用途（与 Info.plist 一一对应）

| 权限 | plist key | 用途话术 | 使用位置 |
|---|---|---|---|
| 麦克风 | `NSMicrophoneUsageDescription`：「语音输入与语音直达需要使用麦克风。」 | 按住说话采集语音做转写提问 | `Features/Voice/VoiceView.swift`（VoiceEngine） |
| 语音识别 | `NSSpeechRecognitionUsageDescription`：「语音直达需要将语音转写为文字。」 | 系统语音转文字，转写文本再发 DeepSeek | 同上（SFSpeechRecognizer zh-CN） |
| 剪贴板 | 无需 plist 声明（按需读取） | 捷径读剪贴板做总结/润色；分享面板"从剪贴板粘贴"；各结果页"复制"写剪贴板 | Intents/Share/各 Feature 结果栏 |

无后台录音、无连续识别：松开即停（`VoiceEngine.stop`），退出页面即释放录音资源。

## 4. App Store 审核备注话术（粘贴即用）

```
智盒AI 为 BYOK 工具：用户自带第三方 AI 供应商 API Key，无自建账号体系。
测试 Key 获取：在用户选择的供应商平台注册并创建 API Key → 填入 App「设置」→「供应商详情」保存。
无 Key 时各功能会中文提示填写，不会白屏/崩溃。
AI 内容标识：对话/写作/总结/语音页顶部均有"由 DeepSeek 提供，为第三方 AI 生成内容"声明。
数据存储：Key 存本机 Keychain，会话存本机 SwiftData，可一键删除；网络请求仅发往用户主动选择的供应商地址。
权限：麦克风 + 语音识别仅用于语音直达页按住说话转写；拒绝后降级为文字提问。
分享扩展/小组件/快捷指令不独立联网（小组件只读本地最近结果；扩展/捷径直调同一 DeepSeek 接口）。
应用内隐私政策路径：设置 → 关于 → 隐私政策。应用内购买由 Apple StoreKit 处理，Pro 产品为一次性非消耗型权益。
```

## 5. 版本与送审前自查

- 版本：`CFBundleShortVersionString` 0.1.0，`CFBundleVersion` 1（主 App `Resources/Info.plist` 与 `project.yml` 一致）。
- 自查清单：3 target 构建通过；真机 6 用例按 `Docs/device-test.md` 通过；隐私清单无新增 API 未声明；AI 标识四页可见；缺 Key/无网/拒权限三条降级路径均为中文提示。
