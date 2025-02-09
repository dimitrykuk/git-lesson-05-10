# git-lesson-05-10

# Инструкция по работе в Git

## Команды в VS code (не связано с Git)

**cd** <название папки> или <путь к папке> - переход в папку с <названием> из корня

**cd ..** - переход на адрес выше (в перспективе к корню)

**mkdir <название папки>**  - создание папки в нашей дирректории

**new-item <название файла.рисшир>** - создание файла в нашей дирректории

**pwd** - вывести в териминале текущий адрес

**ls** - вывести в теримнал список всех имеющихся файлов и папок в текущей дирректории

**rm <название файла.рисшир>** или **rm <название папки>** - удалить файл или папку

## Общие команды в Git

git config —global user.name "User_name" - Инициализация имени пользователя (глобальная)

git config —global user.email "user_email" - Инициализация почты пользователя (глобальная)

git --version (можно просто git version)- посмотреть версию Git

git status - проверка состояния файлов в текущей папке

git add <название файла.рисшир> - добавление в версию сделанных изменений в файле

git add . - добавление всех измененний в версию

git reset . - убрать из версии все файлы

git commit -m "коментарий" - сохранение версии с коментарием

git commit -am "коментарий" - то же, что и предыдущее, только применимо если ранее уже использовался git add в этой ветке и не требует его повторного написания

git branch <название ветки> - создание ветки с таким-то названием

git branch - просмотр имеющихся веток в проекте (журнал веток)

git branch -b <название ветки> - создание ветки с переходом в неё

git branch -d <название ветки> - удалить ветку, если она была слита с другой

git branch -D <название ветки> - удалить ветку вне зависимости от того слита она или нет

git checkout <ХЭШ№> - перейти на сохранение с таким-то ХЭШем

git checkout <название ветки> - перейти в актуальную версию такой-то ветки

git diff <ХЭШ№> - показать разницу между текущей версией и таким-то ХЭШем

git diff <ХЭШ№1> <ХЭШ№2> - показать разницу между ХЭШ№ и ХЭШ№2

git merge <название ветки> - слить в текующую ветку указанную

git log - проверка имеющихся сохранений (журнал сохранений)

git log --graph - показать дерево commit-ов

## Работа в локальном репозитории

**git init** - инициализация локального репозитория (начало работы в выбранной папке)

*В репозитории, где начинается работа не должно внутренних репозиториев*

## Работа в удаленном репозитории

*Варианты добавления удаленного репозитория:*

1. *Можно склонировать имеющийся на чужом аккаунте GitHub репозиторий.*
2. *Создать локальный репозиторий и отправить на аккаунт.*

git clone <адрес репозитория> - клонирует удаленный репозиторий с указанным адресом (после адреса можно указать название папки)

git pull - стянуть с удаленного репозитория все изменения и слить с имеющимся в локальном

git push - отправить из локального репозитория в удаленный все изменения

Для того, чтобы внести изменения в чужой репозиторий необходимо:

1. Сделать копию (вилку) чужого репозитория через Fork на странице интересующего репозитория - добавить копию к себе на аккаунт.
2. На странице копии у себя на аккаунте скопировать ссылку на удаленный репозиторий.
3. В терминале Git указать git clone <ссылка> - сделать локального клона.
4. Внести изменения в проект.
5. Отправить изменения к себе на аккаунт - git push.
6. Запросить у хозяина исходников рассмотреть возможность принятия изменений в главный проект - pull request

## Прочее

.gitignore - файл, в котором можно указать название других файлов и игнорировать их в git status

q - выход из большого списка в терминале (например? при просмотре сохранений через git log)
