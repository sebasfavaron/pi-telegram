# π Telegram Extension

Use Telegram as a bridge into your live π session. Pair one Telegram user, then chat with π from Telegram while preserving the same session state, tools, queue, and session metadata already running locally.

![Telegram Bridge screenshot](./assets/telegram-bridge.png)

This repository is a fork of [`llblab/pi-telegram`](https://github.com/llblab/pi-telegram).

For the original project overview, installation, configuration, and full feature documentation, see the upstream README:
- https://github.com/llblab/pi-telegram

## Start Here

This fork adds a native Telegram `/new` command.

### `/new`

Use `/new` inside the Telegram DM with your bot to start a fresh Pi session.

Differences from upstream:
- adds `/new` as a reserved Telegram command
- includes `/new` in bot commands and bridge help
- intercepts `/new` at the bridge layer so it is not sent as normal model text
- triggers the core Pi `/new` command internally in a way compatible with the Telegram polling runtime

Tested end-to-end from Telegram on `ballbox-first`.
