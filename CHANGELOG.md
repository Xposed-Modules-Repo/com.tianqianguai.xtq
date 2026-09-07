# Changelog

## 12.23.1-prod.01（versionCode 26）

### 中文

- 版本号对应已验证的主要适配版本 X `12.23.1-prod.01`（versionCode `312231001`）。
- 完成 X `12.23.1-prod.01` 的链接、媒体、过滤、敏感媒体、高质量视频、浏览历史与翻译适配。
- 自动翻译覆盖符合条件的短帖和回复，自动结果保留原文；目标语言默认跟随 X，也可明确选择固定语言。空正文会跳过，待处理内容会及时刷新，手动翻译路径保持不变。
- 图片保存按钮与视频/GIF 下载接管改为独立开关；关闭后分别保留 X 原生保存或下载方式。
- 新增可选的“不自动跳到下一个视频”设置，与帖子内横向轮播独立，仍可手动切换；既有设置默认值保持不变，该新设置默认关闭。
- 设置按类别分组并支持展开或收起，调整会自动保存并显示保存反馈；浏览历史抽屉入口随 X 语言本地化。
- 广告帖子过滤覆盖帖子详情中的嵌套模块。
- 延续浏览历史、链接净化、原图与媒体下载、广告/推广过滤、敏感媒体直显和清晰视频等既有功能。
- 本版本没有新增用户可见功能移除。

### English

- The version name matches the verified primary target, X `12.23.1-prod.01` (versionCode `312231001`).
- Adapts link, media, filtering, sensitive-media, high-quality-video, browsing-history, and translation behavior for X `12.23.1-prod.01`.
- Automatic translation now covers eligible short posts and replies while preserving the original text; the target follows X by default or can be set explicitly. Empty bodies are skipped, pending work is refreshed promptly, and manual translation remains unchanged.
- Image save buttons and video/GIF download takeover are separate switches; turning either off keeps X's native save or download behavior.
- Adds an optional “Do not automatically move to the next video” setting, independent of the in-post horizontal carousel; videos remain switchable manually, existing defaults are unchanged, and the new setting is off by default.
- Groups settings into collapsible categories, saves changes automatically with save feedback, and localizes the browsing-history drawer entry to X's language.
- Promoted-post filtering now covers nested modules in post details.
- Preserves existing browsing history, link cleanup, original-image and media downloads, ad/promoted-content filtering, sensitive-media display, and high-quality-video features.
- No additional user-visible features were removed in this release.

## 12.21.1-prod.05（versionCode 20）

### 中文

- 版本号直接对应主要适配的 X `12.21.1-prod.05`，便于快速识别兼容版本。
- 新增 X 原生短帖自动翻译，并在自动翻译结果中保留原文；手动翻译路径保持不变。
- 图片查看页新增“保存原图”和多图“全部保存”，视频与 GIF 下载行为保持不变。
- 完成 X `12.21.1-prod.05` 的链接、媒体、过滤、浏览历史与翻译目标适配。
- 移除不受支持的投票结果增强和媒体 URL 复制操作。
- 更新 XTQ 桌面图标。

### English

- The version name now directly matches the primary target, X `12.21.1-prod.05`, for immediate compatibility identification.
- Adds automatic short-post translation through X's native flow and preserves the original text in automatic results; manual translation remains unchanged.
- Adds “Save original” and multi-image “Save all” actions to the image viewer while preserving video and GIF download behavior.
- Adapts link, media, filtering, browsing-history, and translation targets for X `12.21.1-prod.05`.
- Removes the unsupported poll-result enhancement and media URL-copy actions.
- Updates the XTQ launcher icon.

## 0.0.1

- 首个官方公开版本。
- 支持链接净化、媒体操作与下载、内容过滤和媒体显示增强。
- 支持 X 内本地浏览历史与独立 Hook 诊断。
- 适配 X 12.20.5 与 12.19.1 的已验证目标；12.20.5 的投票结果增强仍待继续适配。
