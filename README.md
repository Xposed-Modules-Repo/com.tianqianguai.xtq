# XTQ

XTQ 是面向 X Android 客户端的 Modern LSPosed 增强模块，作用域仅为 `com.twitter.android`。
XTQ is a Modern LSPosed enhancement module for the X Android client, scoped only to `com.twitter.android`.

当前公开版本：`0.0.1`（versionCode 19）。
Current public release: `0.0.1` (versionCode 19).

主要适配：X `12.20.5-prod.01`，并保留 X `12.19.1-release.0` 的精确目标。
Primary compatibility: X `12.20.5-prod.01`, while retaining the exact target for X `12.19.1-release.0`.

## 核心特色 / Signature Feature

**X 内本地浏览历史 / Private in-X browsing history**

在 X 内注入的侧边栏浏览历史，仅记录用户明确打开的帖子、视频或 GIF；不会记录滚动曝光、自动播放或仅查看图片。历史仅保留在本机并保持私密，支持重新打开记录和清空历史，不上传任何数据。
Injected inside X's sidebar, local browsing history records only posts, videos, or GIFs that the user explicitly opens; it does not record scroll exposure, autoplay, or image-only viewing. History stays local and private, supports reopening entries and clearing history, and uploads no data.

## 其他功能 / Other Features

- **链接净化 / Link cleanup**：净化复制、分享和应用内跳转中的 X 链接跟踪参数。 / Cleans tracking parameters from X links copied, shared, or opened in the app.
- **媒体链接与下载 / Media links and downloads**：提供图片、视频和 GIF 链接复制及下载，视频优先选择非 HLS 最高码率变体。 / Copies and downloads image, video, and GIF links, preferring the highest-bitrate non-HLS video variant.
- **内容过滤 / Content filtering**：隐藏推广内容、推广用户、视频轮播、资料推荐和横幅。 / Hides promoted content, promoted users, video carousels, profile recommendations, and banners.
- **媒体与投票选项 / Media and poll options**：提供敏感媒体显示、高质量视频与投票结果增强选项。 / Provides sensitive-media display, high-quality video, and poll-result enhancement options.
- **独立 Hook 组 / Independent Hook groups**：各 Hook 组独立失败并保持 fail-open，不阻止 X 原行为。 / Hook groups fail independently and remain fail-open, so they do not block X's original behavior.

## 安装 / Installation

1. 从 [Releases](https://github.com/Xposed-Modules-Repo/com.tianqianguai.xtq/releases) 下载并安装签名 APK。 / Download and install the signed APK from [Releases](https://github.com/Xposed-Modules-Repo/com.tianqianguai.xtq/releases).
2. 在 LSPosed 中启用 XTQ，作用域只选择 X。 / Enable XTQ in LSPosed and select only X as the scope.
3. 强制结束并重新打开 X。 / Force-stop and reopen X.

XTQ 使用 libxposed API 102。Release APK 经过 R8 代码/资源优化、重打包和入口混淆，不包含 Debug ADB Provider。
XTQ uses libxposed API 102. The Release APK uses R8 code/resource optimization, repackaging, and entry-point obfuscation, and does not include the Debug ADB Provider.

## 兼容性 / Compatibility

- X `12.20.5-prod.01`：模块、链接、媒体、过滤、敏感媒体、高质量视频与浏览历史 Hook 已在设备回归中加载。 / On X `12.20.5-prod.01`, the module, link, media, filtering, sensitive-media, high-quality-video, and browsing-history hooks have loaded in device regression.
- X `12.19.1-release.0`：保留已验证的精确目标。 / X `12.19.1-release.0`: its verified exact target is retained.
- X `12.20.5-prod.01` 的 `poll.results` 仍可能显示 `FAIL`，属于后续适配项；其他 Hook 组保持独立运行。 / `poll.results` on X `12.20.5-prod.01` may still show `FAIL` and remains a follow-up compatibility item; other Hook groups continue to run independently.
- X 更新可能改变混淆目标；目标不匹配时 XTQ 保留 X 原行为。 / X updates may change obfuscated targets; when a target does not match, XTQ preserves X's original behavior.

## 源码 / Source

XTQ 是闭源项目。本仓库仅包含官方发布元数据和签名 APK 发布文件。
XTQ is closed source. This repository contains official release metadata and signed APK releases only.
