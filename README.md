# XTQ

XTQ 是面向 X Android 客户端的 Modern LSPosed 增强模块，作用域仅为 `com.twitter.android`。

当前公开版本：`0.0.1`（versionCode 19）
主要适配：X `12.20.5-prod.01`，并保留 X `12.19.1-release.0` 的精确目标。

## 功能

- 净化复制、分享和应用内跳转中的 X 链接跟踪参数。
- 提供图片、视频和 GIF 链接复制及下载，视频优先选择非 HLS 最高码率变体。
- 隐藏推广内容、推广用户、视频轮播、资料推荐和横幅。
- 提供敏感媒体显示、高质量视频与投票结果增强选项。
- 在 X 侧边栏提供仅存储于本机的浏览历史。
- 各 Hook 组独立失败并保持 fail-open，不阻止 X 原行为。

## 安装

1. 从 [Releases](https://github.com/Xposed-Modules-Repo/com.tianqianguai.xtq/releases) 下载并安装签名 APK。
2. 在 LSPosed 中启用 XTQ，作用域只选择 X。
3. 强制结束并重新打开 X。

XTQ 使用 libxposed API 102。Release APK 经过 R8 优化与混淆，不包含 Debug ADB Provider。

## 兼容性

- X `12.20.5-prod.01`：模块、链接、媒体、过滤、敏感媒体、高质量视频与浏览历史 Hook 已在设备回归中加载。
- X `12.20.5-prod.01` 的 `poll.results` 仍可能显示 `FAIL`，属于后续适配项；其他 Hook 组保持独立运行。
- X 更新可能改变混淆目标；目标不匹配时 XTQ 保留 X 原行为。

## Source

XTQ is closed source. This repository contains official release metadata and signed APK releases only.
