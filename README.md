# РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ
## Факультет физико-математических и естественных наук
### Кафедра прикладной информатики и теории вероятностей

**ОТЧЕТ**
 **ПО ЛАБОРАТОРНОЙ РАБОТЕ № 2**
 
 *дисциплина:        Операционные системы*

 Студент:     ГАБРИЭЛЬ ТЬЕРРИ

 Группа: НКНбд 01-20

 МОСКВА 2021 г.

 # Цель работы :
 Изучить идеологию и применение средств контроля версий
 # Ход работы:  
 заходим по [ссылке](https://github.com/) и попадаем в наш аккаунт github. .( рисунок 1)

![](https://raw.githubusercontent.com/tgabriel22/Lab2/main/Images/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA1.png "Рисунок1")

Загрузим в виртуальную машину. запустим терминал и начнем работать с сервером репозитория. Настроим систему управления версиями git, как описано ниже, для сервера репозитория.( рисунок 2, 3)
![](https://raw.githubusercontent.com/tgabriel22/Lab2/main/Images/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA2.png "Рисунок 2")
![](https://raw.githubusercontent.com/tgabriel22/Lab2/main/Images/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA3.png "Рисунок 3")

Далее скопировали ранее сгенерированный открытый ключ из локальной консоли  в буфер обмена. Отправились на сайт https://github.com/ под нашей учетной записью, перешли в меню настроек GitHub . Выбрали SSH-ключи в боковом меню настроек GitHub и нажали кнопку Добавить ключ. После этого создали репозиторий под названием lab2. .( рисунок 4,5, 6)
![](https://raw.githubusercontent.com/tgabriel22/Lab2/main/Images/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA4.png "Рисунок 4")
![](https://raw.githubusercontent.com/tgabriel22/Lab2/main/Images/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA5.png "Рисунок 5")
![](https://raw.githubusercontent.com/tgabriel22/Lab2/main/Images/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA6.png "Рисунок 6")

**Подключение репозитория к github:**   создали репертуар (репозит): Mkdir reposit  / Создаём заготовку для файла README.md:  echo "# Лаб2" >> README.md /  Инициализируем системы git: git init  /Создаём заготовку для файла README.md:  git add README.md  /Делаем первый коммит и выкладываем на github: git commit -m "first commit" / git branch -M main / git remote add origin  https://github.com/tgabriel22/Lab2.git/  git push -u origin main. .( рисунок 7)
![](https://raw.githubusercontent.com/tgabriel22/Lab2/main/Images/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA7.png "Рисунок 7")

**Первичная конфигурация:**          Добавим файл лицензии: wget https://creativecommons.org/licenses/by/4.0/legalcode.txt  – Добавим шаблон игнорируемых файлов. Просмотрим список имеющихся шаблонов: curl -L -s https://www.gitignore.io/api/list . Затем скачаем шаблон, например, для C: curl -L -s https://www.gitignore.io/api/c >> .gitignore Добавим новые файлы: git add .    Выполним коммит: git commit -m “push”           Отправим на github: git push .( рисунок 8)
![](https://raw.githubusercontent.com/tgabriel22/Lab2/main/Images/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA8.png "Рисунок 8")

**Конфигурация git-flow**   Инициализируем git-flow: git flow init   / Проверьте, что Вы на ветке develop: git branch  / Создадим релиз с версией 1.0.0: git flow release start 1.0.0  / Запишем версию: echo "1.0.0" >> VERSION / Добавим в индекс: git add . /  git commit -m “ first version “ / Зальём релизную ветку в основную ветку: git flow release finish 1.0.0  / Отправим данные на github :  git push --all git push --tags Создадим релиз на github. (рисунок 9, 10)
![](https://raw.githubusercontent.com/tgabriel22/Lab2/main/Images/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA9.png "Рисунок 9")
![](https://raw.githubusercontent.com/tgabriel22/Lab2/main/Images/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA10.png "Рисунок 10")


# Вывод: 
### изучил идеологию и применение средств контроля версий.




## Контрольные вопросы:
1. Что такое системы контроля версий (VCS) и для решения каких задач они предназначаются? 
Системы контроля версий (Version Control System, VCS) применяются при работе нескольких человек над одним проектом. Обычно основное дерево проекта хранится в локальном или удалённом репозитории, к которому настроен доступ для участников проекта. При внесении изменений в содержание проекта система контроля версий позволяет их фиксировать, совмещать изменения, произведённые разными участниками проекта, производить откат к любой более ранней версии проекта, если это требуется
2. Объясните следующие понятия VCS и их отношения: хранилище, commit, история, рабочая копия. 
Хранилище (репозиторий) – это система, которая обеспечивает хранение всех существовавших версий файлов.
Commit - запись изменений.
История - список предыдущих изменений.
Рабочая копия – копия файла, с которой непосредственно ведётся работа (находится вне репозитория)
С помощью коммитов изменения, внесённые в рабочую копию, заносятся в хранилище. Благодаря истории можно отследить изменения, вносимые в репозиторий. Перед началом работы рабочую копию можно получить из одной из версий, хранящихся в репозитории. 
3. Что представляют собой и чем отличаются централизованные и децентрализованные VCS? Приведите примеры VCS каждого вида. 
В централизованных СКВ все файлы хранятся в одном репозитории, и каждый пользователь может вносить изменения. В децентрализованных их несколько, и они могут обмениваться изменениями между собой, а центрального репозитория может не существовать вообще.
Среди классических (т.е. централизованных) VCS наиболее известны CVS, Subversion, а среди распределённых — Git, Bazaar, Mercurial.
4. Опишите действия с VCS при единоличной работе с хранилищем. 
Получить нужную версию проекта (рабочую копию), внести в неё необходимые изменения, сделать нужный коммит, создав при этом новую версию проекта (старые не удаляются). 
5. Опишите порядок работы с общим хранилищем VCS. 
Аналогично единоличной работе, но также можно объединить внесённые разными пользователями изменения, отменить изменения или заблокировать некоторые файлы для изменения, обеспечив привилегированный доступ конкретному разработчику.
6. Каковы основные задачи, решаемые инструментальным средством git? 
Система контроля версий Git представляет собой набор программ командной строки. Доступ к ним можно получить из терминала посредством ввода команды git с различными опциями.
Git позволяет создавать локальные репозитории и вносить в них изменения, а также работать с удалёнными репозиториями.
7. Назовите и дайте краткую характеристику командам git. 
1)создание основного дерева репозитория: git init 
2)получение обновлений (изменений) текущего дерева из центрального репозитория: git pull 
3)отправка всех произведённых изменений локального дерева в центральный репозиторий: git push 
4)просмотр списка изменённых файлов в текущей директории: git status
5)просмотр текущих изменения: git diff 
6)сохранение текущих изменений: 
а)добавить все изменённые и/или созданные файлы и/или каталоги: git add . 
б)добавить конкретные изменённые и/или созданные файлы и/или каталоги: git add имена_файлов 
в)удалить файл и/или каталог из индекса репозитория (при этом файл и/или каталог остаётся в локальной директории): git rm имена_файлов 
7)сохранение добавленных изменений: 
а)сохранить все добавленные изменения и все изменённые файлы: git commit -am 'Описание коммита' 
б)сохранить добавленные изменения с внесением комментария через встроенный редактор: git commit 
8)создание новой ветки, базирующейся на текущей: git checkout -b имя_ветки 
9)переключение на некоторую ветку: git checkout имя_ветки (при переключении на ветку, которой ещё нет в локальном репозитории, она будет создана и связана с удалённой)
10)отправка изменений конкретной ветки в центральный репозиторий: git push origin имя_ветки 
11)слияние ветки с текущим деревом: git merge --no-ff имя_ветки 
12)удаление ветки: 
а)удаление локальной уже слитой с основным деревом ветки: git branch -d имя_ветки 
б)принудительное удаление локальной ветки: git branch -D имя_ветки 
в)удаление ветки с центрального репозитория: git push origin :имя_ветки
8. Приведите примеры использования при работе с локальным и удалённым репозиториями. 
Допустим, нужно добавить в проект новый файл file.txt
Загрузим нужную версию из удалённого репозитория: git checkout last (last – имя нужной нам ветки)
Добавим файл в локальный репозиторий: git add file.txt (файл лежит в том же каталоге, что и репозиторий)
Сохраним изменения: git commit –am “file.txt was added”
Отправим изменения в удалённый репозиторий: git push
9. Что такое и зачем могут быть нужны ветви (branches)? 
СКВ могут поддерживать работу с несколькими версиями одного файла, сохраняя общую историю изменений до точки ветвления версий и собственные истории изменений каждой ветви. Это удобно при работе над одним проектом нескольких человек, или если вносимые на каждой из ветвей изменения будут разительно отличаться (например, создание программ с разным функционалом на базе одного интерфейса).
10. Как и зачем можно игнорировать некоторые файлы при commit?
Во время работы над проектом так или иначе могут создаваться файлы, которые не требуется добавлять впоследствии в репозиторий. Например, временные файлы, создаваемые редакторами, или объектные файлы