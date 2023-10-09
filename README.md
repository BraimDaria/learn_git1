# Homework file

Добавлена инструкция по работе с git, включая нформацию о работе с удаленными репозиториями.

## Создание репозитория

*репозиторий это хранилище данных*

**git init** - создание репозитория

после создания репозитория git начинает отслеживать все изменения

## Сохранение изменений

*commit - фиксация, зафиксировать*

1. **cmd+S** - сохранить файл
2. **git add** /название файла/
|| **git add .** - добавит все файлы в папке

*если начать вводить название файла для добавления и нажать tab - название заполнится автоматически*

3. **git commit -m "комментарий к сохранению"** 

*git commit --amend -m “новый комментарий” - изменить комментарий для сохранения*

## Работа с ветками

**git branch** - вывести список веток
*(*) отмечает ту ветку, где мы сейчас располагаемся*

**git branch названиеновойветки** - создать ветку

**git checkout названиеветки** - переместиться на ветку

**git merge названиеветки** - для слияния ветки с другой, *делать из ветки с которой хотим слить*

**git branch -d названиеветки** - удалить ветку

*под каждое изменение лучше делать отдельную ветку - потом сливать с master - затем удалять не нужные
ветки*

## Работа с удаленными репозиториями

**git clone** *ссылка_гит_хаб* - открыть у себя удаленный репозиторий

чтобы выгрузить **свой репозиторий**: зайти на сайт github.com, выбрать new repo, идти по инструкции *push an existing repository*

чтобы **выгрузить измененный** репозиторий на github.com: сохранить изменения как обычно, ввести команду **git push** 

также можно вносить изменения прямо в github.com - через кнопку commit changes, а
чтобы изменения отразились и на компьютере - ввести команду **git pull**, она сливает изменения с нашим текущим репозиторием

**pull request** - для предложения изменений в чужой проект

для этого сначала делаем полную копию репозитория через кнопку **fork** - клонируем его через git clone - создаем отдельную ветку и в ней файл с описанием этого проекта

у нас появится точно такой же репозиторий, но уже на нашем аккаунте,
далее на github.com через кнопку **compare & pull reqest** - добавляем коммент об изменениях и оправляем измененный проект

*в гитхаб принято добавлять README файл с описанием программы*

## Полезные команды

**.gitignore** - создать такой файл - указать там имя файла из нашей папки, который должен игнорироваться

**git log** - посмотреть какие версии существуют (журнал изменений)

**git log –graph** - более детальное отображение дерева коммитов

**git checkout xxxx** - вернуться к одной из версий (по первым 4 символам из git log)

**git checkout master** - после переключения между версиями рекомендуется вернуться в актуальное состояние (на главную ветку)

**git diff** - разница между текущим состоянием файла и тем, что уже сохранено

**pwd** - путь к папке где находимся