## Как работать с ГИТ.
1. git init - начало работы 
2. gii add - добавить папку 
3. git commit -m "сообщение" - сохранить файл с новым сообщением
4. git diff - посмотреть разницу между сохранениями
5. git checkout - переключаться междуу ветками
## Жирный и курсив
* *курсив*
* **жирный**
## Работа с ветками
1. git branch - показать все ветки
2. git branch имя - создать новую ветку
3. git checkout - переключаться между ветками 
4. git merge - слить ветки

## Как удалить ветку после синхронизации
git  branch -d name - удалить ветку после слияния
git branch -D  - удалить ветку без слияния
## Работа с удалкенными репозиториями.
1. Создаем репозиторий на сайте github
2. Если мы хотим открыть удаленный репозиторий в VS, то используем код: 
echo "# название репозитория" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/nastasyaly/1.git
git push -u origin main
3. Далее, чтобы перенести информацию из github в VS - нажимаем git pull, наоборот - git push