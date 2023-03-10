# Инструкция по работе с Git

## Шпаргалка по markdown.

---

Чтобы выделить текст *курсивом*, нужно использовать *

---

Текст **полужирный** оформляется при помощи **

---


> Цитаты оформляются при помощи угловой скобки. Также могут включать код.

---


### Картинка

![Куда же без котиков?](cat.jpg)

---

### Списки

* Элемент 1
* Элемент 2
* Элемент 3

1. Первый
2. Второй

---

### Ссылки

Это [ссылка](https://habr.com/ru/post/541258/ "Git для новичков") с тайтлом.

[Эта ссылка](https://habr.com/ru/post/542616/) без заголовка.



## Команды Git

git --version – какая версия Git установлена

git init – позволяет сделать из указанной папки репозиторий

git status – текущее состояние

git add – добавление файлов к отслеживанию

git commit – сохраняет текущее состояние

git log – журнал всех изменений

git checkout – возврат к состоянию указанного коммита, переход по веткам

git diff – сравнивает файл с уже закоммиченным

---

## Ветки

git branch - выводит список веток.

git merge - слияние веток.

git checkout -b <Имя ветки>- создание новой ветки и переключение на нее.