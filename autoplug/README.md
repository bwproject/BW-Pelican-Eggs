# ProjectBW AutoPlug для Pelican/Pterodactyl

Яйцо для запуска **AutoPlug** на панели Pelican/Pterodactyl.

> ⚠️ **Важно:** автоматическое обновление Java в AutoPlug должно оставаться отключённым. Автоматическая смена Java внутри контейнера может привести к несовместимости или повреждению окружения сервера.

## Особенности

- Конфигурация `autoplug/general.yml` не перезаписывается при каждом запуске.
- Конфигурация `autoplug/updater.yml` не перезаписывается при каждом запуске.
- Параметры яйца используются при первоначальном создании конфигурации.
- Поддерживается автоматическое обновление самого яйца через `meta.update_url`.
- AutoPlug устанавливается автоматически, если его JAR-файл ещё отсутствует.
- `server.properties` не заменяется, если файл уже существует.
- Можно задавать тип сервера, версию Minecraft, ключ AutoPlug и аргументы Java через переменные яйца.

## Автоматическое обновление яйца

Яйцо содержит ссылку на актуальную версию файла в репозитории ProjectBW:

`https://raw.githubusercontent.com/bwproject/BWGravitLauncher/main/pelican/eggs/autoplug/egg-autoplug.json`

После изменения яйца в GitHub Pelican/Pterodactyl сможет проверить эту ссылку и предложить обновление импортированного яйца.

## Переменные

| Переменная | Назначение |
|---|---|
| `SERVER_TYPE` | Тип программного обеспечения Minecraft-сервера. |
| `SERVER_KEY` | Ключ сервера AutoPlug. Храните его в секрете. |
| `GAME_VERSION` | Версия Minecraft. |
| `JAVA_ARGS` | Дополнительные аргументы запуска Java. |

## Благодарности

- AutoPlug — https://autoplug.one/
- Pterodactyl — https://pterodactyl.io/
- Исходная идея и основа — PteroPlug от Luna: https://github.com/ImLunaUwU/PteroPlug

## Примечание

Это версия ProjectBW, адаптированная под Pelican/Pterodactyl. Использование сторонних компонентов осуществляется в соответствии с их лицензиями и условиями.