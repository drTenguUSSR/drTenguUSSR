# общая информация

## npm, глобально установленные пакеты

проверка устаревших пакетов

npm outdated -g

обновление одного

npm update -g <package_name>

обновление всех

npm update -g

rem: выполнение "npm update"  создает файл "package-lock.json"

## chrome ungoogled обновление

[any_auto_updates_on_ungoogled_chromium](https://www.reddit.com/r/browsers/comments/15g640f/any_auto_updates_on_ungoogled_chromium/?rdt=46330)

[chrlauncher](https://github.com/henrypp/chrlauncher/issues/92#issuecomment-343274418)

winget upgrade -e eloston.ungoogled-chromium

## chocolatey (choco) обновление

[chocolatey upgrade](https://docs.chocolatey.org/en-us/choco/commands/upgrade)

choco list
choco outdated
choco upgrade all

nb: рекомендуется запуск от как Администратора
choco upgrade chocolatey

результат

````cmd
C:\ProgramData\chocolatey\logs\chocolatey.log
````
