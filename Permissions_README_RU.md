# Foundryx: Права доступа (Русский)

Этот документ перечисляет все permission-узлы Foundryx и поясняет, за что каждый отвечает. Все узлы находятся в пространстве `foundryx.*`. При отсутствии плагина разрешений действуют fallback-уровни операторов Minecraft (0 — все игроки, 2 — оператор второго уровня, 3 — оператор третьего уровня). Если используется LuckPerms или другая система, права нужно назначать вручную.

## Игроки (Fallback 0)

| Команда | Permission-узел | Описание |
| --- | --- | --- |
| `/home` | `foundryx.command.home` | Телепорт к сохранённому дому. |
| `/sethome` | `foundryx.command.sethome` | Создание или обновление дома. |
| `/delhome` | `foundryx.command.delhome` | Удаление дома. |
| `/homes` | `foundryx.command.homes` | Список всех домов игрока. |
| `/warp` | `foundryx.command.warp` | Телепорт к общему варпу. |
| `/warps` | `foundryx.command.warps` | Перечень доступных варпов. |
| `/spawn` | `foundryx.command.spawn` | Перемещение на спавн сервера. |
| `/tpa` | `foundryx.command.tpa` | Запрос телепорта к игроку (алиас: `/call`). |
| `/tpaccept` | `foundryx.command.tpaccept` | Принятие запроса телепорта. |
| `/tpdeny` | `foundryx.command.tpdeny` | Отклонение запроса телепорта. |
| `/balance` | `foundryx.command.balance` | Проверка личного баланса. |
| `/pay` | `foundryx.command.pay` | Перевод валюты другому игроку. |
| `/kit` | `foundryx.command.kit` | Получение набора предметов. |
| `/afk` | `foundryx.command.afk` | Вручную включает/выключает статус AFK. |
| `/near` | `foundryx.command.near` | Показывает игроков поблизости в заданном радиусе. |
| `/suicide` | `foundryx.command.suicide` | Мгновенный респаун. |
| `/motd` | `foundryx.command.motd` | Показ сообщения дня. |
| `/mail` | `foundryx.command.mail` | Открывает внутриигровую почту. |
| `/msg` | `foundryx.command.msg` | Личное сообщение (алиасы: `/tell`, `/m`). |
| `/helpop` | `foundryx.command.helpop` | Обращение к модераторам. |
| `/rules` | `foundryx.command.rules` | Отображает правила сервера. |
| `/help` | `foundryx.command.help` | Справочное меню с категориями команд. |

> **Важно:** При наличии плагина прав перечисленные команды нужно выдать явно, иначе игроки их потеряют.

## Персонал (Fallback 2)

| Команда | Permission-узел | Назначение |
| --- | --- | --- |
| `/setwarp` | `foundryx.command.setwarp` | Создаёт новый варп. |
| `/delwarp` | `foundryx.command.delwarp` | Удаляет существующий варп. |
| `/setspawn` | `foundryx.command.setspawn` | Задаёт точку спавна. |
| `/fly` | `foundryx.command.fly` | Включает полёт. |
| `/fly <игрок>` | `foundryx.command.fly.others` | Переключает полёт для другого игрока. |
| `/balance <игрок>` | `foundryx.command.balance.others` | Просмотр чужого баланса. |
| `/heal` | `foundryx.command.heal` | Мгновенно лечит цель. |
| `/heal <игрок>` | `foundryx.command.heal.others` | Лечит другого игрока. |
| `/feed` | `foundryx.command.feed` | Восстанавливает голод. |
| `/feed <игрок>` | `foundryx.command.feed.others` | Восстанавливает голод другого игрока. |
| `/repair` | `foundryx.command.repair` | Чинит предмет в руке. |
| `/repair all` | `foundryx.command.repair.all` | Чинит все предметы в инвентаре. |
| `/repair armor` | `foundryx.command.repair.armor` | Чинит экипированную броню. |
| Цвета `/nick` | `foundryx.command.nick.color` | Разрешает цветовые коды в нике. |
| Форматы `/nick` | `foundryx.command.nick.format` | Разрешает жирный/курсив и т. д. |
| `/kill` | `foundryx.command.kill` | Уничтожает цель. |
| `/time` | `foundryx.command.time` | Меняет время суток. |
| `/weather` | `foundryx.command.weather` | Меняет погоду. |
| `/effect` | `foundryx.command.effect` | Выдаёт или снимает эффекты. |

