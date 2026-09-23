# Forest 主题

Forest 是一个可独立安装的 **Eidos Lite 宿主主题插件**，为整个应用提供暖纸色浅色界面和深森林色深色界面。它不是某个插件视图的主题，也不会按 Space 单独启用。

简短的 [`plugin.json`](plugin.json) 指向 [`theme.css`](theme.css)；CSS 包含背景、文字、侧栏、状态色、交互状态、字体和少量布局变量。插件包只有经过校验的 CSS，没有 JavaScript、远程字体、网络权限或 Space 数据访问权限。

## 安装与使用

需要支持 **Plugin API 1.6.0** 的 Eidos Lite 开发版本。现有已发布的旧版 Lite 无法安装本主题。

1. 在 Lite 中打开 **插件 → 安装插件…**，选择 `dist/eidos.forest-theme-0.1.0.eidos-plugin`；也可以把该文件拖到插件管理器。
2. 打开 **Forest** 详情，点击 **应用主题**。
3. Lite 的浅色、深色或跟随系统设置仍决定使用 `light` 或 `dark` 配色。主题选择对这台设备上的所有 Space 生效。
4. 点击 **使用默认主题** 可取消应用。卸载当前主题也会恢复默认界面。

## 从源码检查与打包

当前 npm 上的 `@eidos.space/plugin-tools` 0.2.0 尚不支持主题插件。请指向包含 Plugin API 1.6.0 工具的 Eidos 源码检出：

```sh
export EIDOS_REPO_DIR=/absolute/path/to/eidos
cd eidos-forest-theme
npm run check
npm run pack:plugin
```

打包会生成 `.eidos-plugin` 和相邻的 `.sha256` 校验和文件。主题无需安装 npm 依赖。CLI Serve 不支持运行主题；CLI 仅可用于创建、检查和打包。
