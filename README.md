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

当前公开版本：`12.29.1-prod.01`（versionCode 46）。<br>
Current public release: `12.29.1-prod.01` (versionCode 46).

主要适配版本：X `12.29.1-prod.01`（`312291001`）。<br>
Primary supported X version: `12.29.1-prod.01` (`312291001`).

## 本版更新 / This release

- 适配 X 12.29.1-prod.01。<br>
  Supports X 12.29.1-prod.01.
- 新增配置导入与导出，可通过 JSON 文件迁移设置；不包含浏览历史。<br>
  Adds settings import and export through JSON files for migration; browsing history is excluded.
- 新增媒体文件命名选项：账号名、昵称或用户 ID 搭配帖子 ID，也可选择仅帖子 ID 或时间戳；默认保留原命名规则。<br>
  Adds media filename options: username, display name, or user ID with the post ID, post ID only, or timestamp; existing naming remains the default.
- 新增阻止自动刷新开关：重启 X 或返回首页时保留已有缓存，手动下拉刷新及无缓存时的加载仍可使用。<br>
  Adds an option to prevent automatic refresh, keeping cached Home posts after restarting X or returning to Home while preserving manual pull-to-refresh and loading without a cache.
- 新增隐藏首页直播与 Spaces 栏的开关，默认关闭，不关闭空间功能。<br>
  Adds an option to hide the Home live and Spaces bar, off by default, while keeping Spaces available.
- 修复隐藏桌面图标后无法从 LSPosed 模块管理打开 XTQ 设置的问题。<br>
  Fixes opening XTQ settings from the LSPosed module manager when the launcher icon is hidden.

## 功能 / Features

- **浏览历史**：在 X 内注入的侧边栏浏览历史，仅记录用户明确打开的帖子、视频或 GIF；不会记录滚动曝光、自动播放或仅查看图片。历史仅保留在本机并保持私密，支持重新打开记录和清空历史，不上传任何数据。<br>
  **Browsing history**: Injected inside X's sidebar, local browsing history records only posts, videos, or GIFs that the user explicitly opens; it does not record scroll exposure, autoplay, or image-only viewing. History stays local and private, supports reopening entries and clearing history, and uploads no data.
- **链接净化**：净化剪贴板、分享和应用内跳转中的 X 链接跟踪参数，并支持选择或配置分享域名。<br>
  **Link cleanup**: Cleans tracking parameters from X links copied, shared, or opened in the app, with selectable and configurable share domains.
- **原图与媒体下载**：图片查看页提供“保存原图”和多图“全部保存”；图片保存按钮与视频/GIF 下载接管分别控制，关闭后保留 X 的原生保存或下载方式。视频与 GIF 下载优先选择非 HLS 最高码率直链；开启视频接管时，为原生隐藏下载项且有有效下载文件的视频补出入口。<br>
  **Original images and media downloads**: Adds “Save original” and multi-image “Save all” actions to the image viewer; image save buttons and video/GIF download takeover are controlled separately, and turning either off keeps X's native save or download behavior. Video and GIF downloads prefer the highest-bitrate non-HLS direct variant. With takeover enabled, eligible videos with a supported file gain a download action even when the native menu hides it.
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
- **下载命名**：提供账号名、昵称、用户 ID、帖子 ID 及时间戳等命名格式。<br>
  **Download filenames**: Offers naming formats using usernames, display names, user IDs, post IDs, or timestamps.
- **自动刷新控制**：可保留重启或返回首页时的缓存内容，手动刷新和无缓存加载保持可用，默认关闭。<br>
  **Automatic refresh control**: Can retain cached Home content across restarts and returns; manual refresh and loading without a cache remain available. Off by default.
- **首页直播空间栏**：可选隐藏首页直播与 Spaces 栏，空间功能和其他入口保留，默认关闭。<br>
  **Home live and Spaces bar**: Optionally hides the Home bar while preserving Spaces and other entry points. Off by default.

## 兼容性 / Compatibility

- 作用范围仅为 `com.twitter.android`。<br>
  Scope is limited to `com.twitter.android`.
- 主要适配 X 12.29.1-prod.01，保留 X 12.28.0 分支；其他旧版记录请参阅历史 Release。<br>
  Targets X 12.29.1-prod.01 and retains the X 12.28.0 branch; see past releases for earlier-version records.
- X 更新可能改变内部适配目标；不匹配时保留 X 原行为，不承诺未来版本自动兼容。<br>
  X updates may change compatibility targets; unmatched targets preserve X behavior, and future-version compatibility is not guaranteed.

每次 X 更新后，我都需要分析变化、构建候选并进行实机验证。<br>
After each X update, I analyze changes, build candidates, and test on real devices.

如果 XTQ 对你有帮助，欢迎给项目一个 Star。每一颗 Star 都是对我的鼓励。<br>
If XTQ helps you, please consider starring the project. Every Star is meaningful encouragement.
https://github.com/Xposed-Modules-Repo/com.tianqianguai.xtq
