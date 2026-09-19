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

当前公开版本：`12.27.0-prod.01`（versionCode 42）。

Current public release: `12.27.0-prod.01` (versionCode 42).

主要适配并已验证：X `12.27.0-prod.01`（versionCode `312252001`）。

Primary verified compatibility: X `12.27.0-prod.01` (versionCode `312252001`).

本次适配 X 12.27.0，修复视频下载、当前媒体选择与图库路由，补充原生隐藏的可下载视频入口，并调整翻译调度。已有功能和设置默认值保留。

This update supports X 12.27.0, fixes video downloading, current-media selection and gallery routing, exposes eligible hidden download actions, and adjusts translation pacing. Existing features and defaults are preserved.

每次 X 更新后，我都需要重新分析适配变化、构建候选并逐项实机验证。如果这些工作对你有帮助，欢迎给项目一个 Star。每一颗 Star 都是对我的鼓励。

After each X update, I work through compatibility changes, build candidates, and test features on a real device. If this helps you, please consider starring the project. Every Star is meaningful encouragement.

## 功能

- **浏览历史**：在 X 内注入的侧边栏浏览历史，仅记录用户明确打开的帖子、视频或 GIF；不会记录滚动曝光、自动播放或仅查看图片。历史仅保留在本机并保持私密，支持重新打开记录和清空历史，不上传任何数据。
- **链接净化**：净化剪贴板、分享和应用内跳转中的 X 链接跟踪参数，并支持选择或配置分享域名。
- **原图与媒体下载**：图片查看页提供“保存原图”和多图“全部保存”；图片保存按钮与视频/GIF 下载接管分别控制，关闭后保留 X 的原生保存或下载方式。视频与 GIF 下载优先选择非 HLS 最高码率直链；开启视频接管时，为原生隐藏下载项且有有效下载文件的视频补出入口。
- **原生翻译增强**：复用 X 原生翻译自动处理符合条件的短帖和回复，在自动翻译结果中保留原文；目标语言默认跟随 X，也可明确选择固定语言。空正文会跳过，待处理内容会及时刷新，手动翻译路径保持不变。
- **内容过滤**：隐藏推广内容、推广用户、视频轮播、资料推荐和横幅；广告帖子过滤覆盖帖子详情中的嵌套模块。
- **视频播放控制**：可选关闭视频播放结束后自动进入下一个视频；该选项与帖子内横向轮播独立，仍可手动切换，默认关闭。
- **媒体显示选项**：提供敏感媒体显示和高质量视频选项。
- **设置与反馈**：设置按类别分组并支持展开或收起，调整会自动保存并显示保存反馈；浏览历史入口随 X 语言本地化。
- **动态适配与兼容性回退**：功能开关、媒体字段、帖子和作者读取支持经过校验的动态识别与缓存回退；不匹配时保留 X 原生行为。此能力不代表所有功能或未来 X 版本均能自动兼容。

## Features

- **Browsing history**: Injected inside X's sidebar, local browsing history records only posts, videos, or GIFs that the user explicitly opens; it does not record scroll exposure, autoplay, or image-only viewing. History stays local and private, supports reopening entries and clearing history, and uploads no data.
- **Link cleanup**: Cleans tracking parameters from X links copied, shared, or opened in the app, with selectable and configurable share domains.
- **Original images and media downloads**: Adds “Save original” and multi-image “Save all” actions to the image viewer; image save buttons and video/GIF download takeover are controlled separately, and turning either off keeps X's native save or download behavior. Video and GIF downloads prefer the highest-bitrate non-HLS direct variant. With takeover enabled, eligible videos with a supported file gain a download action even when the native menu hides it.
- **Native translation enhancements**: Reuses X's native translation flow to automatically translate eligible short posts and replies while preserving the original text; the target follows X by default or can be set explicitly. Empty bodies are skipped and pending work is refreshed promptly; manual translation remains unchanged.
- **Content filtering**: Hides promoted content, promoted users, video carousels, profile recommendations, and banners; promoted-post filtering also covers nested modules in post details.
- **Video playback control**: Optionally stops automatic movement to the next video after playback; this is independent of the in-post horizontal carousel, and videos remain switchable manually. It is off by default.
- **Media display options**: Provides sensitive-media display and high-quality video options.
- **Settings and feedback**: Groups settings into collapsible categories, saves changes automatically with save feedback, and localizes the browsing-history entry to X's language.
- **Dynamic adaptation and fallback**: Validated discovery and cached fallback for feature switches, media fields, and post/author readers; unmatched targets preserve X's native behavior. This does not guarantee automatic compatibility for every feature or future X version.

## 兼容性

- 静态 scope：仅 `com.twitter.android`。
- X `12.27.0-prod.01`（`312270001`）：在实机验证视频菜单补出与下载；既有功能保留，验证范围见本次 Release。
- 本次未重新验证其他 X 版本；旧版验证记录请参阅历史 Release。
- X 更新可能改变内部适配目标；目标不匹配时 XTQ 保留 X 原行为。

## Compatibility

- Static scope: `com.twitter.android` only.
- X `12.27.0-prod.01` (`312270001`): Video menu availability and downloads were verified on a real device. Existing features are preserved; see this Release for verification scope.
- Other X versions were not retested for this release; earlier verification is documented in previous releases.
- X updates may change internal compatibility targets; when a target does not match, XTQ preserves X's original behavior.
