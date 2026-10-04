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

当前公开版本：`12.31.0-prod.01`（versionCode 56）。<br>
Current public release: `12.31.0-prod.01` (versionCode 56).

主要适配版本：X `12.31.0-prod.01`（`312310001`）。<br>
Primary supported X version: `12.31.0-prod.01` (`312310001`).

## 本版更新 / This release

- 适配 X 12.31.0-prod.01，恢复浏览历史入口与记录、自动翻译的原文与译文显示，以及广告过滤。<br>
  Supports X 12.31.0-prod.01, restoring browsing-history access and recording, original-plus-translated text, and ad filtering.
- 修复新版视频下载、原图保存与自定义命名；单媒体文件不再额外添加 `_1`，多媒体保留序号。<br>
  Fixes video downloads, original-image saving and custom filenames in the new X version; single-media files no longer get an extra `_1`, while multiple files retain their sequence numbers.
- 修复最高画质选择和停止自动播放下一条视频，保留手动切换。<br>
  Fixes highest-quality playback selection and stopping automatic advance to the next video while preserving manual switching.
- 新增“优先使用 Re:X”选项，默认关闭；开启后让出指定重叠功能并隐藏对应设置，关闭后恢复 XTQ 控制与原设置值。<br>
  Adds an optional “Prefer Re:X” mode, off by default. It yields selected overlapping features and hides their controls; turning it off restores XTQ control and saved settings.

## 功能 / Features

- **浏览历史**：在 X 内注入的侧边栏浏览历史，仅记录用户明确打开的帖子、视频或 GIF；不会记录滚动曝光、自动播放或仅查看图片。历史仅保留在本机并保持私密，支持重新打开记录和清空历史，不上传任何数据。<br>
  **Browsing history**: Injected inside X's sidebar, local browsing history records only posts, videos, or GIFs that the user explicitly opens; it does not record scroll exposure, autoplay, or image-only viewing. History stays local and private, supports reopening entries and clearing history, and uploads no data.
- **链接净化**：净化剪贴板、分享和应用内跳转中的 X 链接跟踪参数，并支持选择或配置分享域名。<br>
  **Link cleanup**: Cleans tracking parameters from X links copied, shared, or opened in the app, with selectable and configurable share domains.
- **原图与媒体下载**：图片查看页提供“保存原图”和多图“全部保存”，图片按钮与视频/GIF 下载接管分别控制；XTQ 管理的图片保存使用自定义目录和命名，默认配置保留 X 原生图片保存行为。视频与 GIF 下载优先选择非 HLS 最高码率直链；开启视频接管时，为原生隐藏下载项且有有效下载文件的视频补出入口。<br>
  **Original images and media downloads**: Adds “Save original” and multi-image “Save all” actions, with separate controls for image buttons and video/GIF download takeover. Images saved through XTQ use its custom folders and filenames; default settings retain X's native image saving. Video and GIF downloads prefer the highest-bitrate non-HLS direct variant. With takeover enabled, eligible videos with a supported file gain a download action even when the native menu hides it.
- **原生翻译增强**：复用 X 原生翻译自动处理符合条件的短帖和回复，在自动翻译结果中保留原文；目标语言默认跟随 X，也可明确选择固定语言。空正文会跳过，待处理内容会及时刷新，手动翻译路径保持不变。<br>
  **Native translation enhancements**: Reuses X's native translation flow to automatically translate eligible short posts and replies while preserving the original text; the target follows X by default or can be set explicitly. Empty bodies are skipped and pending work is refreshed promptly; manual translation remains unchanged.
- **内容过滤**：隐藏推广内容、推广用户、视频轮播、资料推荐和横幅；广告帖子过滤覆盖帖子详情中的嵌套模块。<br>
  **Content filtering**: Hides promoted content, promoted users, video carousels, profile recommendations, and banners; promoted-post filtering also covers nested modules in post details.
- **视频播放控制**：可选关闭视频播放结束后自动进入下一个视频；该选项与帖子内横向轮播独立，仍可手动切换，默认关闭。<br>
  **Video playback control**: Optionally stops automatic movement to the next video after playback; this is independent of the in-post horizontal carousel, and videos remain switchable manually. It is off by default.
