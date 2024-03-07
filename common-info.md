# общая информация (рецепты)

## markDown ограничения

стили не работают (как тег <style></style>> так и атрибут тега типа
style="float: right;")
см. [полный список тегов запрещенных тегов](https://github.github.com/gfm/#disallowed-raw-html-extension-)

````text
<title>
<textarea>
<style>
<xmp>
<iframe>
<noembed>
<noframes>
<script>
<plaintext>
````

в рамках preformated text не работают выделения (*)

в рамках таблицы не работают выделения ни (\*) ни тегом (b)

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

[пример GitExtensions-squash-A.gif](images/GitExtensions-squash-A.gif)

## установленные пакеты

Preferences -> Package Control -> List Packages

## Markdown HTML Preview

[Markdown HTML Preview https://github.com/zeyon/MarkdownHtmlPreview](https://github.com/zeyon/MarkdownHtmlPreview)
[https://github.com/zeyon/MarkdownHtmlPreview](https://github.com/zeyon/MarkdownHtmlPreview)

нажать ctrl+shift+m

## MarkdownEditing

[репо MarkdownEditing https://sublimetext-markdown.github.io/MarkdownEditing/](https://sublimetext-markdown.github.io/MarkdownEditing/)

## Sublime Text Markdownlint

[плугин https://github.com/jonlabelle/SublimeLinter-contrib-markdownlint](https://github.com/jonlabelle/SublimeLinter-contrib-markdownlint)

[консольный клиент https://github.com/igorshubovych/markdownlint-cli](https://github.com/igorshubovych/markdownlint-cli)

````text
Usage: markdownlint [options] <files|directories|globs>

  MarkdownLint Command Line Interface

  Options:
    -V, --version                               output the version number
    -c, --config [configFile]                   configuration file (JSON, JSONC, JS, YAML, or TOML)
    -d, --dot                                   include files/folders with a dot (for example `.github`)
    -f, --fix                                   fix basic errors (does not work with STDIN)
    -i, --ignore [file|directory|glob]          file(s) to ignore/exclude (default: [])
    -j, --json                                  write issues in json format
    -o, --output [outputFile]                   write issues to file (no console)
    -p, --ignore-path [file]                    path to file with ignore pattern(s)
    -q, --quiet                                 do not write issues to STDOUT
    -r, --rules  [file|directory|glob|package]  include custom rule files (default: [])
    -s, --stdin                                 read from STDIN (does not work with files)
    --enable [rules...]                         Enable certain rules, e.g. --enable MD013 MD041 --
    --disable [rules...]                        Disable certain rules, e.g. --disable MD013 MD041 --
    -h, --help                                  display help for command
````

информация актуальна для (markdownlint -V) "0.39.0"
настройки правил - создать в рабочей папке .markdownlint.json
с содержимым

````json
{
  "MD013": {
       "code_block_line_length": 120
    } 
}
````

подробности [https://github.com/DavidAnson/markdownlint/blob/main/doc/md013.md](https://github.com/DavidAnson/markdownlint/blob/main/doc/md013.md)

### MD040/fenced-code-language

[список языков https://gitlab.com/gitlab-org/gitlab/-/issues/32881](https://gitlab.com/gitlab-org/gitlab/-/issues/32881)

````text
plaintext: When no language. Also used for output from shell commands. Replace text with this.
JavaScript: Replace js with this
html
ruby: Replace rb with this
shell: Replace bash and sh with this.
toml: Config files, like with Runner docs
ini: Simple config files, when not TOML (sometimes). Replace conf with this?
prometheus: Prometheus config
yaml: Replace yml with this
sql
asciidoc
dockerfile: Replace docker with this
erb
elixir
golang: Replace go with this
graphql
html
http
haml
json: Replace json-doc (broken) with this
markdown: Replace md with this
mermaid
nginx
python
php
perl
TypeScript: Replace ts with this.
xml
````

### включение HTML

[https://github.com/updownpress/markdown-lint/blob/master/rules/033-no-inline-html.md](https://github.com/updownpress/markdown-lint/blob/master/rules/033-no-inline-html.md)

````cmd
markdownlint --disable MD033 -- README.md
````

## markdown table

[https://copyprogramming.com/howto/set-table-column-width-via-markdown](https://copyprogramming.com/howto/set-table-column-width-via-markdown)

info:
Preferences -> Package Control -> List Packages

## Markdown Images

[https://github.com/xsleonard/sublime-MarkdownImages](https://github.com/xsleonard/sublime-MarkdownImages)

These can be activated with the command palette (cmd+shift+p):

````text
MarkdownImages: Hide Images
MarkdownImages: Show All Images
MarkdownImages: Show Local Images
MarkdownImages: Show Remote Images
````

## орфография

меню “View” - “Dictionary” под пунктом “Language - English” появиться пункт “russian-english”

Чтобы осуществить проверку (spellcheck) на ошибки в русско-язычном тексте в
редакторе Sublime Text, нужно выбрать в меню вышеназванный пункт -
“View” - “Dictionary” - “russian-english”, тем самым указав редактору,
какой - словарь использовать для проверки. А затем запустить
проверку орфографии (spellcheck), нажав клавишу F6. Повторное нажатие клавиши
отключает проверку орфографии.

игнорирование слов: C:\Users\sysop\AppData\Roaming\Sublime Text\Packages\User\Preferences.sublime-settings

"word_wrap": false,
  "index_files": true,
  "dictionary": "Packages/russian_english.dic",
  "ignored_words":
  [
    "БЭМ"
  ],
}
