# Инструкция по работе с git и ветками

## Создание репозитория
Для того, чтобы добавить версионность к созданной папке, и создать в ней локальный репозиторий, для этого необходимо открыть окно терминала в этой папке и написать команду *git init*. Тогда Ваша папка станет репозиторием, и в ней появится скрытая папка .git

## Добавление файлов в репозиторий
Добавить версионность к файлу, находящемуся в папке-репозитории, можно с помощью команды *git add*. Пишется она следующим образом *git add <название файла>*

## Создание коммитов
Для того, чтобы зафиксировать изменения в текущей версии используется команда *git commit*. Используется она следующим образом: *git commit -m "<Сообщение к коммиту>"*. Сообщение к коммиту писать **ОБЯЗАТЕЛЬНО**

## Просмотр истории коммитов
Для просмотра истории всех сделанных коммитов используется команда *git log*. Чтобы увидеть всю историю коммитов, в папке репозитория в терминале необходимо написать *git log*

## Переключение между коммитами
Для того, чтобы переключаться между коммитами, необходимо использовать команду *git checkout*. Используется она следующим образом: *git checkout <номер коммита>*. Номер коммита можно взять, просмотрев список всех коммитов. 

## Создание ветки
Для того, чтобы создать новую ветку используется команда *git branch*. В папке с репозиторием напишите команду *git branch <название ветки*. Проверить то, что ветка создалась можно с помощью команды *git branch* в папке с репозиторием.

## Переключение между вектками
Для того, чтобы переключиться между ветками используется команда *git checkout*. Применяется она следующим образом: в папке с репозиторием необходимо написать *git checkout <название созданной ветки>*

## Слияние веток
Слияние веток можно произвести, использовав команду *git merge*. Используется она следующим образом: в папке с репозиторием надо написать команду *git merge <сливаемая ветка*>, сделать это необходимо в ветке, куда происходит слияния. При слиянии веток возможны **КОНФЛИКТЫ**. В случае возникновения конфликта, необходимо вручную получить желаемую версию файла, после чего сделать коммит(см. инструкцию выше)

## Удаление веток
Удаление слитой ветки можно произвести с помощью команды *git branch -d*. Использется она следующим образом: в папке с репозиторием пишем команду *git branch -d <название удаляемой ветки>*. Удаляемая ветка должна быть **ОБЯЗАТЕЛЬНО СЛИТА** с какой-нибудь из существующих веток

## Работа с удаленными (дальними) репозиториями

Для загрузки данных в удаленный репозитарий сначала нужно к нему подключиться. Для чего:

* создаем аккаунт на [Github.com] пример, сервер может быть любымпш

* создаем у себя на компьютере локальный репозиторий

* необходимо "подружить" локальный и удаленный репозиторий Github подскажет как это сделать

Теперь, необходимо в локальном репозитарии создать коммит (минимум один) и с помощью команды __git push__ можем отправить его на сервер в удаленный репозиторий. Эта команда имеет два параметра - имя удаленного репозитория (origin) и ветку, в которую необходимо внести изменения (master — это ветка по умолчанию для всех репозиториев). В нашем случае мы будем писать комманду __git push --set-upstream origin remote_repositouies__ так, как мы создали отдельную ветку __remote_repositouies__ и внесли в нее изменения.

Для того, чтобы "выкачать" изменения с удаленного репозитория используется команда __git pull origin master__, которая вытягивает все изменения с удаленного репозитория к нам в локальный репозиторий. 

* Стоит обратить внимание! Команда __git pull__ составная состоит из __git fetch__+__git merge__. Тоесть она не только забирает изменения с удаленного репозитория, а еще и сливает ветки.

Так же можно "клонировать" удаленный репозиторий.

С помощью команды __git clone__ <адресс удаленного репозитория>, GitHub автоматически создаст новый локальный репозитарий в виде удаленного на собственном сервере. 