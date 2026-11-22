# Sincord

![Sincord neon S icon](./browser/icon.png)

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

This repository contains the Sincord source code, not a ready-made installer.

### Browser

<a href="https://github.com/kidthemasked577-ux/Sincord/releases/latest/download/extension-chrome.zip"><img alt="Download for Chrome" src="https://img.shields.io/badge/Download-Chrome-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white"></a>
<a href="https://github.com/kidthemasked577-ux/Sincord/releases/latest/download/extension-firefox.zip"><img alt="Download for Firefox" src="https://img.shields.io/badge/Download-Firefox-FF7139?style=for-the-badge&logo=firefoxbrowser&logoColor=white"></a>

These downloads are available after a release publishes `extension-chrome.zip` and `extension-firefox.zip` as assets. Releases are published manually.

After installing the dependencies, run:

```powershell
corepack pnpm install
corepack pnpm buildWeb --dev
```

The Chrome extension will be written to `dist/extension-chrome.zip`. In Chrome or Edge, open `chrome://extensions`, enable Developer mode, and load the ZIP as an unpacked extension. You can then open Discord in that browser.

### Desktop

After installing the dependencies, run:

```powershell
corepack pnpm install
corepack pnpm build --dev
corepack pnpm inject
```

Restart Discord completely to launch Sincord.

To remove it:

```powershell
corepack pnpm uninject
```

## Building

Install dependencies with `pnpm install`, then run `pnpm build --dev` for the desktop build or `pnpm buildWeb --dev` for the browser build. See [CONTRIBUTING.md](./CONTRIBUTING.md) for development details.

## Updates

The Git origin is configured for `https://github.com/kidthemasked577-ux/Sincord`. For source builds, Git updater changes are available after the project is pushed to the `main` branch.

Standalone builds use GitHub Releases. Each release name must end with the full or short current Git commit hash, and it must include the Sincord build assets: `patcher.js`, `preload.js`, `renderer.js`, and `renderer.css`. Publishing releases is a manual GitHub action and is not performed automatically.

## Upstream project

Sincord is based on [Vencord](https://github.com/Vendicated/Vencord) by Vendicated and its contributors. Upstream plugin documentation and support are available at [vencord.dev](https://vencord.dev/); those resources refer to Vencord, not Sincord.

## Disclaimer

Discord is a trademark of Discord Inc. Mention of it does not imply affiliation with or endorsement by Discord Inc. Client modifications may violate Discord's Terms of Service; use them at your own discretion.
