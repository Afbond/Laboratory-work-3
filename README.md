# Laboratory-work-3
**РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ**

**Факультет физико-математических и естественных наук Кафедра прикладной информатики и теории вероятностей**

**Отчёт по лабораторной работе №3**

**По предмету**

«Операционные системы»**

**Выполнил:**

Студент группы НПМбв-01-19

Студенческий билет номер №: 1032186403

Бондаренко Артем Федорович

**МОСКВА**

2023г.



**Цель работы**

Научиться оформлять отчёты с помощью легковесного языка разметки Markdown.


**Ход работы**

Перепишем предыдущую лабораторную работу на облегченном языке разметки Markdown.

***Начало переписывания прошлой лабораторной работы на языке Markdown***

**РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ**

**Факультет физико-математических и естественных наук**

**Кафедра прикладной информатики и теории вероятностей**

**Отчёт по лабораторной работе №2**

По предмету

**«Операционные системы»**

Выполнил:

Студент группы НПМбв-01-19

Студенческий билет номер №: 1032186403

Бондаренко Артем Федорович

**МОСКВА**

2023г.

**Содержание:**

Цель работы. (3 стр.)

Ход работы. (3 стр.)

Настройка github. (3 стр.)

Создание учетной записи git. (3 стр.)

Установка git-flow. (4 стр.)

Базовая настройка. (6 стр.)

Создание SHH ключей. (7 стр.)

Создание PGP ключей. (8 стр.)

Добавление PGP ключа в GitHub. (9 стр.)

Настройка автоматических подписей коммитов. (10 стр.)

Шаблон для рабочего пространства. (11 стр.)

Создание репозитория курса на основе шаблона. (11 стр.)

Настройка каталога курса. (12 стр.)

Выводы. (13 стр.)

Ответы на контрольные вопросы. (14 стр.)

**Цель работы**

Изучить идеологию и применение средств контроля версий.
Освоить умения по работе с git.


**Ход работы**

Создание учетной записи за github

 Создадим учётную запись на https://github.com.

Создали учетную запись. (Ссылка: рис.1)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P1.png)
 
Рис.1: Профиль на github

**Установка программного обеспечения**

Установка git-flow.

Обратимся к инструкции для уcтановки git-flow на CentOS (Ссылка: рис.2)

 ![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P2.png)
 
   Рис.2: Инструкция по установке git-flow на CentOS на ТУИСе
   

Введем в терминале. (Ссылка: рис.3)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P3.png)

Рис.3: Введенные команды для установки и результат

Способ для установки git-flow для cent-os выдает ошибку.

Попробуем способ для Fedora, так как способ для CentOs дал ошибку. (Ссылка: рис.4)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P4.png)

Рис.4: Введенные команды для установки git-flow для FedoraLinux

**Базовая установка**  **git**

– Зададим имя и email владельца репозитория:

– Настроим utf-8 в выводе сообщений git:

– Настройте верификацию и подписание коммитов git.

– Зададим имя начальной ветки (будем называть её master):

– Параметр autocrlf:

– Параметр safecrlf:(Ссылка: рис.5)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P5.png)

Рис.5: Результат введенных команд для базовой установки

**Создание ключей**  **SSH**

Сгенерировали ключи (Ссылка: рис.6)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P6.png)

Рис.6: Сгенерированный ключ

Подключили ключ к профилю на github(Ссылка: рис.7)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P7.png)

Рис.7: Прикрепленный SSH ключ к профилю github

**Создание ключей**  **PGP**

Генерируем ключ

gpg --full-generate-key

– Из предложенных опций выбираем:

– тип _RSA and RSA_;

– размер 4096;

– выберите срок действия; значение по умолчанию — 0 (срок действия не истекает

никогда).

– GPG запросит личную информацию, которая сохранится в ключе:

– Имя (не менее 5 символов).

– Адрес электронной почты.

– При вводе email убедитесь, что он соответствует адресу, используемому на

GitHub.(Ссылка: рис.8)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P8.png)

Рис.8: Выбор опций для генерации GPG ключа

Получим следующие сгенерированные ключи (Ссылка: рис 9)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P9.png)

Рис.9: сгенерированные публичные и приватные GPG ключи

**Добавление ключа**  **PGP**  **в**  **github****.**

Получим публичный блок сгенерированного ранее ключа. (Ссылка: рис.10)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P10.png)

Рис.10: блок публичного GPG ключа

Скопируем полученный блок на github и добавим PGP ключ (Ссылка: рис.11)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P11.png)

