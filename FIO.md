# Инструкция по работе с Markdown

## Выделение текста

Текст, окруженный одинарными символами, выделяется курсивным шрифтом, а текст, окруженный двойными символами, выделяется полужирным шрифтом. Также, выделенный фрагмент может находиться в любой части слова. Текст, выделенный курсивом с использованием синтаксиса языка Markdown, выглядит следующим образом:

*Пример*

или так

**Пример**

можно выделить еще и так:

***Пример***


## Списки

Markdown поддерживает упорядоченные (нумерованные) и нупорядоченные (ненумерованные списки). Для формирования нупорядоченных списков используют такие маркеры как (*), (+) и (-). Все эти маркеры являются взаимозаменяемыми. 
Примеры:
* Список 1
* Список 2
* Список 3

или
+ Список 1
+ Список 2
+ Список 3
- Список 4

Для формирования упорядоченных маркеров используются числа с точками. Пример:

1. Список А
2. Список В
3. Список С



## Работа с изображениями

Вставка изображения имеет следующий вид:

![альтернативный текст](/путь/к/изображению.jpg)

иными словами он состоит из следующих элементов

* восклицательный знак;

* квадратные скобки в которых указывается альтернативный изображению текст;

* круглые скобки, содержащие URL-адрес или относительный путь изображения, а также (необязательно) всплывающую подсказку, заключённуе в двойные или одиночные кавычки.


## Ссылки

Markdown содержит два типа оформления ссылок:

* Гиперссылка с немедленным указанием адреса (внутритекстовая);

* Гиперссылка, подобная сноске.

Подразумевается, что помимо URL-адреса существует еще текст ссылки. Он заключается в квадратные скобки. Для создания внутритекстовой гиперссылки необходимо использовать круглые скобки сразу после закрывающей квадратной. Внутри них необходимо поместить URL-адрес. В них же возможно расположить название, заключенное в кавычки, которое будет отображаться при наведении, но этот пункт не является обязательным.

[пример](http://example.com/ "Необязательная подсказка")

При создании сносной гиперссылки вместо целевого адреса используется вторая пара квадратных скобок, внутри которых помещается метка, идентификатор ссылки (id).

[пример] [id]

Markdown позволяет также использовать неявно выраженный идентификатор (сокращенный). В этом случае метка не приводится, вместо неё текст гиперссылки используется и в качестве её имени, а вторая пара квадратных скобок остаётся пустою. Например, чтобы сделать слово «Example» гиперссылкой, ведущей на сайт http://example.com/, достаточно написать:

[Example] []

и затем определить гиперссылку:

[Example]: http://example.com/

В результате на экран выводится следующее: 

[Example][] [Example]: http://example.com/


## Таблицы

## Цитаты

Для обозначения цитат используется знак "больше" ">". Его можно вставлять как перед каждой строкой цитаты, так и перед первой строкой параграфа. так же можно создавать вложенные цитаты (цитаты внутри цитат). Для их разметки используют дополнительные уровни знаков цитирования ">". Примеры цитат:

> Это цитата
> в которой перед каждой строкой 
> ставится угровая скобка.

> Это пример цитаты, 
в котором уголовая скобка
ставиться перед началом нового параграфа.

> Второй параграф.

Вложенная цитата:

> первый уровень цитирования
>> второй уровень цитирования
>>> третий уровень цитирования

Уровень цитирования не может превышать 15-ть.


# Работаем с командами Git

## Основные команды Git

* git log — вызывать список действий и сохранений,
* git init — создать репозиторий в папке на локальной машине,
* git add — отслеживать добавленные файлы,
* git commit + комментарий — сохранить текущее состояние,
* git diff — показать разницу между версиями,
* git chechout — переключиться между разными версиями.


# Работа с ветками в Git

## Работа с черновиками

**git branch**

Если у нас несколько версий черновика, мы
можем вывести на экран ветку, где находимся,
командой git branch. Создать ветку можно командой git branch.
Делать это надо в папке с репозиторием: 

+ git branch <название новой ветки>

Переключение с одной ветки на другую произходит при помощи следующей команды:

+ git checkout <имя ветки>

Команда git log покажет состояние более новых
версий проекта. Но если вызвать эту команду из
самой «свежей» ветки, мы не увидим исходного
файла. Когда мы правим текст/код в текущей ветке,
автоматического слияния не происходит: можно
создавать один документ в разных версиях в разных ветках.

## Совмещение двух вариантов текста

При совмещении текста переходим из ветки в которой работам в ветку master при помощи команды **git checkout master**. Чтобы слить любую ветку с текущей, вызываем
**git merge <имя ветки для слияния с текущей>**.

## Удаление веток

Если ветка в которой мы работали больше не нужна, то ее можно удалить при помощи следующей команды:

* git branch -d <имя удаляемой ветки>


## Конфликт изменений

При работе в двух ветках одновременно может
возникнуть ситуация, когда в одной и другой
ветке мы по-разному изменили блок текста.
Если затем мы попробуем слить эти ветки, Git
сообщит о конфликте и предложит выбрать,
какие же изменения записать. Поэтому у проекта в репозитории должен быть один
ответственный пользователь, наделённый правом проводить
слияния и разрешать конфликты.

1. Создаем конфликт.
Добавляем следующую фразу:

 "This is  documentation."
"This is documentation."

"It contains lots of info."




## Визуализация всех веток

Визализация всех веток происходит при помощи следующей команды:

* git log --graph

где ключ -graf в связке с командой log позволяет отобразить коммиты в виде дерева.

# Работа с удаленными репозиториями

## Добавление удаленного репозитория

Чтобы добавить новый удаленный репозиторий, выполните команду 

* git remote add 

в терминале в каталоге, в котором хранится репозиторий.

Команда **git remote add** принимает два аргумента:

* имя удаленного репозитория, например, origin;
* URL-адрес удаленного репозитория, например, https://github.com/OWNER/REPOSITORY.git.


## Изменение URL-адреса удаленного репозитория

* git remote set-url

Эта команда изменяет существующий URL-адрес удаленного репозитория.

Команда **git remote set-url** принимает два аргумента:

- Имя существующего удаленного репозитория. Например, к распространенным вариантам относятся *origin* и *upstream*.
- Новый URL-адрес удаленного репозитория.


## Переименование удаленного репозитория

- git remote rename - команда ля переименования существующего удаленного репозитория.

Команда **git remote** rename принимает два аргумента:

1. Имя существующего удаленного репозитория, например, *origin*;
2. Новое имя удаленного репозитория, например, *destination*.


## Удаление удаленного репозитория

Чтобы удалить удаленный URL-адрес из репозитория, используйте следующую команду:

+ git remote rm

Команда **git remote rm** принимает один аргумент:

+ имя удаленного репозитория, например, destination.

При удалении удаленного URL-адреса из репозитория выполняется только отмена привязки для локальных и удаленных репозиториев. Сам удаленный репозиторий не удаляется.

## Прочие команды для работы с удаленным репозиторием

- git clone - загружает все изменения и позволяет слить все ветки на локальном компьютере и в удаленном репозитории.
- git pull - позволяет скачать все из текущего репозитория и автоматически сделать слияние с нашей версией.
- git push_ - позволяет отправить нашу версию репозитория на внешний репозиторий. Требует авторизации на внешнем репозитории.
- pull request - команда для предложения изменений, запрос на вливание изменений в репозиторий.
