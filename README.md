<div align="center">

<img src="https://raw.githubusercontent.com/mauringo/clipkeep-macos/main/docs/images/clipboard-assistant-icon.png" width="96" height="96" alt="Clipboard Assistant icon">

# Clipboard Assistant · Homebrew Tap

[![Cask checks](https://github.com/mauringo/homebrew-tap/actions/workflows/cask.yml/badge.svg)](https://github.com/mauringo/homebrew-tap/actions/workflows/cask.yml)
[![Latest app release](https://img.shields.io/github/v/release/mauringo/clipkeep-macos)](https://github.com/mauringo/clipkeep-macos/releases/latest)
[![MIT](https://img.shields.io/badge/license-MIT-green)](LICENSE)

A personal Homebrew tap for a native macOS clipboard manager.

[App & screenshots](https://github.com/mauringo/clipkeep-macos) · [Releases](https://github.com/mauringo/clipkeep-macos/releases) · [Issues](https://github.com/mauringo/homebrew-tap/issues)

</div>

## Install

Requires Homebrew, Apple Silicon, and macOS 13 or later:

```sh
brew install --cask mauringo/tap/clipboard-assistant
open "/Applications/Clipboard Assistant.app"
```

Homebrew adds this tap automatically. It may ask you to trust the third-party cask. This is a personal tap, separate from the official Homebrew catalog.

Already installed manually? Quit the app and move the old app bundle to Trash before switching, including any duplicate in `~/Applications`. Keep `~/Library/Application Support/ClipboardAssistant` to preserve saved history. Session-only history is lost when quitting.

Downloads are ad hoc signed and are not Apple notarized. macOS may block first launch; Homebrew does not remove that limitation. See the app's [distribution notes](https://github.com/mauringo/clipkeep-macos/blob/main/docs/DISTRIBUTION.md).

## Update from Terminal

Quit the app, then run:

```sh
brew update && brew upgrade --cask mauringo/tap/clipboard-assistant
open "/Applications/Clipboard Assistant.app"
```

Turn off **Clipboard Assistant → Automatically Check for Updates** and let Homebrew manage updates. Homebrew downloads a prebuilt app and keeps update control in Terminal. The optional in-app updater also downloads prebuilt apps starting with v1.7.0; older versions build source locally and take longer. No Swift compiler is needed for Homebrew installation or updates.

If you use a custom Homebrew app directory, reopen the app from that directory.

## Maintain the cask

For each app release, copy `Casks/clipboard-assistant.rb` from [the app repository](https://github.com/mauringo/clipkeep-macos), with the new version and exact SHA-256 checksum, into this repository. Commit and push the change so `brew update` can discover it. Never replace a published release archive without changing its version.

CI checks Homebrew style, cask metadata, and the release archive checksum. These checks do not assert Apple notarization or official Homebrew acceptance.

## License

MIT · Copyright © 2026 Mauro (mauringo).