Эти права доступны операторам уровня 2 автоматически, но их можно уточнить через LuckPerms.

## Администрирование и модерация (Fallback 3)

| Команда | Permission-узел | Назначение |
| --- | --- | --- |
| `/back` | `foundryx.command.back` | Возвращает на предыдущую позицию. |
| `/createkit` | `foundryx.command.createkit` | Сохраняет текущий инвентарь как набор. |
| `/delkit` | `foundryx.command.delkit` | Удаляет набор. |
| `/tp` | `foundryx.command.tp` | Телепорт к игроку или координатам. |
| `/tphere` | `foundryx.command.tphere` | Призыв игрока к себе. |
| `/tppos` | `foundryx.command.tppos` | Телепорт на координаты. |
| `/nick` | `foundryx.command.nick` | Изменяет собственный ник. |
| `/nickreset` | `foundryx.command.nick.reset.others` | Сбрасывает ник другого игрока. |
| `/god` | `foundryx.command.god` | Включает неуязвимость. |
| `/god <игрок>` | `foundryx.command.god.others` | Переключает неуязвимость другому игроку. |
| `/gm` | `foundryx.command.gm` | Переключает режим игры. |
| `/gm <игрок>` | `foundryx.command.gm.others` | Меняет режим игры у другого игрока. |
| `/hat` | `foundryx.command.hat` | Перемещает предмет в слот шлема. |
| `/realname` | `foundryx.command.realname` | Показывает настоящий ник игрока. |
| `/helpop reply` | `foundryx.command.helpop.reply` | Отвечает на запросы helpop. |
| `/freeze` | `foundryx.command.freeze` | Блокирует перемещение игрока. |
| `/eco` | `foundryx.command.eco` | Управляет балансами напрямую. |
| `/ban` | `foundryx.command.ban` | Выдаёт перманентный бан. |
| `/tempban` | `foundryx.command.tempban` | Выдаёт временный бан. |
| `/banip` | `foundryx.command.banip` | Блокирует IP-адрес. |
| `/unban` | `foundryx.command.unban` | Снимает бан игрока. |
| `/unbanip` | `foundryx.command.unbanip` | Снимает IP-бан. |
| `/banlist` | `foundryx.command.banlist` | Показывает список банов. |
| `/kick` | `foundryx.command.kick` | Выбрасывает игрока с сервера. |
| `/vanish` | `foundryx.command.vanish` | Включает режим невидимости для персонала (алиас: `/v`). |
| `/whois` | `foundryx.command.whois` | Отображает профиль модерации. |
| `/list` | `foundryx.command.list` | Выводит форматированный список игроков. |
| `/tab reload` | `foundryx.command.tab.reload` | Перезагружает оформление списка игроков (tab-листа). |
| `/gc` | `foundryx.command.gc` | Отображает показатели производительности. |
| `/jail` | `foundryx.command.jail` | Заключает игрока в тюрьму. |
| `/setjail` | `foundryx.command.setjail` | Создаёт или обновляет тюрьму. |
| `/unjail` | `foundryx.command.unjail` | Освобождает заключённого. |
| `/mute` | `foundryx.command.mute` | Выдаёт бессрочный мут. |
| `/tempmute` | `foundryx.command.tempmute` | Выдаёт временный мут. |
| `/unmute` | `foundryx.command.unmute` | Снимает мут. |
| `/invsee` | `foundryx.command.invsee` | Открывает инвентарь другого игрока. |
| `/enderchest` (личный) | `foundryx.command.enderchest.small` | Доступ к личному удалённому эндер-сундуку. |
| `/enderchest` (расширенный) | `foundryx.command.enderchest.large` | Открывает расширенный сундук для персонала. |
| `/enderchest` (чужой) | `foundryx.command.enderchest.other` | Позволяет просматривать чужие эндер-сундуки. |
| `/clearchat` | `foundryx.command.clearchat` | Очищает общий чат у всех игроков (алиас: `/cc`). |
| `/clear` | `foundryx.command.clear` | Очищает инвентарь исполнителя или указанного игрока. |
| `foundryxstorage tojson`/`fxstorage tojson` | `foundryx.command.storage.migrate` | Экспортирует данные из БД в JSON для резервного копирования. |
| `foundryxstorage todb`/`fxstorage todb` | `foundryx.command.storage.migrate` | Импортирует JSON-резерв из файлов обратно в базу данных. |

