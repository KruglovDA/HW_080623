# Краткое руководство по Git
## Основные команды
### Работа с локальным репозиторием
* git init - создает локальный репозиторий
* git commit - создает коммит
* git add - добавляет файл (-a и git commit -am - делает то же самое)
* git log - вызывает список всех коммитов (сохранений)
* git diff - показывает разницу между сохраненной версией и нынешней
* git checkout - епреключение между версиями
* git branch - выводит список веток ( * указана ветка, в которой сейчас находитесь)
* git branch <Название новой ветки> - создает новую ветку
* git merge <Название ветки> - сливает 2 ветки (в ту, в которой находимся, ту, чье название напишем)
* git branch -d <Название ветки> - удаляет ненужную ветку
* git checkout -b <название ветки> - создает новую ветк и сразу переключает а неё
* git rebase <куда> - перемещает копию коммита в ветку, где находимся
* <^> и <~> используются как относительные ссылки, чтобы вернуться на предыдущий коммит. ^ - на 1 коммит ранее, ~(num) - на несколько коммитов, сколько указано в num
* git reset - переносит на предыдущий коммит (можно также использовать относитепльные ссылки)

### Работа с удаленным репозиторием на github
* git clone <ссылка на репозиторий> - копирует удаленный репозиторий в локальный
* git pull - добавляет к локальный репозиторий информацию из внешнего, автоматчески делая merge
* git push - отправляет свою версю репозитория во внешний репозиторий
* pull request - запрос на вливание изменений в удаленный репозиторий (к другому владельцу)
* git revert - отменяет изменения и делится отмененными изменениями

### Настройка совместной работы
1. Создать аккаунт на GitHub
2. Создать локальный репозиторий
3. Подружить локальный и удаленный репозиторий
4. Сделать git hush 

### Как сделать pull request
* Сделать folk (ответвление)
* Сделать git clone СВОЕЙ версии репозитория
* Сделать новую ветку и в ней внести изменения
* Сделать коммит
* Отправить на GitHub
* В GitHub нажать кнопку pull request

## Выделение текста
Чтобы сделать текст полужирным, нужно обрамить его 2-мя звездочками (**) или 2-мя знаками нижнего подчеркивания (__). **Вот так** или __вот так__

Чтобы сделать текст курсивом, нужно обрамить текст звездочкой (*) или знаком нижнего подчеркивания (_). *Вот так* или _вот так_

Чтобы сделать текст зачеркнутым, нужно обрамить его 2-мя волнистыми черточками (~~). ~~Вот так~~

Альтернативные способы выделения текста жирным или курсивом нужны для того, чтобы мы могли совмещать оба этих способа. Например, _текст может быть выделен курсивом и при этом быть **полужирным**_. 

Чтобы атьть ололовок, нужно перед текстом поставить решетку (#).

Чтобы сделать подзаголовок, нужно перед текстом поставить 2 решетки (##).

## Списки 

Чтобы сделать нумерованный список, ножно каджый пункт пронумеровать. Например:
1. Первый пункт
2. Второй пункт

Чтобы сделать ненумерованный список, ножно перед пунктами ставить звездочку (*) или плюс (+). Например:
* Элемент 1
* Элемент 2
+ Элемент 3
+ Элемент 4

## Добавление изображения
Чтобы вставить изображение в текст, достаточно написать следующее:
![Привет, это Genshin](Gensh.jpg)

## Ссылки
Чтобы добавить ссылку, нужно сначала в квадратных скобках ([]) указать такст ссылки, а затем в круглых скобках (()) указать URL-адрес.

Например, ссылка на сайт [GeekBrains](https://gb.ru/)

## Цитаты
Чтобы вставить цитату, нужно обрамить текст обратными ковычками (`).
Например так:

`Программное обеспечение является одним из видов обеспечения вычислительной системы, наряду с техническим (аппаратным), математическим, информационным, лингвистическим, организационным, методическим и правовым обеспечением[13]. `

Или тремя обратными ковычками (```) вот так:

```
Я помню чудное мгновенье:
Передо мной явилась ты,
Как мимолетное виденье,
Как гений чистой красоты.
```

## Работа с таблицами
Чтобы вставить таблицу, текст необходимо обрамлять вертикальной чертой (|) и дефисвми (-). Вертикальная черта используется для разделения столбцов, а дефисы - для создания заголовков каждого столбца.

Например:

| First Header | Second Header |
| --- | --- |
| Content Cell | Content Cell |
| Content Cell | Content Cell |

Чтобы сделать вравнивание текста, используется двоеточие (:) слева, справа или с обеих сторон.

Например:

| First Header | Second Header | Third Header |
| :--- | :---: | ---: |
| Cell | Cell | Cell |
| Cell | Cell | Cell |

Чтобы включить вертикальную черту в качестве содержимого таблицы, нужно перед ней использовать (\).

Например:

| Название | Знак |
| --- | --- |
| Точка | . |
| Вертикальныя черта | \| |