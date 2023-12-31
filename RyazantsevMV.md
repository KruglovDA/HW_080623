# Краткое руководство по **git**
## Основные команды
* git init - создаёт локальный репозиторий
* git commit -m "comment" - создаёт коммит c коментарием comment
* git commit amend -m "new_comment" - изменить комментарий последнего commit на new_comment
* git add - добавляет файл в сохранение (-а в git commit -am - делает то же самое)
* git status - вывод состояния отслеживаемых файлов
* git log - история изменений
* git diff - сравнение изменений файлов
* git branch branch_name - создать ветку branch_name
* git checkout branch_name - переключиться на ветку branch_name
* git checkout [4 первых символа имени комита] - переключиться на комит с именем начинающимся с указанных символов, достаточно 4
* git merge branch_name - совместить ветку branch_name и ветку master
* git branch -d branch_name - удалить ветку branch_name 
## Работа с удалёнными репозиториями
* fork - ветвление проекта на github, Если вы хотите вносить свой вклад в уже существующие проекты, в которых у нас нет прав на внесения изменений путём отправки (push) изменений, вы можете создать своё собственное ответвление (fork) проекта. Это означает, что GitHub создаст вашу собственную копию проекта, данная копия будет находиться в вашем пространстве имён и вы сможете легко делать изменения путём отправки (push) изменений.
* git clone - с сервера забирается (pulled) каждая версия каждого файла из истории проекта. Фактически, если серверный диск выйдет из строя, вы можете использовать любой из клонов на любом из клиентов, для того, чтобы вернуть сервер в то состояние, в котором он находился в момент клонирования.
* git fetch [remote-name] - Данная команда связывается с указанным удалённым проектом и забирает все те данные проекта, которых у вас ещё нет. После того как вы выполнили команду, у вас должны появиться ссылки на все ветки из этого удалённого проекта, которые вы можете просмотреть или слить в любой момент. Когда вы клонируете репозиторий, команда clone автоматически добавляет этот удалённый репозиторий под именем «origin». Таким образом, git fetch origin извлекает все наработки, отправленные на этот сервер после того, как вы его клонировали (или получили изменения с помощью fetch). Важно отметить, что команда git fetch забирает данные в ваш локальный репозиторий, но не сливает их с какими-либо вашими наработками и не модифицирует то, над чем вы работаете в данный момент. Вам необходимо вручную слить эти данные с вашими, когда вы будете готовы.
* git push [remote-name] [branch-name] - Когда вы хотите поделиться своими наработками, вам необходимо отправить их в удалённый репозиторий. Команда для этого действия простая: git push **remote-name** **branch-name**. Чтобы отправить вашу ветку master на сервер origin (повторимся, что клонирование обычно настраивает оба этих имени автоматически), вы можете выполнить следующую команду для отправки ваших коммитов: **git push origin master**. Эта команда срабатывает только в случае, если вы клонировали с сервера, на котором у вас есть права на запись, и если никто другой с тех пор не выполнял команду push. Если вы и кто-то ещё одновременно клонируете, затем он выполняет команду push, а после него выполнить команду push попытаетесь вы, то ваш push точно будет отклонён. Вам придётся сначала получить изменения и объединить их с вашими и только после этого вам будет позволено выполнить push
* git pull - используется для извлечения и загрузки содержимого из удаленного репозитория и немедленного обновления локального репозитория этим содержимым. Слияние удаленных вышестоящих изменений в локальный репозиторий. 
## Более удобная работа с логом и коммитами
* git log --all --oneline выводит список комитов всех веток в одну линию 
* git log --graph - выводит лог веток в графическом виде.