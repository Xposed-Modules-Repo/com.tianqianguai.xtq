<p align="center">
  <img src="docs/assets/xtq-icon.png" width="168" height="168" alt="XTQ icon">
</p>

<h1 align="center">XTQ</h1>

<p align="center">
  面向 X Android（<code>com.twitter.android</code>）的 LSPosed/Xposed 增强模块
  <br>
  An LSPosed/Xposed enhancement module for X Android
</p>
<p align="center">
  <a href="https://github.com/Xposed-Modules-Repo/com.tianqianguai.xtq/stargazers"><img src="https://img.shields.io/github/stars/Xposed-Modules-Repo/com.tianqianguai.xtq?style=for-the-badge&logo=github&label=Star" alt="GitHub Stars"></a>
  <a href="https://t.me/XTQ_Offical"><img src="https://img.shields.io/badge/Telegram-XTQ__Offical-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram Official Group"></a>
  <a href="https://t.me/zhongjitianqianguai3"><img src="https://img.shields.io/badge/Telegram-Release_Channel-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="软件发布频道 / Release Channel"></a>
</p>
<p align="center">
  如果 XTQ 对你有帮助，欢迎点一个 Star 支持项目 ⭐
  <br>
  If XTQ helps you, please consider leaving a Star.
</p>

当前公开版本：`0.0.1`（versionCode 19）。

Current public release: `0.0.1` (versionCode 19).

主要适配：X `12.20.5-prod.01`，并保留 X `12.19.1-release.0` 的精确目标。

Primary compatibility: X `12.20.5-prod.01`, while retaining the exact target for X `12.19.1-release.0`.

## 功能

- **X 内本地浏览历史**：在 X 内注入的侧边栏浏览历史，仅记录用户明确打开的帖子、视频或 GIF；不会记录滚动曝光、自动播放或仅查看图片。历史仅保留在本机并保持私密，支持重新打开记录和清空历史，不上传任何数据。
- **链接净化**：净化复制、分享和应用内跳转中的 X 链接跟踪参数。
- **媒体链接与下载**：提供图片、视频和 GIF 链接复制及下载，视频优先选择非 HLS 最高码率变体。
- **内容过滤**：隐藏推广内容、推广用户、视频轮播、资料推荐和横幅。
- **媒体与投票选项**：提供敏感媒体显示、高质量视频与投票结果增强选项。
- **独立 Hook 组**：各 Hook 组独立失败并保持 fail-open，不阻止 X 原行为。

## Features

- **Private in-X browsing history**: Injected inside X's sidebar, local browsing history records only posts, videos, or GIFs that the user explicitly opens; it does not record scroll exposure, autoplay, or image-only viewing. History stays local and private, supports reopening entries and clearing history, and uploads no data.
- **Link cleanup**: Cleans tracking parameters from X links copied, shared, or opened in the app.
- **Media links and downloads**: Copies and downloads image, video, and GIF links, preferring the highest-bitrate non-HLS video variant.
- **Content filtering**: Hides promoted content, promoted users, video carousels, profile recommendations, and banners.
- **Media and poll options**: Provides sensitive-media display, high-quality video, and poll-result enhancement options.
- **Independent Hook groups**: Hook groups fail independently and remain fail-open, so they do not block X's original behavior.

## 兼容性

- 静态 scope：仅 `com.twitter.android`。
- X `12.20.5-prod.01`：模块、链接、媒体、过滤、敏感媒体、高质量视频与浏览历史 Hook 已在设备回归中加载。
- X `12.19.1-release.0`：保留已验证的精确目标。
- X `12.20.5-prod.01` 的 `poll.results` 仍可能显示 `FAIL`，属于后续适配项；其他 Hook 组保持独立运行。
- X 更新可能改变混淆目标；目标不匹配时 XTQ 保留 X 原行为。

## Compatibility

- Static scope: `com.twitter.android` only.
- On X `12.20.5-prod.01`, the module, link, media, filtering, sensitive-media, high-quality-video, and browsing-history hooks have loaded in device regression.
- X `12.19.1-release.0`: its verified exact target is retained.
- `poll.results` on X `12.20.5-prod.01` may still show `FAIL` and remains a follow-up compatibility item; other Hook groups continue to run independently.
- X updates may change obfuscated targets; when a target does not match, XTQ preserves X's original behavior.
