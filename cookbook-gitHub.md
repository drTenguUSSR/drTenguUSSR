# cookbook-gitHub.md

## публикация через GitHub pages

[официальная документация](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

1. в корне репозитория сделать папку /docs и разместить в ней  
index.html и сопутствующих html/css/... файлов
2. сделать репозиторий публичным - в открытом репозитории
нажать setting (в верхнем меню, правее от "Insights")/
General/Danger Zone/Change repository visibility
3. Settings /слева в секции "Code and automation" выбрать "Pages"
    - пункт "Branch" - выбрать ветку
    - пункт "select folder" - выбрать "/docs"
    - нажать "Save"
4. результат - в верху страницы будет видна информация о доступности сайти типа

````html
Your site is live at https://drtenguussr.github.io/test4/
````

(также тут настраивается свой "Custom domain", не проверено)

## публикация на username.github.com без имени репозитория

чтобы сайт репозитория на pages.github.io был доступен
без указания имени репозитория через слеш, нужно, чтобы
имя репозитория соответствовало <логин> + "github.io"
пример - логин drTenguUSSR соотвественно нужно создать
(переименовать) репозиторий в "drTenguUSSR.github.io"
и он будет доступен в браузере как
[https://drTenguUSSR.github.io](https://drTenguUSSR.github.io)
а [https://drtenguussr.github.com](https://drtenguussr.github.com)
работать не будет
, НО<br>
если создать еще репозиторий и назвать "0471.github.io"
то при попытке открыть
[https://0471.github.io](https://0471.github.io)
будет ошибка HTTP/404