### Дополнительные права для наказаний

| Permission-узел | Назначение |
| --- | --- |
| `foundryx.command.kill.exempt` | Защищает игрока от `/kill` без права форса у исполнителя. |
| `foundryx.command.kill.force` | Позволяет обойти защиту `/kill`. |
| `foundryx.command.kill.notify` | Присылает уведомления о применении `/kill`. |
| `foundryx.command.kick.exempt` | Делает игрока невосприимчивым к обычному `/kick`. |
| `foundryx.command.kick.force` | Разрешает кикать игроков с защитой. |
| `foundryx.command.kick.notify` | Сообщает о киках в чате. |
| `foundryx.command.ban.exempt` | Не даёт забанить игрока без дополнительного права. |
| `foundryx.command.ban.force` | Разрешает банить даже защищённых игроков. |
| `foundryx.command.ban.notify` | Отправляет уведомления о перманентных банах. |
| `foundryx.command.tempban.exempt` | Блокирует временные баны без права форса. |
| `foundryx.command.tempban.force` | Позволяет выдавать временный бан защищённым игрокам. |
| `foundryx.command.tempban.notify` | Сообщает о временных банах. |
| `foundryx.command.mute.exempt` | Защищает от бессрочного мута. |
| `foundryx.command.mute.force` | Даёт возможность выдать мут защищённому игроку. |
| `foundryx.command.mute.notify` | Присылает уведомления о выданных мутах. |
| `foundryx.command.tempmute.exempt` | Защищает от временного мута без права форса. |
| `foundryx.command.tempmute.force` | Разрешает временно мутить защищённых игроков. |
| `foundryx.command.tempmute.notify` | Уведомляет о временных мутах. |
| `foundryx.command.clear.exempt` | Не даёт очистить инвентарь командой `/clear`. |
| `foundryx.command.clear.force` | Позволяет очистить инвентарь даже защищённых игроков. |
| `foundryx.command.clear.notify` | Отправляет уведомления об очистке инвентарей. |

## Дополнительные узлы

| Permission-узел | Описание | Fallback |
| --- | --- | --- |
| `foundryx.chat.color` | Разрешает цветовое форматирование в общем чате. | Оператор уровня 2 |
| `foundryx.chat.format` | Разрешает жирный/курсивный/подчёркнутый/зачёркнутый стиль чата. | Оператор уровня 2 |
| `foundryx.afk.kick_exempt` | Игнорирует автоматический кик за AFK. | Оператор уровня 3 |
| `foundryx.command.list.hidden` | Позволяет `/list` показывать скрытых или невидимых игроков. | Оператор уровня 3 |
| `foundryx.kit.<id>` | Управляет доступом к конкретному набору. | Задаётся конфигурацией |

## Рекомендации

1. Выдавайте группам широкие права (`foundryx.command.*`), затем ограничивайте чувствительные команды отрицательными узлами.
2. Разделяйте роли модерации и строительства, выделяя отдельные наборы разрешений для каждой команды.
3. После подключения LuckPerms проверьте, что команды с пометкой «ручная выдача» действительно добавлены в нужные группы.
4. Добавьте `foundryx.command.storage.migrate` и `foundryx.command.tab.reload` в привилегированные группы, если делегируете резервное копирование данных или обслуживание таб-листа.