Рис.11 Добавление полученного GPG ключа на github и результат

**Настройка автоматических подписей коммитов git**

Используя введёный email, укажим Git применять его при подписи коммитов: (Ссылка: рис.12)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P12.png)

Рис 12: Настройка автоматической установки коммитов

**Создание репозитория курса на основе шаблона**

Создание каталога (Ссылка: рис.13) 

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P13.png)

Рис.13: создание каталога

Создание репозитория (Ссылка: рис.14)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P14.png)

Рис.14 Вид репозиториев на github после создания

Сам шаблон. (Ссылка: рис. 15)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P15.png)

Рис 15. Ссылка на шаблон, по которому будет создан репозиторий

Копирование представленного шаблона в репозиторий (Ссылка: рис.16)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P16.png)

Рис.16: Команды для клонирования репозитория по шаблону

**Настройка каталога курса**

Произведем необходимые действия, удалим ненужные файлы и применим необходимые настройки. (Ссылка: рис.17)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P17.png)

Рис. 17. Введение команд для настройки каталога курса

Введем команду push чтобы перенести изменения в github. (Ссылка: рис. 18)

![Image alt](https://github.com/Afbond/Laboratory-work-3/blob/main/P18.png)

Рис.18: Введение команды чтобы перенести изменения в репозиторий на github

# **Вывод, итог**

Таким образом, была изучена идеология и применение контроля версий, освоены умения по работе с git. Полученные знания были также применены на практике.

# **Ответы на контрольные вопросы**

1. Что такое системы контроля версий (VCS) и для решения каких задач они предназначаются?

Контроль версий, также известный как управление исходным кодом, — это практика отслеживания изменений программного кода и управления ими. Системы контроля версий — это программные инструменты, помогающие командам разработчиков управлять изменениями в исходном коде с течением времени.

2. Объясните следующие понятия VCS и их отношения: хранилище, commit, история, рабочая копия.

Основным понятием VCS является репозиторий (repository) – специальное хранилище файлов и папок проекта, изменения в которых отслеживаются. В распоряжении разработчика имеется так называемая "рабочая копия" (working copy) проекта, с которой он непосредственно работает. Рабочую копию необходимо периодически синхронизировать с репозиторием, эта операция предполагает отправку в него изменений, которые пользователь внес в свою рабочую копию (такая операция называется commit) и актуализацию рабочей копии, в процессе которой к пользователю загружается последняя версия из репозитория (этот процесс носит название update).

3. Что представляют собой и чем отличаются централизованные и децентрализованные VCS? Приведите примеры VCS каждого вида.

Централизованные и распределенные системы контроля версий

Системы контроля версий можно разделить на две группы: распределенные и централизованные.

Централизованные системы контроля версий

Централизованные системы контроля версий представляют собой приложения типа клиент-сервер, когда репозиторий проекта существует в единственном экземпляре и хранится на сервере. Доступ к нему осуществлялся через специальное клиентское приложение. В качестве примеров таких программных продуктов можно привести CVS, Subversion. 

Распределенные системы контроля версий

Распределенные системы контроля версий (Distributed Version Control System, DVCS) позволяют хранить репозиторий (его копию) у каждого разработчика, работающего с данной системой. При этом можно выделить центральный репозиторий (условно), в который будут отправляться изменения из локальных и, с ним же эти локальные репозитории будут синхронизироваться. При работе с такой системой, пользователи периодически синхронизируют свои локальные репозитории с центральным и работают непосредственно со своей локальной копией. После внесения достаточного количества изменений в локальную копию они (изменения) отправляются на сервер. При этом сервер, чаще всего, выбирается условно, т.к. в большинстве DVCS нет такого понятия как "выделенный сервер с центральным репозиторием". !

4.Опишите действия с VCS при единоличной работе с хранилищем.

Создаем репозиторий на github. Создаем каталог проекта, заходим туда с помощью «cd \*каталог проекта\*», инициализируем системы git с помощью команды «git init». Далее создаем заготовки добавляем через «git add .». Делаем первый коммит и выкладывает на github.

5. Опишите порядок работы с общим хранилищем VCS.

Когда вы хотите поделиться своими наработками, вам необходимо отправить их в удалённый репозиторий. Команда для этого действия простая: git push \<remote-name\> \<branch-name\>. Чтобы отправить вашу ветку master на сервер origin (повторимся, что клонирование обычно настраивает оба этих имени автоматически), вы можете выполнить следующую команду для отправки ваших коммитов:

« git push origin master»

Эта команда срабатывает только в случае, если вы клонировали с сервера, на котором у вас есть права на запись, и если никто другой с тех пор не выполнял команду push. Если вы и кто-то ещё одновременно клонируете, затем он выполняет команду push, а после него выполнить команду push попытаетесь вы, то ваш push точно будет отклонён. Вам придётся сначала получить изменения и объединить их с вашими и только после этого вам будет позволено выполнить push.

6.Каковы основные задачи, решаемые инструментальным средством git?

Хранение и использование информации.

7. Назовите и дайте краткую характеристику командам git.

Наиболее часто используемые команды git:

git init – создание основного дерева репозитория:

git pull – получение обновлений (изменений) текущего дерева из центрального репозитория:

git push – отправка всех произведённых изменений локального дерева в центральный репозиторий:

git status – просмотр списка изменённых файлов в текущей директории:

git diff – просмотр текущих изменения:

git add – добавить все изменённые и/или созданные файлы и/или каталоги

git add \*имена\_файлов\* – добавить конкретные изменённые и/или созданные файлы и/или каталоги.

git commit -am 'Описание коммита' – сохранить все добавленные изменения и все изменённые файлы:

git checkout -b \*имя\_ветки\* – создание новой ветки, базирующейся на текущей:

git checkout \*имя\_ветки\* – переключение на некоторую ветку:

(при переключении на ветку, которой ещё нет в локальном репозитории, она будет создана и связана с удалённой)

git push origin имя\_ветки – отправка изменений конкретной ветки в центральный репозиторий:

gitmerge --no-ff имя\_ветки – слияние ветки с текущим деревом:

git branch -d имя\_ветки – удаление локальной уже слитой с основным деревом ветки:

git branch -D имя\_ветки – принудительное удаление локальной ветки:

git push origin :имя\_ветки – удаление ветки с центрального репозитория:

8. Приведите примеры использования при работе с локальным и удалённым репозиториями.

Вот пример создания текстового файла и добавления его в локальный репозиторий.

Создадим тестовый текстовый файл hello.txt и добавим его в локальный репозиторий:

echo 'hello world' \> hello.txt

git add hello.txt

git commit -am 'Новый файл'

Вот пример команды для загрузки репозитория из локального каталога на сервер:

git remote add origin

ssh://git@github.com/\<username\>/\<reponame\>.git

git push -u origin master

9. Что такое и зачем могут быть нужны ветви (branches)?

Команда git branch — главный инструмент для работы с ветвлением. С ее помощью можно добавлять новые ветки, перечислять и переименовывать существующие и удалять их

Под каждую новую функцию должна быть отведена собственная ветка, которую можно отправлять в центральный репозиторий для создания резервной копии или совместной работы команды. Ветки feature создаются не на основе master, а на основе develop.

Когда работа над функцией завершается, соответствующая ветка сливается обратно с веткой develop. Функции не следует отправлять напрямую в ветку master. Как правило, ветки feature создаются на основе последней ветки develop.

10. Как и зачем можно игнорировать некоторые файлы при commit?

Git поддерживает игнорирование файлов, но сам его не настраивает. Для игнорирования файлов и директорий, программист должен создать файл .gitignore в корне проекта

Как только .gitignore создан и в него добавлен какой-то файл или директория, игнорирование заработает автоматически. Все новые файлы, попадающие под игнорирование, не отобразятся в выводе команды git status.

В процессе работы над любым проектом в директории с кодом создаются файлы, которые не являются частью исходного кода. Все эти файлы можно условно разделить на несколько групп:

Инструментарий

• Служебные файлы, добавляемые операционной системой (.DS\_Store в MacOS)

• Конфигурационные и временные файлы редакторов (например, .idea, .vscode)

Временные файлы

• Логи. В них содержится полезная информация для отладки, которая собирается во время запуска и работы приложения

• Кеши. Файлы, которые нужны для ускорения разных процессов

Артефакты

• Результаты сборки проекта. Например, после компиляции или сборки фронтенда

• Устанавливаемые во время разработки зависимости (например, node\_modules, vendor)

• Результаты выполнения тестов (например, информация о покрытии кода тестами)

Все это в обычной ситуации не должно попадать в репозиторий. Как правило, эти файлы не несут никакой пользы с точки зрения исходного кода.

Поэтому целесообразно и можно игнорировать некоторые файлы.

***Конец переписывания прошлой лабораторной работы на языке Markdown***

**Выводы**

Таким образом, были получены знания о том как оформлять отчёты с помощью легковесного языка разметки Markdown, а также конвертировать их в различные форматы.

