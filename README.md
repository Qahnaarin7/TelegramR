# TelegramR

TelegramR is an unofficial Telegram Desktop client for Windows x64. It runs alongside the official app using its own profile. The installer adds a Start menu shortcut and offers a desktop shortcut.

[Download the latest Windows installer](https://github.com/Qahnaarin7/TelegramR/releases/latest)

## Features

- **Ghost mode:** separate controls for online presence, read receipts, and typing or recording indicators.
- **Sending:** optional 12-second delay for text and supported media, silent sending, a queue with cancellation, and per-chat overrides.
- **Local history:** an encrypted, searchable archive for received text from deleted messages and earlier edits. Expand earlier versions inside the message bubble.
- **Stickers and backups:** local favorite stickers and encrypted backups of settings and the favorites list.
- **Activity and Windows integration:** own activity time when Telegram provides it, a blue taskbar icon, and a separate tray icon that adapts to the Windows theme.
- **Updates:** checks for signed TelegramR releases, rollback, and a manual check of the latest official Telegram Desktop version.

Silent sending delivers a notification without sound. Other Telegram clients manage their own reminders and online presence. The local archive covers text received by TelegramR.

## Source and build

TelegramR 0.5.3 is based on Telegram Desktop v7.4.7, commit `85d55638476185e9af32aac888371ef9da06cfb9`. Clone the upstream repository, check out that commit, initialize its submodules, and apply the cumulative patch with `git apply TelegramR-source.patch`. The matching release source archive includes the patch, the Windows installer recipe, the updater helper source, and build instructions.

Use MSVC 14.44, static Qt 6.11.2, OpenSSL 3.5.9, and Ninja Multi-Config. Configure a Windows x64 Release build with your own Telegram API credentials and `DESKTOP_APP_DISABLE_AUTOUPDATE=ON`.

[Upstream source](https://github.com/telegramdesktop/tdesktop/tree/v7.4.7) · [TelegramR releases](https://github.com/Qahnaarin7/TelegramR/releases)

## Updates and license

TelegramR verifies an Ed25519-signed release manifest and checks the installer’s SHA-256 and size before installation. The official version check shows the upstream release and compares it with the version used by TelegramR. Upstream changes are integrated into a new TelegramR build.

Licensed under GPL-3.0. See LICENSE and LEGAL for details.
