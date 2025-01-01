# Git

## squash коммитов (GitExtensions)

1. выбрать коммит до которого squash
2. в контекстном меню выбрать "rebase current brunch on/Selected commit interactively..."
3. в диалоге "rebase current brunch interactively" подтвердить
4. для всех коммитов кроме верхнего поставить вместо "pick" "s"
5. нажать "сохранить" (на панели) и "закрыть" (window)
6. в открывшемся диалоге удалить или закоменировать через "#" коментарии
  и написать новый
7. нажать "сохранить" (на панели) и "закрыть" (window)
8. нажать push
9. в диалоге открывшемся диалоге - "Force push with lease"

![пример GitExtensions-squash-A.gif](images/GitExtensions-squash-A.gif)

## squash 2

описан в https://htmlacademy.ru/blog/git/how-to-squash-commits-and-why-it-is-needed

1. настроить редактор. notepad++
```cmd
git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"
```
2. Теперь перепишем историю с момента HEAD~5
``cmd
git rebase -i HEAD~5
``\
(pick - для первого комита; squash для сливаемых)
3. сохранить файл и закрыть редактор
4. в открывшемся редакторе оставляем только один коментарий
5. сохраняекм и закрываем редактор
6. выполнить ``git push --force`` команду
