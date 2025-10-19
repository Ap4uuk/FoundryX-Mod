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
| `/balance` | `foundryx.command.balance` | Проверка личного баланса. |
| `/pay` | `foundryx.command.pay` | Перевод валюты другому игроку. |
| `/kit` | `foundryx.command.kit` | Получение набора предметов. |
| `/afk` | `foundryx.command.afk` | Вручную включает/выключает статус AFK. |
| `/suicide` | `foundryx.command.suicide` | Мгновенный респаун. |
| `/motd` | `foundryx.command.motd` | Показ сообщения дня. |
| `/tpa` | `foundryx.command.tpa` | Запрос телепорта к игроку. |
| `/tpaccept` | `foundryx.command.tpaccept` | Принятие запроса телепорта. |
| `/tpdeny` | `foundryx.command.tpdeny` | Отклонение запроса телепорта. |
| `/mail` | `foundryx.command.mail` | Открывает внутриигровую почту. |
| `/msg` | `foundryx.command.msg` | Личное сообщение другому игроку. |
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
| `/balance <игрок>` | `foundryx.command.balance.others` | Просмотр чужого баланса. |
| `/heal` | `foundryx.command.heal` | Мгновенно лечит цель. |
| `/feed` | `foundryx.command.feed` | Восстанавливает голод. |
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
| `/gm` | `foundryx.command.gm` | Переключает режим игры. |
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
| `/whois` | `foundryx.command.whois` | Отображает профиль модерации. |
| `/list` | `foundryx.command.list` | Выводит форматированный список игроков. |
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

## Дополнительные узлы

| Permission-узел | Описание | Fallback |
| --- | --- | --- |
| `foundryx.chat.color` | Разрешает цветовое форматирование в общем чате. | Оператор уровня 2 |
| `foundryx.afk.kick_exempt` | Игнорирует автоматический кик за AFK. | Оператор уровня 3 |
| `foundryx.kit.<id>` | Управляет доступом к конкретному набору. | Задаётся конфигурацией |

## Рекомендации

1. Выдавайте группам широкие права (`foundryx.command.*`), затем ограничивайте чувствительные команды отрицательными узлами.
2. Разделяйте роли модерации и строительства, выделяя отдельные наборы разрешений для каждой команды.
3. После подключения LuckPerms проверьте, что команды с пометкой «ручная выдача» действительно добавлены в нужные группы.

