# pi-telegram-sebas

Fork de `llblab/pi-telegram`:
- upstream: https://github.com/llblab/pi-telegram

## Diferencias en este fork

- agrega comando nativo de Telegram `/new`
- `/new` aparece en bot commands y ayuda del bridge
- `/new` se intercepta en el bridge, no se manda como texto normal al modelo
- implementación adaptada al runtime real del polling de Telegram: dispara el core `/new` internamente vía `sendUserMessage("/new", { deliverAs: "followUp" })`

## Estado

Probado end-to-end desde Telegram en `ballbox-first`.