- **媒体显示选项**：提供敏感媒体显示和高质量视频选项。<br>
  **Media display options**: Provides sensitive-media display and high-quality video options.
- **设置与反馈**：设置按类别分组并支持展开或收起，调整会自动保存并显示保存反馈；浏览历史入口随 X 语言本地化。<br>
  **Settings and feedback**: Groups settings into collapsible categories, saves changes automatically with save feedback, and localizes the browsing-history entry to X's language.
- **桌面图标**：可选隐藏 XTQ 的系统桌面图标；仍可从 LSPosed 模块管理中打开 XTQ 设置，默认显示。<br>
  **Launcher icon**: Optionally hides the XTQ icon from the system launcher; XTQ settings remain available from the LSPosed module manager, and the icon is shown by default.
- **动态适配与兼容性回退**：功能开关、媒体字段、帖子和作者读取支持经过校验的动态识别与缓存回退；不匹配时保留 X 原生行为。此能力不代表所有功能或未来 X 版本均能自动兼容。<br>
  **Dynamic adaptation and fallback**: Validated discovery and cached fallback for feature switches, media fields, and post/author readers; unmatched targets preserve X's native behavior. This does not guarantee automatic compatibility for every feature or future X version.
- **配置迁移**：支持 JSON 设置导入与导出，不导出浏览历史。<br>
  **Settings transfer**: Imports and exports settings as JSON without browsing history.
- **下载命名**：提供账号名、昵称、用户 ID、帖子 ID 及时间戳等命名格式；单媒体不加多余序号，多媒体保留序号。<br>
  **Download filenames**: Offers naming formats using usernames, display names, user IDs, post IDs, or timestamps; single-media files omit an unnecessary sequence suffix and multiple files retain their sequence numbers.
- **自动刷新控制**：可保留重启或返回首页时的缓存内容，手动刷新和无缓存加载保持可用，默认关闭。<br>
  **Automatic refresh control**: Can retain cached Home content across restarts and returns; manual refresh and loading without a cache remain available. Off by default.
- **首页直播空间栏**：可选隐藏首页直播与 Spaces 栏，空间功能和其他入口保留，默认关闭。<br>
  **Home live and Spaces bar**: Optionally hides the Home bar while preserving Spaces and other entry points. Off by default.

- **Re:X 共存**：可选“优先使用 Re:X”，默认关闭；让出指定重叠功能并隐藏对应设置，原设置值仍保留。浏览历史、翻译、XTQ 图片保存、最高画质和停止自动连播仍由 XTQ 控制。Re:X 视频下载的目录与命名由 Re:X 配置；此选项不会自动启用 Re:X 或修改其配置。<br>
  **Re:X coexistence**: Optional “Prefer Re:X” mode is off by default. It yields selected overlapping features and hides their controls while preserving saved values. Browsing history, translation, XTQ image saving, highest-quality playback and stop-auto-advance remain under XTQ control. Re:X manages its own video download folders and filenames; this option does not enable Re:X or modify its configuration.

## 兼容性 / Compatibility

- 作用范围仅为 `com.twitter.android`。<br>
  Scope is limited to `com.twitter.android`.
- 本版主要适配 X 12.31.0-prod.01；其他版本的兼容记录请参阅对应历史 Release。<br>
  This release targets X 12.31.0-prod.01; see the corresponding past releases for other-version compatibility records.
- X 更新可能改变内部适配目标；不匹配时保留 X 原行为，不承诺未来版本自动兼容。<br>
  X updates may change compatibility targets; unmatched targets preserve X behavior, and future-version compatibility is not guaranteed.

每次 X 更新后，我都需要分析变化、构建候选并进行实机验证。<br>
After each X update, I analyze changes, build candidates, and test on real devices.

如果 XTQ 对你有帮助，欢迎给项目一个 Star。每一颗 Star 都是对我的鼓励。<br>
If XTQ helps you, please consider starring the project. Every Star is meaningful encouragement.
https://github.com/Xposed-Modules-Repo/com.tianqianguai.xtq
