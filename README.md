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
  如果 XTQ 对你有帮助，欢迎点一个 Star。每一颗 Star 都是对我的鼓励 ⭐
  <br>
  If XTQ helps you, please consider leaving a Star. Every Star is meaningful encouragement.
</p>

当前公开版本：`12.23.1-prod.01`（versionCode 26）。

Current public release: `12.23.1-prod.01` (versionCode 26).

主要适配并已验证：X `12.23.1-prod.01`（versionCode `312231001`）。

Primary verified compatibility: X `12.23.1-prod.01` (versionCode `312231001`).

## 功能

- **浏览历史**：在 X 内注入的侧边栏浏览历史，仅记录用户明确打开的帖子、视频或 GIF；不会记录滚动曝光、自动播放或仅查看图片。历史仅保留在本机并保持私密，支持重新打开记录和清空历史，不上传任何数据。
- **链接净化**：净化剪贴板、分享和应用内跳转中的 X 链接跟踪参数，并支持选择或配置分享域名。
- **原图与媒体下载**：图片查看页提供“保存原图”和多图“全部保存”；图片保存按钮与视频/GIF 下载接管分别控制，关闭后保留 X 的原生保存或下载方式。视频与 GIF 下载优先选择非 HLS 最高码率直链。
- **原生翻译增强**：复用 X 原生翻译自动处理符合条件的短帖和回复，在自动翻译结果中保留原文；目标语言默认跟随 X，也可明确选择固定语言。空正文会跳过，待处理内容会及时刷新，手动翻译路径保持不变。
- **内容过滤**：隐藏推广内容、推广用户、视频轮播、资料推荐和横幅；广告帖子过滤覆盖帖子详情中的嵌套模块。
- **视频播放控制**：可选关闭视频播放结束后自动进入下一个视频；该选项与帖子内横向轮播独立，仍可手动切换，默认关闭。
- **媒体显示选项**：提供敏感媒体显示和高质量视频选项。
- **设置与反馈**：设置按类别分组并支持展开或收起，调整会自动保存并显示保存反馈；浏览历史入口随 X 语言本地化。
- **独立 Hook 组**：各 Hook 组独立失败并保持 fail-open，不阻止 X 原行为。

## Features

- **Browsing history**: Injected inside X's sidebar, local browsing history records only posts, videos, or GIFs that the user explicitly opens; it does not record scroll exposure, autoplay, or image-only viewing. History stays local and private, supports reopening entries and clearing history, and uploads no data.
- **Link cleanup**: Cleans tracking parameters from X links copied, shared, or opened in the app, with selectable and configurable share domains.
- **Original images and media downloads**: Adds “Save original” and multi-image “Save all” actions to the image viewer; image save buttons and video/GIF download takeover are controlled separately, and turning either off keeps X's native save or download behavior. Video and GIF downloads prefer the highest-bitrate non-HLS direct variant.
- **Native translation enhancements**: Reuses X's native translation flow to automatically translate eligible short posts and replies while preserving the original text; the target follows X by default or can be set explicitly. Empty bodies are skipped and pending work is refreshed promptly; manual translation remains unchanged.
- **Content filtering**: Hides promoted content, promoted users, video carousels, profile recommendations, and banners; promoted-post filtering also covers nested modules in post details.
- **Video playback control**: Optionally stops automatic movement to the next video after playback; this is independent of the in-post horizontal carousel, and videos remain switchable manually. It is off by default.
- **Media display options**: Provides sensitive-media display and high-quality video options.
- **Settings and feedback**: Groups settings into collapsible categories, saves changes automatically with save feedback, and localizes the browsing-history entry to X's language.
- **Independent Hook groups**: Hook groups fail independently and remain fail-open, so they do not block X's original behavior.

## 兼容性

- 静态 scope：仅 `com.twitter.android`。
- X `12.23.1-prod.01`（versionCode `312231001`）：XTQ26 的链接、媒体、过滤、敏感媒体、高质量视频、浏览历史、翻译、设置与视频行为已在设备回归中验证。
- X 更新可能改变内部适配目标；目标不匹配时 XTQ 保留 X 原行为。

## Compatibility

- Static scope: `com.twitter.android` only.
- On X `12.23.1-prod.01` (versionCode `312231001`), XTQ26's link, media, filtering, sensitive-media, high-quality-video, browsing-history, translation, settings, and video-behavior changes were verified on device.
- X updates may change internal compatibility targets; when a target does not match, XTQ preserves X's original behavior.
