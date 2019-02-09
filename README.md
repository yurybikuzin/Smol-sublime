# Smol-sublime

Репозиторий содержит файлы для поддержки  в [Sublime3](https://www.sublimetext.com/3)

- подсветки синтаксиса 
- комментариев 

для `*.view.tree`-файлов (проект [$mol](https://github.com/eigenmethod/mol))

## Подсветка синтаксиса

[view.tree.sublime-syntax](view.tree.sublime-syntax) - поддержка подсветки синтаксиса

[Пример (картинка)](screenshots/example.png)

### Особенности

Невалидные (в зависимости от контекста) символы подсвечиваются стилем `invalid.illegal` (красный фон, белый текст в цветовой схеме [Monokai Extended](https://github.com/jonschlinkert/sublime-monokai-extended)):
- если использован пробел вместо tab'а в начале строки: [Пример (картинка)](screenshots/space-indent.png)
- если использован tab вместо пробела внутри строки: [Пример (картинка)](screenshots/tab-inside-line.png)
- если использован недопустимый/неожиданный символ: [Пример (картинка)](screenshots/unexpected.png)

Адекватно подсвечивает закомментированную ветку дерева: [Пример (картинка)](screenshots/comments.png)

## Поддержка комментариев

[view.tree.tmPreferences](view.tree.tmPreferences) - поддержка комментариев (`CMD`+`/` - macOS, `Ctrl`+`/` - другие OS)

### Особенности

Корректно работают только однострочные комментарии (`CMD`+`/` в текущей строке)

Блочные (если выбрать блок строк и нажать `CMD`+`/`) комментарии работают некорректно

Но для "выключения" ветки `.tree` достаточно однострочных комментариев, так как подсветка реагирует на них адекватно, согласно [правилам `.tree`-синтаксиса](https://habr.com/ru/post/248147/): [Пример (картинка)](screenshots/comments.png)

## Установка

Поместите файлы [view.tree.sublime-syntax](view.tree.sublime-syntax) и [view.tree.tmPreferences](view.tree.tmPreferences) в папку `Packages/User` и перезапустите `Sublime 3` 

В `Sublime 3` в меню `View/Syntax/User` должен появиться пункт `ViewTree`

После открытия в `Sublime 3` `*.view.tree`-файла надо выбрать пункт меню `View/Syntax/Open all with current extension as .../User/ViewTree`

### Вопросы по установке

#### Как найти папку `Packages/User ?

В `Sublime 3` надо выбрать пункт меню `Sublime Text/Preferences/Browse Packages...`

Откроется файловый менеджер с текущей папкой `Packages`, содержащей папку `User`

Папка `User` - это и есть искомая папка `Packages/User`

#### Как найти пункт меню `Browse Packages...` ?

В `Sublime 3` надо в меню `Help/Search` ввести `Browse` и выбрать вариант `Menu Items: Preferences/Browse Packages...`







