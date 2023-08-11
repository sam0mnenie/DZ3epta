    # Инструкция для работы с Markdown
**!!Всегда сохранять файл перед commit ctrl + S**
###_Заголовки и цитаты имеют многоуровневый формат:_
#1 
##2 
###3 и т.д.
>11111111111111111111111111111111111111111111111111111111111111111111111
>>_222222222222222222222222222222222222222222222222222222222222222222222_
>>>**33333333333333333333333333333333333333333333333333333333333333333**
и т.д

## Выделение текста

==Выделение жёлтым==
Для выделения жёлтым цветом обрамите текст в два "равно". ==

*Курсив.*
Для выделения текста курсивом обрамите его звёздочкой. *

**Полужирный**
Для выделения текста полужирным обрамите его двумя звёздочками. **

!!!Важно Текст можно выделить полужирным или курсивом и знаками (*) или (_) соответственно.

!!! Важно Текст можно выделить полужирным знаком (**) и (__).

Альтернативные способы выделения текста полужирным или курсивом нужны для того, чтобы мы могли совмещать оба этих способа. Например, _текст может быть выделен курсивом и при этом быть **полужирным**_.

__!!!__
Используется для создания заметок.

~~Зачёркнутый~~
Для зачёркивания текста обрамите его двумя тильдами. ~~

## Списки

Для добавления списков с точкой достаточно добавить звёздочку или знак +.
* Элемент 1
* Элемент 2
* Элемент 3
+ Элемент 4

*Для добавления списков с нумерацией всё по стандарту.*

1.Первый элемент нумерованного списка.
2.Второй элемент.

## Работа с изображениями

Чтобы добавить изображение в текст достаточно написать следующее:
![Комментарий к картинке текстом](название картинки с форматом или ссылка)
![Logo](markdown.png)

## Цитаты

Для добавления цитаты используется >.
>Пример.

## Запомнить
### Установка имени пользователя и email:
* ==git config --global **user.name** ""== - устанавливает имя пользователя.
* ==git config --global **user.email** ""== - устанавливает email пользователя.
#### Отправление файла на github.
==git remote add origin https://github.com/L1GH7n1nG/testGeakBrains.git== - регистрация по ссылке на удалённый репозиторий(origin - название репозитория).
==git branch -M main== - обозначение основной ветки.
==git push -u origin main== - отправка локального репозитория на удалённый.

## Команды git
* ==git init== - для выделения папки репозитория git.
* ==git add== - добавление файла к отслеживанию git.
* ==git commit -m== - сохраняет текущее состояние(сохранение) и оставили текстовое напоминание -m "Текст(напоминание)"
* ==git diff== - показывает отличие текущего(сохранённого) файла от закоммиченного файла. - удалённые, + добавленные.
* ==git log== - показывает все коммиты и их id с комментариями.
* ==git checkout master== - выйти из документа в "мастер".
* ==git checkout и название commit== - вернуться к предыдущему сохранению.
* ==git commit -am ""== - сразу добавление файла и commit(только, если не было создано нового файла).
* ==git status== - показывает последние изменения, которые, возможно, вам нужно сохранить.
* ==git branch== - создание новой ветки внутри master(main).
* ==git checkout и название ветки== - переход к ветке внутри main.
* ==git merge <название_ветки>== - делает слияние в находящейся ветке с нужной веткой.
* ==git log --graph== - показывает подробные изменения с разветвлением.
* ==git branch -d <название_ветки>== - удаляет нужную ветку.
* ==git checkout -b <название_ветки>== - создают ветку и сразу переходит в неё.
* ==git push== - отправление локального репозитория на удалённый.
* ==git pull== - загрузка удалённого репозитория на компьютер.
* ==git clone <ссылка_на_репозиторий>== - загрузка удалённого репозитория на компьютер.
# Команды вне курса.
* ==git rebase <название_ветки>== - копирует ветку и коммит делая историю коммитов последовательными и красивыми.
__Пример: Переходим в изменяемую ветку. Копирует коммит в конец нужной нам ветки git rebase main - переносит коммит в конец нужной(или основной) ветки. Далее можно перенести все изменения перейдя в основную ветку main и сделав то же самое(rebase).__
* ==git checkout <название_ветки> и ^== в конце означает перемещение на один коммит назад. Аналогично ^^ и тд.
* ==git branch -f main HEAD~3== - -f принудительно переместит ветку (main) на 3 назад при помощи ~ и n(кол-во коммитов назад) от HEAD.
* ==git reset HEAD~n== - возвращается на несколько коммитов назад. (для локальной)
* ==git revert HEAD~n== - возвращается на несколько коммитов назад, создаёт копию коммита для удалённого репозитория. После можно использовать push.
* ==git cherry-pick <название коммита> кол-во без запятой== - копирует нужны нам коммиты в HEAD.
* ==git rebase -i HEAD~n== - позволяет отобрать коммиты из нужного нам кол-ва и выбросить нам ненужные, создав копии оставшихся. Плюс ко всему позволяет переставить коммиты местами в нужном нам порядке или соединить нужные изменения из коммитов.
* ==git commit --amend== - это удобный способ изменить последний коммит. Она позволяет объединить проиндексированные изменения с предыдущим коммитом без создания нового коммита. Ее можно использовать для редактирования комментария к предыдущему коммиту без изменения состояния кода в нем. Но такое изменение не только редактирует последний коммит, но и полностью его заменяет.
* ==git tag <название>== - создаёт тег, который нельзя перемещать.
* ==git describe <название>== - Теги являются прекрасными ориентирами в истории изменений, поэтому в git есть команда, которая показывает, как далеко текущее состояние от ближайшего тега,помогает сориентироваться после отката на много коммитов по истории изменений.

## Как дать запрос на изменения в чужой репозиторий.
1. Загрузить копию удалённого репозитория на github ==(Fork)==.
2. Клонировать удалённый репозиторий на свой компьютер ==(clone)==.
3. Создать ветку и вносить изменения только в этой ветке.
4. Commit изменения.
5. Загрузить изменения на свой удалённый репозиторий ==(push)==.
6. Подать запрос на изменения. ==(Compare & pull request).==

















