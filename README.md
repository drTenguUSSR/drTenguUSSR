# drTenguUSSR main

![avatar](images/tengu-port.png)
## проект TengedSedsvcEmu

TengedSedsvcEmu пет-проект реализующий интерфейс СЭДсервиса

[СЭД-сервис в рамках CMJ](https://sup.inttrust.ru:8446/prjdocs/master/specs/sedsvc/index.html)

[СЭДсервис как отдельный компонент](https://sup.inttrust.ru:8446/prjdocs/sedsvc/master/specs/sedsvc/index.html)

[подробности ../../../TengedSedsvcEmu](../../../TengedSedsvcEmu)

<table>
  <caption>
    TengedSedsvcEmu
  </caption>
  <thead class="header">
    <tr>
      <th width="10%">№</th>
      <th width="45%">оригинальная реализация и проблемы</th>
      <th width="45%">TengedSedsvcEmu</th>
    </tr>
  </thead>
<tbody>
<tr><td>1</td><td valign="top">
    Для отображения пользовательского интерфейса
    используется HTML 3.2/4.0 внутри JSP страницы
</td><td valign="top">
    Для отображения пользовательского интерфейса
    используется HTML5 + CSS3. применяются семантические теги и БЭМ
</td></tr>

<tr><td>2</td><td valign="top">
    для определения url точки доступа применяется серверный компонент,
    написанный на java
    <ul>
    <li>пояснение-1: если URL точки входа определяется сервером, то
        корректный проброс порта через промежуточный сервер (proxy)
        становится затруднительным</li>
    <li>
    пояснение-2: если адрес определен не верно, то нет возможности его исправить
    </li>
</td><td valign="top">
    точка входа сервера определяется клиентом, исходя из текущего адреса
    страницы и имеется возможность ее редактирования
</td></tr>

<tr><td>3</td><td valign="top">
        серверная сторона написана на Java 8 + Spring 4.1
    </td><td valign="top">
        перевод на Java JVM актуальной версии LTS (21?)
        + SpringBoot + Kotlin [^1]
</td></tr>

</tbody>
</table>