# Changelog

## 12.28.0-prod.01（versionCode 45）

- 适配 X 12.28.0-prod.01。
- Supports X 12.28.0-prod.01.
- 恢复该版本的翻译、浏览历史、图库、视频下载、最高画质和停止自动连播流程；目标不匹配时保留 X 原生行为。
- Restores the translation, browsing-history, gallery, video-download, highest-quality, and stop-auto-advance flows for this version; unmatched targets preserve X's native behavior.
- 新增“隐藏桌面图标”设置：启用后隐藏 XTQ 的系统桌面图标，仍可从 LSPosed 模块管理中打开 XTQ 设置；默认显示。
- Adds a “Hide desktop icon” setting. When enabled, it hides XTQ from the system launcher while settings remain available from the LSPosed module manager; the icon is shown by default.
- 保留已有功能和设置默认值；本版本没有移除用户可见功能。
- Existing features and setting defaults are preserved; no user-visible feature was removed.

## 12.27.1-prod.01（versionCode 44）

### 中文

- 修复视频下载失效和最高画质适配；已有功能和设置默认值保留。

### English

- Fixes video downloading and highest-quality adaptation while preserving existing features and defaults.

## 12.27.1-prod.01（versionCode 43）

### 中文

- 适配 X 12.27.1，修复帖子/作者读取、详情过滤、图库、视频下载和最高画质契约。
- 修复帖子/作者读取、详情过滤、图库和视频契约，保留已有功能和设置默认值。

### English

- Supports X 12.27.1 and fixes post/author readers, detail filtering, gallery, video downloads and highest-quality contracts.
- Fixes post/author readers, detail filtering, gallery and video contracts while preserving existing features and defaults.

## 12.27.0-prod.01（versionCode 42）

### 中文

- 适配 X **12.27.0-prod.01**，保留浏览历史、翻译、链接净化、媒体下载、过滤和视频控制，设置默认值不变，无功能移除。
- 修复视频下载被误判为图片，以及错误带入相邻视频的问题；保存当前视频的最高有效码率文件。
- 开启“视频下载接管”时，为原生隐藏下载项、但具有可下载文件的视频补出下载入口。
- 修复图库路由监听，调整翻译请求超时和调度节奏；关闭下载操作弹窗后直接保存。
- 已在 X 12.27.0 实机验证。本次未重跑其他 X 版本和所有旧功能的完整交互矩阵；不承诺所有视频格式均可下载。


### English

- Adapts to X **12.27.0-prod.01**, preserving browsing history, translation, link cleanup, downloads, filtering and video controls. Defaults are unchanged; no features were removed.
- Fixes videos being mistaken for cover images and unrelated videos being included. Saves the current video's highest valid bitrate file.
- With video download takeover enabled, exposes a download action for videos whose native menu hides it when a downloadable file is available.
- Fixes gallery route tracking, adjusts translation timeout and pacing, and saves directly when the action dialog is disabled.
- Verified on a real device running X 12.27.0. Other X versions and the full existing-feature interaction matrix were not retested. Not all video formats are supported.


## 12.25.2-prod.01（versionCode 40）

### 中文

- 保留浏览历史、链接净化、媒体下载、翻译、内容过滤和视频播放控制，已有设置默认值不变，无功能移除。
- 适配 X `12.25.2-prod.01`（`312252001`）。
- 功能开关、媒体字段及帖子/作者读取新增动态识别与缓存回退；不代表所有功能或未来版本均可自动适配。
- 修复回复页面重建后翻译被错误去重，以及敏感媒体未直接显示的问题。
- 更新视频事件与图库生命周期适配。
- 381 项单元测试通过；三种动态解析路径共 72 项过程检查通过。最终安装包实测帖子双语、历史保存/重启保留/重新打开和视频下载，下载文件完整解码通过。
- 本次未重新验证其他 X 版本，也未重跑所有旧功能的完整交互矩阵。

### English

- Preserves browsing history, link cleanup, media downloads, translation, filtering, and video playback controls. Existing defaults are unchanged; no features were removed.
- Supports X `12.25.2-prod.01` (`312252001`).
- Adds dynamic discovery and cached fallback for feature switches, media fields, and post/author readers; this is not universal or future-version compatibility.
- Fixes reply translation being incorrectly deduplicated after page recreation and sensitive media not displaying directly.
- Updates video-event and gallery-lifecycle compatibility.
- Passed 381 unit tests and 72 process checks across three resolution paths. The final APK passed bilingual post display, history saving/restart persistence/reopening, and video downloading with a complete decode check.
- Other X versions and the complete interaction matrix of all existing features were not retested for this release.

## 12.25.0-prod.01（versionCode 36）

### 中文

- 保留浏览历史、链接净化、原图与媒体下载、内容过滤、翻译和视频播放控制等已有功能，设置默认值保持不变。
- 适配 X `12.25.0-prod.01`（`312250001`）。
- 修复部分回复未自动翻译或只显示译文的问题，自动翻译完成后同时保留原文。
- 修复退出图片查看页后“保存原图”按钮残留的问题，覆盖系统返回、工具栏返回与边缘返回。
- 修复打开视频或翻页时误触发下载的问题；用户明确下载后只生成对应文件，后续翻页不追加下载。
- 实机验证回复双语、原图保存、图片返回和视频下载；本次未重新验证其他 X 版本。
- 本次没有新增用户可见功能移除。

### English

- Preserves browsing history, link cleanup, original-image and media downloads, filtering, translation, and video playback controls, with unchanged setting defaults.
- Adapts to X `12.25.0-prod.01` (`312250001`).
- Fixes replies that did not translate automatically or showed only the translation; completed automatic translations now retain the original text.
- Fixes lingering Save Original controls after system Back, toolbar Back, and edge-back gestures.
- Fixes unintended downloads when opening or changing videos. Explicit downloads save the selected content without adding downloads on later page changes.
- Verified bilingual replies, original-image saving, viewer exit, and video downloading on a real device. Other X versions were not retested for this release.
- No additional user-visible features were removed.

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

### 中文

- 首个官方公开版本。
- 支持链接净化、媒体操作与下载、内容过滤和媒体显示增强。
- 支持 X 内本地浏览历史与独立 Hook 诊断。
- 适配 X 12.20.5 与 12.19.1 的已验证目标。
- X 12.20.5 的投票结果增强仍待继续适配。

### English

- First official public release.
- Supports link cleanup, media actions and downloads, content filtering, and media display enhancements.
- Includes local browsing history inside X and independent Hook diagnostics.
- Adapts the verified targets for X 12.20.5 and X 12.19.1.
- The poll-result enhancement for X 12.20.5 remained to be adapted.
