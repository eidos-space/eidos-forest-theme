# Forest

Forest gives Eidos Lite a warm paper light palette and a deep forest dark palette.

Requires **Eidos Lite 0.29.0 or later**, with Plugin API **3.7.0**. Names and documentation follow the app language.

## Install and use

Install the archive from Marketplace or the plugin's GitHub Release. Open **Plugins → Forest → Apply theme**. The theme applies across Spaces on this device; Lite's Light, Dark or System setting selects the palette. Choose **Use default theme** to restore the built-in appearance. Uninstalling the active theme also restores it.

The package contains validated CSS only. It has no executable code, network access, remote fonts or access to Space files. CLI Serve, Android and iOS do not support this host theme.

## Development

Use Node.js 22.12 or later and the pinned public SDK/tools 0.9.0:

```sh
npm ci
npm run check
npm run pack:plugin
```

The archive and SHA-256 checksum are written to `dist/`.
