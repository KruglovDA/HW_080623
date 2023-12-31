 ## Переименование файлов

Переименовать файл или папку можно параметром mv. Для него указывается источник source и назначение destination. Источник — реально существующий файл или папка, а назначение — существующая папка.

* git mv dir1/somefile.js dir2

При выполнении команды файл или папка, указанные как источник, будут перемещены в папку назначения. Индекс будет обновлён соответственно, но изменения нужно записать.

Чтобы выделить текст полужирным, необходимо обрамить его двойными звездочками(**) или ( __ ). Например **вот так** или __вот так__.

Это делается для того чтобы в тексте можно было использовать и то и другое.

##  Списки 
что - то написано , ...
* git branch - выводит список веток 
* git branch branch_name - сощдает новую ветку с именем 

## Отмена подготовленных и неподготовленных изменений

Восстановить файлы рабочего дерева, не подготовленные к коммиту, можно параметром checkout. Для проведения операции требуется указать путь к файлу. Если путь не указан, параметр git checkout изменит указатель HEAD, чтобы задать указанную ветку как текущую.

* git checkout somefile.js

Восстановить подготовленный файл рабочего дерева можно параметром reset. Потребуется указать путь к файлу, чтобы убрать его из области подготовленных файлов. При этом не будет производиться откат никаких изменений или модификаций — однако файл перейдёт в категорию не подготовленных к коммиту.
* _git config --global user.name "Tara Routray"_

Кроме того, командой *git config* можно изменять адрес электронной почты, привязанный к вашим коммитам Git. Новый адрес электронной почты будет автоматически отображаться во всех дальнейших коммитах, поданных на GitHub через командную строку.

* git config --global user.email "dev@tararoutray.com"

## Внимание! Не изменяйте публичные коммиты.

С помощью amend прекрасно исправляются локальные коммиты, а исправления можно передать в общий репозиторий. Однако изменять коммиты, уже доступные другим пользователям, не следует. Помните, что изменённые коммиты являются совершенно новыми, а предыдущий коммит уже не будет доступен в текущей ветке. Последствия будут такими же, как при отмене изменений публичного снимка
