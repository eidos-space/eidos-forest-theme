# 森林主题

为 Eidos Lite 提供暖纸浅色和深森林暗色配色。

需要 **Eidos Lite 0.29.0** 及以上版本，支持插件 API **3.7.0**。名称和文档跟随应用语言。

## 安装与使用

从插件市场或项目的 GitHub Release 安装归档，打开 **插件 → 森林 → 应用主题**。主题在本机所有 Space 生效；Lite 的浅色、深色或跟随系统设置决定使用哪套配色。点击 **使用默认主题** 可恢复内置外观，卸载当前主题也会恢复。

安装包只有经过验证的 CSS，不包含可执行代码、网络访问、远程字体或 Space 文件访问权限。CLI Serve、Android 和 iOS 不支持此宿主主题。

## 开发

使用 Node.js 22.12 及以上版本，以及固定的公开 SDK/tools 0.9.0：

```sh
npm ci
npm run check
npm run pack:plugin
```

归档及 SHA-256 校验文件位于 `dist/`。
