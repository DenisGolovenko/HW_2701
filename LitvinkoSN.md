# Руководство по GIT

### Команды git

* init - создание локального репозитория
* add - добавление файла
* status - состояние репозитроия
* commit - делает коммит
* branch - выводит список веток
+ merge - слияние веток
+ push - выгрузка в удаленный репозиторий
+ pull - загрузка из удаленного репозитория

## Commit
Коммит в git репозитории хранит снимок всех файлов в директории. Почти как огромная копия, только лучше.

Ветки в Git, как и коммиты, невероятно легковесны. Это просто ссылки на определённый коммит.

## Git Merge
Первый способ объединения изменений, который мы рассмотрим - это git merge - слияние или просто мердж. Слияния в Git создают особый вид коммита, который имеет сразу двух родителей. Коммит с двумя родителями обычно означает, что мы хотим объединить изменения из одного коммита с другим коммитом и всеми их родительскими коммитами.

## Git Rebase
Второй способ объединения изменений в ветках - это rebasing. При ребейзе Git по сути копирует набор коммитов и переносит их в другое место.

## Git init
Для создания нового репозитория используется команда git init. Команду git init выполняют только один раз для первоначальной настройки нового репозитория. Выполнение команды приведет к созданию нового подкаталога .git в вашем рабочем каталоге. Кроме того, будет создана новая главная ветка.

## Git add
Команда git add добавляет изменение из рабочего каталога в раздел проиндексированных файлов. Она сообщает Git, что вы хотите включить изменения в конкретном файле в следующий коммит. Однако на самом деле команда git add не оказывает существенного влияния на репозиторий: изменения регистрируются в нем только после выполнения команды git commit.
Основное назначение команды git add состоит в переносе ожидающих изменений из рабочего каталога в раздел проиндексированных файлов Git.
Этот раздел удобно рассматривать как буфер между рабочим каталогом и историей проекта. Раздел проиндексированных файлов является одним из «трех деревьев» Git, наряду с рабочим каталогом и историей коммитов.

## Git push
Команда git push используется для выгрузки содержимого локального репозитория в удаленный репозиторий. Она позволяет передать коммиты из локального репозитория в удаленный.

## Git pull
Команда git pull используется для извлечения и загрузки содержимого из удаленного репозитория и немедленного обновления локального репозитория этим содержимым. Слияние удаленных вышестоящих изменений в локальный репозиторий — это обычная задача рабочего процесса, возникающая при совместной работе на основе системы Git. Команда git pull на самом деле представляет собой комбинацию двух других команд: git fetch и git merge. На первом этапе git pull выполняется команда git fetch, ограниченная локальной веткой, на которую указывает HEAD. Сразу после загрузки содержимого команда git pull выполняет слияние. Для слитого содержимого создается новый коммит, а указатель HEAD обновляется и начинает указывать на этот новый коммит.