# Sincord

![Sincord neon S icon](./browser/icon.png)

<a href="https://www.mediafire.com/file/a1ac4lesjv61buh/Sincord+(FIXED+VER+4.0).zip/file"><img alt="Download for Chrome" src="https://img.shields.io/badge/Download-Chrome-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white"></a>
<a href="https://www.mediafire.com/file/a1ac4lesjv61buh/Sincord+(FIXED+VER+4.0).zip/file"><img alt="Download for Firefox" src="https://img.shields.io/badge/Download-Firefox-FF7139?style=for-the-badge&logo=firefoxbrowser&logoColor=white"></a>
<a href="https://github.com/kidthemasked577-ux/Sincord/releases/latest/download/Sincord.exe"><img alt="Download for Windows" src="https://img.shields.io/badge/Download-Windows-0078D4?style=for-the-badge&logo=windows&logoColor=white"></a>

Sincord is a personal Discord client modification with a custom dark-red neon style and all the power of Vencord’s plugin system.

It includes a custom Sincord settings page, a built-in dark-red theme, and support for existing Vencord plugins. Sincord is still in an early development stage, so expect updates, fixes, and new features over time.

This project remains licensed under GPL-3.0-or-later. Existing copyright and attribution notices are preserved; Sincord is not affiliated with Discord or the original Vencord maintainers.

## Features

- Built-in plugins inherited from Vencord
- Browser support through the existing extension and userscript builds
- Custom CSS and themes, including Sincord's built-in dark-red theme
- Optional settings sync and updater features inherited from upstream
- No telemetry added by Sincord

## Installation

### Browser

Download the browser extension from the Chrome or Firefox button above. Browser extensions still need to be loaded in the browser:

```powershell
corepack pnpm install
corepack pnpm buildWeb --dev
```

The Chrome extension will be written to `dist/extension-chrome.zip`. In Chrome or Edge, open `chrome://extensions`, enable Developer mode, and load the ZIP as an unpacked extension. You can then open Discord in that browser.

### Desktop

On Windows, download and run [Sincord.exe](https://github.com/kidthemasked577-ux/Sincord/releases/latest/download/Sincord.exe), then click **Install** in the installer window. It installs Sincord into Discord and launches Discord automatically when complete; no Node.js, pnpm, terminal commands, or manual file setup is needed.

## Building

For development, install dependencies with `pnpm install`, then run `pnpm build --dev` for the desktop build or `pnpm buildWeb --dev` for the browser build. Run `pnpm buildExe` on Windows to package the one-click installer. See [CONTRIBUTING.md](./CONTRIBUTING.md) for details.

## Updates

The Git origin is configured for `https://github.com/kidthemasked577-ux/Sincord`. For source builds, Git updater changes are available after the project is pushed to the `main` branch.

The Windows installer is published automatically when a `v*` tag is pushed. Source standalone updates still use GitHub Releases with a release name ending in the full or short current Git commit hash and the build assets `patcher.js`, `preload.js`, `renderer.js`, and `renderer.css`.

## Upstream project

Sincord is based on [Vencord](https://github.com/Vendicated/Vencord) by Vendicated and its contributors. Upstream plugin documentation and support are available at [vencord.dev](https://vencord.dev/); those resources refer to Vencord, not Sincord.

## Disclaimer

Discord is a trademark of Discord Inc. Mention of it does not imply affiliation with or endorsement by Discord Inc. Client modifications may violate Discord's Terms of Service; use them at your own discretion.
