Хачатрян Кристине Артуровна, КЭО 2 курс
Самостоятельная работа. Дисциплина «Управление IT-проектами для корпоративного обучения».
Задание 1. Инвариантная самостоятельная работа.
1. Изучив конкретную систему управления IT-проектами корпоративного обучения, использовав одну из стратегий ветвления (branching strategies) на основе сервиса GitHub реализовать добавление функции в существующем программном IT-проекте веб-ориентированной компоненте образовательной среды, предварительно создать запрос на добавление функционала (issue), спланировать временные затраты. Оформление отчета по результатам работы и презентации или одностраничного сайта с основными результатами. Публичное выступление.

ИСР1. Примеры использования базовых команд Git

Создание нового репозитория

git init

Чтобы создать новый репозиторий, нам нужно открыть терминал, зайти в папку нашего проекта и выполнить команду init. Это включит приложение в этой конкретной папке и создаст скрытую директорию .git, где будет храниться история репозитория и настройки.

Команда git init используется для инициализации локального репозитория.

<img src="https://c.radikal.ru/c01/2112/2b/cf2473dc1bef.png" />

Определение состояния

git status

Команда git status — это еще одна важнейшая команда, которая показывает информацию о текущем состоянии репозитория: актуальна ли информация на нём, нет ли чего-то нового, что поменялось, и так далее. Запуск git status на нашем свежесозданном репозитории должен выдать:

<img src="https://a.radikal.ru/a30/2112/84/f49278af21c0.png" />

Подготовка файлов

git add
Команда git add используется, чтобы добавить отслеживание изменений, вносимых в файлы.
Мы можем выполнить команду к какому-то конкретому файлу: git add file.c или же к группе файлов, используя маску: git add "*.c". А также если мы хотим добавить все, что находится в директории, мы можем использовать: git add -A

<img src="https://a.radikal.ru/a18/2112/db/a51bae40dfaf.png" />

<img src="https://b.radikal.ru/b25/2112/23/3e8151c76851.png" />

Коммит(фиксация изменений)

git commit

Коммит представляет собой состояние репозитория в определенный момент времени. Это похоже на снапшот, к которому мы можем вернуться и увидеть состояние объектов на определенный момент времени. Чтобы зафиксировать изменения, нам нужно хотя бы одно изменение в области подготовки (мы только что создали его при помощи git add), после которого мы может коммитить: git commit

<img src="https://a.radikal.ru/a06/2112/fb/5ce84f875929.png" />

Отправка изменений на сервер

git push

Сейчас самое время переслать наш локальный коммит на сервер. Этот процесс происходит каждый раз, когда мы хотим обновить данные в удаленном репозитории. Команда, предназначенная для этого - git push. Она принимает два параметра: имя удаленного репозитория (мы назвали наш origin) и ветку, в которую необходимо внести изменения (master — это ветка по умолчанию для всех репозиториев).

Пример: git push origin master

<img src="https://a.radikal.ru/a03/2112/9f/0afa3ef2ce24.png" />

Клонирование репозитория

git clone

Чтобы скачать данные из репозитория и получить полностью работоспособную копию проекта, необходимо воспользоваться командой - git clone.

<img src="https://b.radikal.ru/b19/2112/91/379f3e39eb8f.png" />

Новый локальный репозиторий создается автоматически с GitHub в качестве удаленного репозитория.

Запрос изменений с сервера

git pull

Если мы сделали изменения в нашем удаленном репозитории, другие пользователи могут скачать изменения при помощи команды git pull.

Пример git pull origin mster

<img src="https://b.radikal.ru/b35/2112/eb/330aeee665bd.png" />

Ветвление

git branch

Основная ветка в каждом репозитории называется master. Чтобы создать еще одну ветку, используем команду branch - git branch name

<img src="https://d.radikal.ru/d26/2112/2d/11eed1d7a89c.png" />


Это создаст новую ветку, пока что точную копию ветки master.

git branch

Сейчас, если мы запустим branch, мы увидим две доступные опции:

<img src="https://d.radikal.ru/d08/2112/a5/4d145cf65dd5.png" />


master — это активная ветка, она помечена звездочкой. Но мы хотим работать с нашей “новой потрясающей фичей”, так что нам понадобится переключиться на другую ветку. Для этого воспользуемся командой checkout, она принимает один параметр — имя ветки, на которую необходимо переключиться - git checkout amazing_new_feature

<img src="https://b.radikal.ru/b15/2112/b0/0eaca9ed06a8.png" />

Слияние веток. Алгоритм для слияния

Шаг 1.

Наша “потрясающая новая фича” будет еще одним текстовым файлом под названием feature.txt. Мы создадим его, добавим и закоммитим:

<img src="https://b.radikal.ru/b31/2112/a1/66076a347fec.png" />

Шаг 2.

Изменения завершены, теперь мы можем переключиться обратно на ветку master.

<img src="https://c.radikal.ru/c03/2112/ec/410ee6062427.png" />

Шаг 3.

Теперь, если мы откроем наш проект в файловом менеджере, мы не увидим файла feature.txt, потому что мы переключились обратно на ветку master, в которой такого файла не существует. Чтобы он появился, нужно воспользоваться merge для объединения веток (применения изменений из ветки amazing_new_feature к основной версии проекта).

<img src="https://b.radikal.ru/b15/2112/84/4f353d120bd5.png" />

Шаг 4.

Теперь ветка master актуальна. Ветка amazing_new_feature больше не нужна, и ее можно удалить.

<img src="https://a.radikal.ru/a25/2112/d5/d376ea401c05.png" />
