# Forest theme

Forest is a standalone **Eidos Lite host theme plugin**. It gives the whole app a warm paper palette in light mode and a deep forest palette in dark mode. It does not target an individual plugin view or enable separately in each Space.

[`plugin.json`](plugin.json) points to [`theme.css`](theme.css), which declares backgrounds, text, sidebar, status colors, interaction states, fonts, and a few layout tokens. The archive contains only validated CSS: no JavaScript, remote fonts, network permission, or access to Space data.

## Install and use

Forest requires an Eidos Lite development build with **Plugin API 1.6.0**. Older published Lite versions cannot install it.

1. In Lite, choose **Plugins → Install plugin…** and select `dist/eidos.forest-theme-0.1.0.eidos-plugin`, or drop the archive into Plugin Manager.
2. Open **Forest** and choose **Apply theme**.
3. Lite's light, dark, or system appearance setting still selects the corresponding palette. The theme selection applies to every Space on this device.
4. Choose **Use default theme** to clear the selection. Uninstalling an active theme also restores the default interface.

## Check and package from source

The currently published `@eidos.space/plugin-tools` 0.2.0 does not yet support theme plugins. Point the scripts at an Eidos source checkout containing Plugin API 1.6.0 tooling:

```sh
export EIDOS_REPO_DIR=/absolute/path/to/eidos
cd eidos-forest-theme
npm run check
npm run pack:plugin
```

Packing writes a `.eidos-plugin` archive and adjacent `.sha256` checksum to `dist/`. This theme needs no npm dependencies. CLI Serve cannot run themes; the CLI can create, check, and pack them.
