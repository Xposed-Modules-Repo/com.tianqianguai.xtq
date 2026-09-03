# Changelog

## 12.21.1-prod.05（versionCode 20）

### 中文

- 版本号直接对应主要适配的 X `12.21.1-prod.05`，便于快速识别兼容版本。
- 新增 X 原生短帖自动翻译，并在自动翻译结果中保留原文；手动翻译路径保持不变。
- 图片查看页新增“保存原图”和多图“全部保存”，视频与 GIF 下载行为保持不变。
- 完成 X `12.21.1-prod.05` 的链接、媒体、过滤、浏览历史与翻译目标适配。
- 移除不受支持的投票结果增强和媒体 URL 复制操作。
- 更新 XTQ 桌面图标。
- Release APK 继续启用 R8 代码/资源优化、重打包和入口混淆，并沿用原 XTQ Release 签名。

### English

- The version name now directly matches the primary target, X `12.21.1-prod.05`, for immediate compatibility identification.
- Adds automatic short-post translation through X's native flow and preserves the original text in automatic results; manual translation remains unchanged.
- Adds “Save original” and multi-image “Save all” actions to the image viewer while preserving video and GIF download behavior.
- Adapts link, media, filtering, browsing-history, and translation targets for X `12.21.1-prod.05`.
- Removes the unsupported poll-result enhancement and media URL-copy actions.
- Updates the XTQ launcher icon.
- The Release APK continues to use R8 code/resource optimization, repackaging, and entry-point obfuscation, signed with the existing XTQ Release key.

## 0.0.1

- 首个官方公开版本。
- 支持链接净化、媒体操作与下载、内容过滤和媒体显示增强。
- 支持 X 内本地浏览历史与独立 Hook 诊断。
- Release APK 启用 R8 代码/资源优化、重打包和入口混淆。
- 适配 X 12.20.5 与 12.19.1 的已验证目标；12.20.5 的投票结果增强仍待继续适配。
