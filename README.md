<p align="center">
  <img src="foundryx.png" alt="foundryx logo" width="160" />
</p>
<h1 align="center">FoundryX</h1>
<p align="center">
  <strong>All-in-one Minecraft server utility mod for Fabric, Forge, and NeoForge</strong>
</p>
<p align="center">
  <a href="#english"><strong>🇬🇧 English</strong></a> ·
  <a href="#русская-версия"><strong>🇷🇺 Русский</strong></a>
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Version-1.1.3-3b82f6?style=for-the-badge" alt="Version 1.1.3" />
  <img src="https://img.shields.io/badge/Minecraft-1.21.10-10b981?style=for-the-badge" alt="Minecraft 1.21.10" />
  <img src="https://img.shields.io/badge/Java-21-ec4899?style=for-the-badge" alt="Java 21" />
  <img src="https://img.shields.io/badge/License-Apache--2.0-f97316?style=for-the-badge" alt="License" />
</p>

---

<details open>
<summary id="english"><strong>🇬🇧 English</strong></summary>

## Overview

FoundryX brings a modern Essentials-style experience to cross-loader Minecraft 1.21.10 servers. A shared core module powers Fabric, Forge, and NeoForge builds while providing the same commands, configuration, and data storage in every environment. Persistent JSON storage keeps homes, warps, balances, jails, and moderation records in sync across restarts, and optional LuckPerms integration offers granular control over who can use what.

## Feature highlights

- **Player navigation** – Homes, spawn, warps, back-tracking, `/tpa` requests, fly toggles, gamemode switches, and god mode with configurable teleport delays and cancellation rules.
- **Economy & kits** – Built-in balance storage, `/pay`, and admin economy controls alongside JSON-driven kits with cooldown tracking and permission nodes per kit.
- **Moderation tools** – Ban lists, temporary bans, IP bans, jail regions, freezes, mutes, helpop, whois snapshots, mail, and inventory viewing keep staff informed and in control.
- **AFK & quality of life** – Automatic AFK detection, manual toggles, optional kick timers, nicknames with formatting control, `/hat`, `/heal`, `/feed`, `/repair`, MOTD, rules, and help menus with categorized descriptions.
- **Chat & tab customization** – Configure default name/message colors, separators, tab refresh rate, group ordering, and list headers directly from the TOML config file.

## Configuration

Running the mod for the first time creates `config/FoundryX.toml`. Key sections include:

- `language.language` – Switches between `en_us` and `ru_ru` translations.
- `teleport` and `tpa` – Delay settings and cancellation behaviour for home, spawn, warp, back, and `/tpa` teleports.
- `tab` and `list` – TAB refresh cadence and group ordering for `/list`.
- `afk` – Idle timeout, kick toggle, and kick delay.

Kits live in `config/FoundryX/kits.json`, created automatically as a template; edit it to define items, cooldowns, and display names.

</details>

<details>
<summary id="русская-версия"><strong>🇷🇺 Русский</strong></summary>

## Обзор

FoundryX переносит современный функционал Essentials на кросс-загрузочные серверы Minecraft 1.21.10. Общий модуль обеспечивает единый набор команд, настроек и хранения данных для Fabric, Forge и NeoForge. Данные о домах, варпах, балансах, тюрьмах и модерации сохраняются в JSON между перезапусками, а интеграция с LuckPerms (если установлена) даёт точный контроль за правами игроков.

## Ключевые возможности

- **Навигация игроков** — Дома, спавн, варпы, возврат на предыдущую точку, запросы `/tpa`, полёт, смена режима игры и «бог-режим» с настраиваемыми задержками телепорта и условиями отмены.
- **Экономика и наборы** — Встроенные балансы, `/pay` и админские команды экономики, а также наборы предметов из `kits.json` с отслеживанием перезарядки и отдельными правами на каждый набор.
- **Инструменты модерации** — Бан-листы, временные и IP-баны, зоны тюрьмы, заморозка, муты, helpop, подробный whois, внутренняя почта и просмотр инвентарей помогают персоналу держать сервер в порядке.
- **AFK и удобство** — Авто-детект AFK, ручное переключение, настраиваемый кик, никнеймы с форматированием, `/hat`, `/heal`, `/feed`, `/repair`, MOTD, правила и справка с категориями команд.
- **Чат и TAB** — Тонкая настройка цвета имён и сообщений, разделителей, частоты обновления TAB-листа, порядка групп и списка `/list` через TOML-конфиг.

## Настройка

При первом запуске создаётся `config/FoundryX.toml`. Основные блоки настроек:

- `language.language` — выбор перевода `en_us` или `ru_ru`.
- `teleport` и `tpa` — задержки и отмена телепортов для домов, спавна, варпов, `/back` и `/tpa`.
- `tab` и `list` — частота обновления TAB и порядок групп команды `/list`.
- `afk` — таймаут бездействия, включение кика и время до кика.

Файл `config/FoundryX/kits.json` создаётся автоматически и служит шаблоном для настройки наборов предметов, их кулдаунов и отображаемых названий.

</details>
