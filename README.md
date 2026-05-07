# pi-telegram-sebas

This repository is a fork of [`llblab/pi-telegram`](https://github.com/llblab/pi-telegram).

## Fork scope

This fork exists to maintain a native Telegram `/new` command for starting a fresh Pi session from Telegram.

## Differences from upstream

Compared with upstream, this fork currently adds:

- a native Telegram `/new` command
- `/new` in the bot command list and bridge help text
- bridge-level interception for `/new`, so it is not forwarded as normal model text
- a runtime-compatible implementation that triggers the core Pi `/new` command internally via `sendUserMessage("/new", { deliverAs: "followUp" })`

## Status

Tested end-to-end from Telegram on `ballbox-first`.

## Upstream

Upstream repository:
- https://github.com/llblab/pi-telegram
